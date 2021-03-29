---
layout: layouts/post.njk
title: Contact Us
templateClass: tmpl-post
eleventyNavigation:
  key: About Me
  order: 3
---

Contact Us Now!
At contactus@realMail.com or phone us at 07123 456789

Or we can contact you:

<form name="contact" method="POST" data-netlify="true">
  <p>
    <label>Your Name: <input type="text" name="name" /></label>   
  </p>
  <p>
    <label>Your Email: <input type="email" name="email" /></label>
  </p>
  <p>
    <label>Your Role: <select name="role[]" multiple>
      <option value="leader">Leader</option>
      <option value="follower">Follower</option>
    </select></label>
  </p>
  <p>
    <label>Message: <textarea name="message"></textarea></label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>

document.querySelector("form").addEventListener("submit", handleSubmit);

const handleSubmit = (e) => {
  e.preventDefault()
  let myForm = document.getElementById('pizzaOrder');
  let formData = new FormData(myForm)
  fetch('/', {
    method: 'POST',
    headers: { "Content-Type": "application/x-www-form-urlencoded" },
    body: new URLSearchParams(formData).toString()
  }).then(() => console.log('Form successfully submitted')).catch((error) =>
    alert(error))
}
