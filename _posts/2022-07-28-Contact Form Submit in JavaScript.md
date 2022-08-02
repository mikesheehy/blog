---
author: Mike
category: codeky
---

An item that frustrates Code Kentucky students is the JavaScript requirement, specifically the contact form. We ask for the form to have some form of validation, and then we want the submit button to pass an input field.

<form>
  <div>
    <input type="text" id="name" placeholder='First Name' required>
  </div>
  <div>
    <input type="email" id="email" placeholder="Email Address" required>
  </div>
  <div>
    <button id="contactButton" onclick="concat()">Contact for Booking!!</button>
  </div>
</form>

<script>
    function concat() {
    var nameInput = document.getElementById('name').value;
  var confirm = 'Thank you, ' + nameInput + '!';
  alert(confirm);
}
</script>