<svelte:head>
	<title>Contact | Send email</title>
</svelte:head>


<script>
  import { createEventDispatcher } from "svelte";
  import Button from "../components/Button.svelte";
  import TextInput from "../components/TextInput.svelte";
  import { isEmpty, isValidEmail } from "../helpers/validation.js";

  export let id = null;

  let fullname = "";
  let email = "";
  let description = "";
  let name = "";
  let placeholder = "";
  let rows = "";

  const dispatch = createEventDispatcher();

  $: fullnameValid = !isEmpty(fullname);
  $: descriptionValid = !isEmpty(description);
  $: emailValid = isValidEmail(email);

  $: formIsValid = fullnameValid && descriptionValid && emailValid;
</script>

<style>
  .container {
    border-radius: 5px;
    background-color: #f2f2f2;
    padding: 20px;
  }
</style>

<h1 style="color: white;">Contact me</h1>

<div class="container">
  <form id='contact-form' method="post" action="https://briskforms.com/go/eacf0e72a032519cba8ae9ce8d390439">
    
    <TextInput
      label="Full Name"
      name="fullname" 
      on:input={event => (fullname = event.target.value)}  
      value={fullname} valid={fullnameValid}   
      validityMessage="Please enter your full name." 
      type="text" 
      id="fname" 
      placeholder="Your full name.."
    />
    
    <TextInput
      name="email"
      id="email"
      label="E-Mail"
      type="email"
      valid={emailValid}
      validityMessage="Please enter a valid email address."
      value={email}
      on:input={event => (email = event.target.value)}
      placeholder="Your email adress.."
    />

    <TextInput
      name="message"
      id="description"
      label="Description"
      controlType="textarea"
      valid={descriptionValid}
      validityMessage="Please enter a valid message."
      bind:value={description} 
      type="textarea"
      placeholder="Write me something.."
      rows="10"
    />
      
      <Button type="submit" value="Submit" disabled={!formIsValid}>Trimite</Button>

  </form>
</div>
