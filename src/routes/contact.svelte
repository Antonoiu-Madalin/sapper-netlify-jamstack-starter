<svelte:head>
	<title>Contact</title>
</svelte:head>


<style>
  input[type="text"],
  textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    margin-top: 6px;
    margin-bottom: 16px;
    resize: vertical;
  }

  input[type="email"],
  textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    margin-top: 6px;
    margin-bottom: 16px;
    resize: vertical;
  }

  input[type="submit"] {
    background-color: #4caf50;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }

  input[type="submit"]:hover {
    background-color: #45a049;
  }

  .container {
    border-radius: 5px;
    background-color: #f2f2f2;
    padding: 20px;
  }
</style>


<h1 style="color: white;">Contact me</h1>

<div class="container">
  <form method="post" action="https://briskforms.com/go/eacf0e72a032519cba8ae9ce8d390439">

    <label for="fname">Full Name</label>
    <input type="text" id="fname" name="fullname" placeholder="Your full name..">

		<label for="lname">Email Adress</label>
    <input type="email" id="lname" name="lastname" placeholder="Your email..">

    <label for="subject">Subject</label>
    <textarea id="subject" name="subject" placeholder="Write something.." style="height:200px"></textarea>

    <input type="submit" value="Submit">
  </form>
</div>