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

<html lang="en">
<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname">

  <input type="radio" id="male" name="gender" value="male">
  <label for="male">Male</label><br>
  <input type="radio" id="female" name="gender" value="female">
  <label for="female">Female</label><br>
  <input type="radio" id="other" name="gender" value="other">
  <label for="other">Other</label>

  <input type="submit" value="Submit">

</form>
</html>
