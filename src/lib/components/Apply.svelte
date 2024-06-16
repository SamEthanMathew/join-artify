<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
  
    let fullName = '';
    let email = '';
    let phoneNumber = '';
    let school = '';
    let position = '';
    let reason = '';
    let volunteerReason = '';
    let webDevReason = '';
  
    async function handleSubmit(event) {
      event.preventDefault();
  
      const formData = {
        fullName,
        email,
        phoneNumber,
        school,
        position,
        reason,
        volunteerReason,
        webDevReason
      };
  
      try {
        const response = await fetch('http://localhost:3000/submit-form', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify(formData)
        });
  
        if (response.ok) {
          console.log('Form submitted successfully');
          // Optionally, you can dispatch an event to notify the parent component
          dispatch('formSubmitted');
        } else {
          console.error('Failed to submit form');
        }
      } catch (error) {
        console.error('Error submitting form:', error);
      }
  
      // Reset form fields
      fullName = '';
      email = '';
      phoneNumber = '';
      school = '';
      position = '';
      reason = '';
      volunteerReason = '';
      webDevReason = '';
    }
  </script>
  
  <style>
    .form-group {
      margin-bottom: 20px;
    }
  
    .form-group label {
      display: inline-block;
      width: 120px;
      font-weight: bold;
    }
  
    .form-group input[type="text"],
    .form-group input[type="email"],
    .form-group input[type="tel"],
    .form-group textarea {
      width: 300px;
      padding: 5px;
    }
  
    .long-question {
      width: 100%;
    }
  </style>
  
  <form on:submit={handleSubmit}>
    <div class="form-group">
      <label>Full Name:</label>
      <input type="text" bind:value={fullName} required />
    </div>
  
    <div class="form-group">
      <label>Email Address:</label>
      <input type="email" bind:value={email} required />
    </div>
  
    <div class="form-group">
      <label>Phone Number:</label>
      <input type="tel" bind:value={phoneNumber} required />
    </div>
  
    <div class="form-group">
      <label>School:</label>
      <input type="text" bind:value={school} required />
    </div>
  
    <div class="form-group">
      <fieldset>
        <legend>Select Position:</legend>
        <label>
          <input type="radio" bind:group={position} value="Volunteer" required />
          Volunteer
        </label>
        <label>
          <input type="radio" bind:group={position} value="Web Dev" required />
          Web Dev
        </label>
      </fieldset>
    </div>
  
    <div class="form-group">
      <label class="long-question">Why do you want to join Artify?</label>
      <textarea bind:value={reason} class="long-question" required></textarea>
    </div>
  
    {#if position === 'Volunteer'}
      <div class="form-group">
        <label class="long-question">Why do you want to become a volunteer?</label>
        <textarea bind:value={volunteerReason} class="long-question" required></textarea>
      </div>
    {/if}
  
    {#if position === 'Web Dev'}
      <div class="form-group">
        <label class="long-question">Why do you want to become a web dev?</label>
        <textarea bind:value={webDevReason} class="long-question" required></textarea>
      </div>
    {/if}
  
    <button type="submit">Submit</button>
  </form>
  