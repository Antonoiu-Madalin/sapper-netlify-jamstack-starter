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

  let sendMessage = false;

  const dispatch = createEventDispatcher();

  $: fullnameValid = !isEmpty(fullname);
  $: descriptionValid = !isEmpty(description);
  $: emailValid = isValidEmail(email);

  $: formIsValid = fullnameValid && descriptionValid && emailValid;
</script>

<style>
  @import url("https://use.fontawesome.com/releases/v5.1.0/css/all.css");

  .container {
    border-radius: 5px;
    background-color: #f2f2f2;
    padding: 20px;
  }
  label {
    display: inline-block;
    margin: 0 0 -1px;
    padding: 15px 25px;
    font-weight: 600;
    text-align: center;
    color: #abc;
    border: 1px solid transparent;
  }

  label:before {
    font-family: fontawesome;
    font-weight: normal;
    margin-right: 10px;
  }

  label[for*="2"]:before {
    font-family: "Font Awesome 5 Brands";
    content: "\f198";
  }

  a label {
    cursor: pointer;
  }

  label {
    cursor: pointer;
  }

  li {
    list-style-type: none;
    padding: 0;
    margin: 0;
    -webkit-touch-callout: none; /* iOS Safari */
    -webkit-user-select: none; /* Safari */
    -khtml-user-select: none; /* Konqueror HTML */
    -moz-user-select: none; /* Firefox */
    -ms-user-select: none; /* Internet Explorer/Edge */
    user-select: none; /* Non-prefixed version, currently
                                      supported by Chrome and Opera */
    -webkit-user-select: none;
    -khtml-user-select: none;
    -moz-user-select: none;
    -o-user-select: none;
    user-select: none;
  }

  a{
      -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -o-user-select: none;
  user-select: none;
  }
</style>

<h1 style="color: white; ">Contact me</h1>
<hr>




    <li>
      <a href="https://join.slack.com/t/hireadevio/shared_invite/enQtNzE5ODg0Mjg0OTQ5LTQ1MjljY2VhMGYzZDg1ZDdhMjg1ZThhM2M2OTYyNTI1NDg1MmQwOTdjMWM3YTk5YzNhYTBiOGVjNzE0MzRkOTE">
        <label for="tab2"><span style="color: #228B22">Join</span> my Slack channel</label>
      </a>
    </li>

    <li>
      <label><i class="fab fa-twitter" style="color: #1da1f2;"> &nbsp; </i> Follow on Tweeter <span style="color: #20B2AA"></span></label>
    </li>

    <li>
      <label on:click={() => {sendMessage = !sendMessage} }><i class="fas fa-envelope" style="color: white;"> &nbsp; </i> Send me a <span style="color: #20B2AA">message</span></label>
  
    </li>




{#if sendMessage} 

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
      
      <Button type="submit" value="Submit" disabled={!formIsValid}>Send</Button>

  </form>
  
</div>
{/if}
