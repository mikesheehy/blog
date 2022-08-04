---
author: Mike
category: codeky
---

An item that frustrates Code Kentucky students is the JavaScript requirement, specifically the contact form. We ask for the form to have some form of validation, and then we want the submit button to pass an input field.

```
<form>
  <div>
    <input type="text" id="name" placeholder='First Name' required>
  </div>
  <div>
    <input type="email" id="email" placeholder="Email Address" required>
  </div>
  <div>
    <button onclick="concat()">Contact for Booking!!</button>
  </div>
</form>

<script>
    function concat() {
    var nameInput = document.getElementById('name').value;
  var confirm = 'Thank you, ' + nameInput + '!';
  alert(confirm);
}
</script>
```

You can check out the code in action here:

<form>
  <div>
    <input type="text" id="name" placeholder='First Name' required>
  </div>
  <div>
    <input type="email" id="email" placeholder="Email Address" required>
  </div>
  <div>
    <button onclick="concat()">Contact for Booking!!</button>
  </div>
</form>

<script>
    function concat() {
    var nameInput = document.getElementById('name').value;
  var confirm = 'Thank you, ' + nameInput + '!';
  alert(confirm);
}
</script>


So, is that all you need to do? Nope, Code KY also requires you to add validation to the form. A lot of students think that adding 'required' to the input form is enough. It doesn't work. Leave the fields blank in the form above and you'll see that the validation messages don't appear until after you receive your thank-you message, which is way too late. Instead, you'll need to write the validation into your javascript.

```
<form>
  <div>
    <input type="text" id="name2" placeholder="First Name">
  </div>
  <div>
    <input type="email" id="email2" placeholder="Email Address">
  </div>
  <div>
    <button onclick="concat2()">Contact for Booking!!</button>
  </div>
</form>

<script>
    function concat2() {
      let nameInput = document.getElementById('name2').value;
      if (nameInput == "") {
        alert("Name must be filled out");
        return false;
      }
      else{
        var confirm = 'Thank you, ' + nameInput + '!';
        alert(confirm);
      }
}
</script>
```

<form>
  <div>
    <input type="text" id="name2" placeholder="First Name">
  </div>
  <div>
    <input type="email" id="email2" placeholder="Email Address">
  </div>
  <div>
    <button onclick="concat2()">Contact for Booking!!</button>
  </div>
</form>

<script>
    function concat2() {
      let nameInput = document.getElementById('name2').value;
      if (nameInput == "") {
        alert("Name must be filled out");
        return false;
      }
      else{
        var confirm = 'Thank you, ' + nameInput + '!';
        alert(confirm);
      }
}
</script>


And there you have it, a contact form that validates the first name and sends back a message using the input. From the if/else statement to the use of let, var, and getElementById, this could be difficult for a student to grasp 1-2 weeks after learning Javascript. If you are experiencing issues, let me know.


