<template>
  <form name="contact" @submit="onSubmit" class="add-form">
    <!-- Name -->
    <div class="field">
      <label class="label is-medium">Name</label>
      <div class="control has-icons-left">
        <input type="hidden" name="form-name" value="ask-question" />
        <input class="input is-medium" v-model="name" name="name" type="text" placeholder="Lerato Zulu" />
        <span class="icon is-small is-left">
          <font-awesome-icon icon="user" />
        </span>
      </div>
    </div>
    <!-- Email -->
    <div class="field">
      <label class="label is-medium">Email</label>
      <div class="control has-icons-left">
        <input
          class="input is-medium"
          type="email"
          v-model="email"
          name="email"
          placeholder="you@email.com"
        />
        <span class="icon is-small is-left">
          <font-awesome-icon icon="envelope" />
        </span>
      </div>
    </div>
    <!-- Subject -->
    <div class="field">
      <label class="label is-medium">Subject</label>
      <div class="control has-icons-left">
        <input
          class="input is-medium"
          type="text"
          v-model="subject"
          name="subject"
          placeholder="Brief Summary"
        />
        <span class="icon is-small is-left">
          <font-awesome-icon icon="briefcase" />
        </span>
      </div>
    </div>
    <!-- Message -->
    <div class="field">
      <label class="label is-medium">Message</label>
      <div class="control">
        <textarea
          class="textarea"
          placeholder="Detailed description of your comment, request, etc"
          rows="8"
          v-model="message"
          name="message"
        ></textarea>
      </div>
    </div>
    <div class="control">
      <button type="submit" class="button is-primary">
        Contact Us
      </button>
    </div>
  </form>
</template>

<script>
 
 import emailjs from 'emailjs-com'

 export default {
  name: 'ContactUs',
  data() {
    return {
      name: '',
      email: '',
      message: ''
    }
  },
  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm('service_3hnq726', 'template_k9kgxm4', e.target,
        '2jHUhJntZZjX3-FsC', {
          name: this.name,
          subject: this.subject,
          email: this.email,
          message: this.message
        })

      } catch(error) {
          console.log({error})
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  }
}

</script>
