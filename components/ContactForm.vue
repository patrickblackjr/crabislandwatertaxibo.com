<template>
  <section id="contact-form">
    <form
      name="contact"
      action="/thank-you"
      method="POST"
      netlify
      data-netlify-honeypot="bot-field"
    >
      <input type="hidden" name="contact" value="contact" />
      <div class="form-group">
        <input
          id="name"
          name="name"
          type="text"
          class="form-control"
          required
          placeholder="Enter name"
        />
        <label for="name">First and last name</label>
      </div>
      <div class="form-group">
        <input
          id="email"
          name="email"
          type="email"
          class="form-control"
          required
          placeholder="Enter email"
        />
        <label for="email">Email address</label>
      </div>
      <div class="form-group">
        <input
          id="phone"
          name="phone"
          type="phone"
          class="form-control"
          required
          placeholder="Enter phone"
        />
        <label for="phone">Phone number</label>
      </div>
      <div class="form-group-out">
        <label class="sr-only" for="message">Message</label>
        <textarea
          id="message"
          name="message"
          class="form-control"
          placeholder="Message"
          rows="4"
        ></textarea>
      </div>
      <input
        class="form-button btn btn-primary mt-3"
        type="submit"
        value="Submit"
      />
    </form>
  </section>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style>
.form-group {
  position: relative;
  margin-bottom: 1rem;
}

.form-group > input,
.form-group > label {
  height: 3.125rem;
  padding: 0.75rem;
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
  border-radius: 0.25rem;
  transition: all 0.1s ease-in-out;
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
  padding-bottom: 0.25rem;
}

.form-group input:not(:placeholder-shown) ~ label {
  padding-top: 0.25rem;
  padding-bottom: 0.25rem;
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
