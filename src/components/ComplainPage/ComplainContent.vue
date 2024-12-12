<template>
  <div class="cover">
    <!-- Added top header space simulation -->
    <div class="header-space"></div>
    
    <div class="container">
      <div class="content-wrapper">
        <!-- Main Content Box -->
        <div class="main-box">
          <!-- Feedback Header Box -->
          <div class="feedback-header">
            <h2>Share Your Thoughts</h2>
            <p>We value your feedback and would love to hear about your experience.</p>
          </div>
          
          <!-- Rating Box -->
          <div class="rating-input">
            <q-rating
              v-model="rating"
              :max="5"
              size="2em"
              color="primary"
              icon="star_border"
              icon-selected="star"
              icon-half="star_half"
            />
          </div>
          
          <!-- Textarea Box -->
          <div class="feedback-input">
            <q-input
              v-model="feedback"
              label="Your Feedback and Suggestions"
              placeholder="Type your feedback and suggestions here..."
              outlined
              dense
              type="textarea"
              rows="5"
              class="modern-textarea"
            />
          </div>
        </div>
        
        <!-- Submit Button -->
        <div class="button-container">
          <q-btn
            label="Submit"
            color="primary"
            @click="submitFeedback"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      rating: 0,
      feedback: '',
    }
  },
  
  methods: {
    submitFeedback() {
      // Submit feedback logic here
      console.log('Rating:', this.rating)
      console.log('Feedback:', this.feedback)
    }
  }
}
</script>

<style scoped>
/* Import Koh Santepheap font */
@import url('https://fonts.googleapis.com/css2?family=Koulen&display=swap');

/* Apply font globally */
* {
  font-family: 'Koulen', display;
}

.cover {
  background: #ffffff;
  width: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-image: linear-gradient(to bottom, #f7f7f7, #ffffff);
}

.header-space {
  width: 100%;
  height: 60px; /* Simulating header space */
  background: #ffffff;
}

.container {
  width: 50%;
  margin: 0 auto;
  padding: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
  background-color: #ffffff;
}

.content-wrapper {
  width: 100%;
}

.main-box {
  padding: 20px;
  text-align: center;
  background-color: #f7f7f7;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.feedback-header {
  margin-bottom: 20px;
}

h2 {
  font-size: 24px;
  font-weight: 400;
  color: #000;
  margin: 0;
  margin-bottom: 8px;
  letter-spacing: 0.5px;
}

p {
  font-size: 16px;
  font-weight: 400;
  color: #666;
  margin: 0;
  margin-bottom: 20px;
  letter-spacing: 0.3px;
}

.rating-input {
  margin-bottom: 20px;
}

.feedback-input {
  margin-bottom: 20px;
}

.modern-textarea {
  border-radius: 10px;
  padding: 10px;
  font-size: 16px;
  font-weight: 400;
  color: #666;
  background-color: #ffffff;
  border: 1px solid #ddd;
}

.modern-textarea .q-field__label {
  font-size: 16px;
  font-weight: 400;
  color: #666;
}

.modern-textarea .q-field__control {
  padding: 10px;
}

.button-container {
  display: flex;
  justify-content: center;
}

/* Making the component responsive */
@media (max-width: 768px) {
  .container {
    width: 80%;
  }
}
/* Import Koh Santepheap font */
@import url('https://fonts.googleapis.com/css2?family=Koh+Santepheap&display=swap');

/* Apply font globally */
* {
  font-family: 'Koh Santepheap', display;
}
</style>