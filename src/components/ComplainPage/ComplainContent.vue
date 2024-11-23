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
            <h2>Your Feedback !!!</h2>
            <p>Give us your feedback on our services.</p>
          </div>
          
          <!-- Textarea Box -->
          <div class="feedback-input">
            <textarea
              placeholder="Typing Here..."
              class="feedback-textarea"
            ></textarea>
          </div>
        </div>
        
        <!-- Submit Button -->
        <div class="button-container">
          <button class="submit-button">Submit</button>
        </div>
      </div>
    </div>
  </div>
</template>

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
}

.header-space {
  width: 100%;
  height: 60px; /* Simulating header space */
  background: #ffffff;
}

.container {
  width: 100%;
  max-width: 1200px; /* Increased max-width */
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 40px;
}

.content-wrapper {
  width: 100%;
}

.main-box {
  background-color: #f5f5f5;
  border-radius: 8px;
  padding: 30px; /* Increased padding */
  margin-bottom: 20px;
}

.feedback-header {
  background-color: #e6e6e6;
  border-radius: 8px;
  padding: 20px; /* Increased padding */
  text-align: center;
  margin-bottom: 25px; /* Increased margin */
}

h2 {
  font-size: 32px; /* Increased font size */
  font-weight: 400; /* Adjusted for Koulen font */
  color: #000;
  margin: 0;
  margin-bottom: 8px;
  letter-spacing: 0.5px;
}

p {
  font-size: 16px; /* Increased font size */
  color: #666;
  margin: 0;
  letter-spacing: 0.3px;
}

.feedback-input {
  background-color: #e6e6e6;
  border-radius: 8px;
  padding: 20px; /* Increased padding */
  margin: 0 auto;
  width: 90%;
}

.feedback-textarea {
  width: 100%;
  min-height: 120px; /* Increased height */
  padding: 0;
  border: none;
  font-size: 16px; /* Increased font size */
  resize: none;
  background-color: transparent;
  color: #666;
  letter-spacing: 0.3px;
}

.feedback-textarea::placeholder {
  color: #666;
  font-family: 'Koulen', display;
}

.button-container {
  display: flex;
  justify-content: flex-end;
  padding-right: 30px; /* Increased padding */
}

.submit-button {
  background-color: #e6e6e6;
  color: #000;
  border: none;
  border-radius: 8px;
  padding: 10px 30px; /* Increased padding */
  font-size: 16px; /* Increased font size */
  cursor: pointer;
  transition: background-color 0.2s;
  letter-spacing: 0.3px;
}

.submit-button:hover {
  background-color: #d9d9d9;
}

/* Making the component responsive */
@media (max-width: 1200px) {
  .container {
    padding: 0 20px;
  }
}

@media (max-width: 768px) {
  .main-box {
    padding: 20px;
  }
  
  .feedback-input {
    width: 95%;
  }
  
  h2 {
    font-size: 28px;
  }
  
  p, .feedback-textarea, .submit-button {
    font-size: 14px;
  }
}
</style>