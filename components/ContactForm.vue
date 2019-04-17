<template>
  <section id="contact-form">
    <form name="contact" action="/thank-you" method="POST" netlify data-netlify-honeypot="bot-field">
      <input type="hidden" name="contact" value="contact">
      <div class="form-group">
        <input name="name" type="text" id="name" class="form-control" required placeholder="Enter name">
        <label for="name">First and last name</label>
      </div>
      <div class="form-group">
        <input name="email" type="email" id="email" class="form-control" required placeholder="Enter email">
        <label for="email">Email address</label>
      </div>
      <div class="form-group">
        <input name="phone" type="phone" id="phone" class="form-control" required placeholder="Enter phone">
        <label for="phone">Phone number</label>
      </div>
      <div class="form-group-out">
        <label class="sr-only" for="message">Message</label>
        <textarea name="message" class="form-control" id="message" placeholder="Message" rows="4"></textarea>
      </div>
      <input class="form-button btn btn-primary mt-3" type="submit" value="Submit"/>
    </form>
  </section>
</template>

<script>

export default {
  data() {
    return {

    }
  }
}

</script>

<style>
.form-group {
  position: relative;
  margin-bottom: 1rem;
}

.form-group > input,
.form-group > label {
  height: 3.125rem;
  padding: .75rem;
}

.form-group > label {
  position: absolute;
  top: 0;
  left: 0;
  display: block;
  width: 100%;
  margin-bottom: 0; /* Override default `<label>` margin */
  line-height: 1.5;
  color: #495057;
  pointer-events: none;
  cursor: text; /* Match the input under the label */
  border: 1px solid transparent;
  border-radius: .25rem;
  transition: all .1s ease-in-out;
}

.form-group input::-webkit-input-placeholder {
  color: transparent;
}

.form-group input:-ms-input-placeholder {
  color: transparent;
}

.form-group input::-ms-input-placeholder {
  color: transparent;
}

.form-group input::-moz-placeholder {
  color: transparent;
}

.form-group input::placeholder {
  color: transparent;
}

.form-group input:not(:placeholder-shown) {
  padding-top: 1.25rem;
  padding-bottom: .25rem;
}

.form-group input:not(:placeholder-shown) ~ label {
  padding-top: .25rem;
  padding-bottom: .25rem;
  font-size: 12px;
  color: #777;
}
/* Fallback for Edge
-------------------------------------------------- */
@supports (-ms-ime-align: auto) {
  .form-group > label {
    display: none;
  }
  .form-group input::-ms-input-placeholder {
    color: #777;
  }
}

/* Fallback for IE
-------------------------------------------------- */
@media all and (-ms-high-contrast: none), (-ms-high-contrast: active) {
  .form-group > label {
    display: none;
  }
  .form-group input:-ms-input-placeholder {
    color: #777;
  }
}
</style>
