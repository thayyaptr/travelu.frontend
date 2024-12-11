/// groupable-select
<template>
  <q-select
    v-bind="selectProps"
    :model-value="internalValue"
    @update:model-value="updateValue"
    :options="processedOptions"
    use-chips
    :emit-value="emitValue"
    :map-options="mapOptions"
    :option-value="optionValue"
    :option-label="optionLabel"
    :multiple="multiple"
    :filled="filled"
  >
    <template v-slot:option="scope">
      <template v-if="scope.opt.isGroup">
        <q-item-label
          header
          v-bind="scope.itemProps"
          style="font-weight: bold; font-size: 1.1em; color: black"
        >
          {{ scope.opt.group }}
        </q-item-label>
      </template>
      <template v-else>
        <q-item v-bind="scope.itemProps" v-on="scope" style="margin-left: 10px">
          <q-item-section>
            <q-item-label>{{ scope.opt[optionLabel] }}</q-item-label>
          </q-item-section>
        </q-item>
      </template>
    </template>
  </q-select>
</template>

<script setup>
import { ref, computed, watch } from "vue";
import { useQuasar } from "quasar";
import { defineProps, defineEmits } from "vue";

const props = defineProps({
  options: {
    type: Array,
    required: true,
  },
  disableGrouping: {
    type: Boolean,
    default: false,
  },
  groupBy: {
    type: String,
    required: false,
  },
  modelValue: {
    type: [String, Number, Array],
    default: () => [],
  },
  emitValue: {
    type: Boolean,
    default: false,
  },
  mapOptions: {
    type: Boolean,
    default: false,
  },
  multiple: {
    type: Boolean,
    default: false,
  },
  filled: {
    type: Boolean,
    default: false,
  },
  optionValue: {
    type: String,
    default: "value",
  },
  optionLabel: {
    type: String,
    default: "label",
  },
});

const emits = defineEmits(["update:modelValue"]);

const $q = useQuasar();

const internalValue = ref(props.modelValue);

const updateValue = (value) => {
  internalValue.value = value;
  emits("update:modelValue", value);
};

watch(
  () => props.modelValue,
  (newValue) => {
    internalValue.value = newValue;
  },
  { immediate: true }
);

const processedOptions = computed(() => {
  if (props.disableGrouping || !props.groupBy) {
    return props.options;
  }

  const grouped = [];
  let currentGroup = null;

  const result = [...props.options];
  result.sort((a, b) => {
    const aGroupValue =
      props.groupBy.split(".").reduce((obj, key) => obj && obj[key], a) || "";
    const bGroupValue =
      props.groupBy.split(".").reduce((obj, key) => obj && obj[key], b) || "";
    if (aGroupValue < bGroupValue) return -1;
    if (aGroupValue > bGroupValue) return 1;
    if (a[props.optionLabel] < b[props.optionLabel]) return -1;
    if (a[props.optionLabel] > b[props.optionLabel]) return 1;
    return 0;
  });

  result.forEach((option) => {
    const groupValue = props.groupBy
      .split(".")
      .reduce((obj, key) => obj && obj[key], option);

    if (groupValue !== currentGroup) {
      currentGroup = groupValue;
      grouped.push({ isGroup: true, group: currentGroup });
    }
    grouped.push(option);
  });

  return grouped;
});

const selectProps = computed(() => {
  const {
    options,
    disableGrouping,
    groupBy,
    modelValue,
    emitValue,
    mapOptions,
    optionValue,
    optionLabel,
    ...restProps
  } = props;
  return restProps;
});
</script>
