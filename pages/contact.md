---
title: "Contact"
permalink: "/contact/"
layout: page
---
<link rel="stylesheet" href="../assets/css/form.css">
<form
  action="https://formspree.io/f/xqalqdpa"
  class="fs-form"
  target="_top"
  method="POST"
>
  <div class="fs-field">
    <label class="fs-label" for="name">Name</label>
    <input class="fs-input" id="name" name="name" required />
  </div>
  <div class="fs-field">
    <label class="fs-label" for="email">Email</label>
    <input class="fs-input" id="email" name="email" required />
  </div>
  <div class="fs-field">
    <label class="fs-label" for="message">Message</label>
    <textarea
      class="fs-textarea"
      id="message"
      name="message"
      required
    ></textarea>
  </div>
  <div class="fs-button-group">
    <button class="fs-button" type="submit">Submit</button>
  </div>
</form>
