<template>
  <div>
      <div class="field has-addons is-fullwidth">
        <p class="control has-icons-left">
          <span class="icon is-small is-left">
            <i class="fas fa-envelope"></i>
          </span>
        </p>
        <div class="control">
          <button type="button" class="button is-primary" @click="formAction">
            {{ $siteConfig.survey.btnText || 'Plant money Seeds' }}
          </button>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: ''
    }
  },
  computed: {
    formAction() {
      if (this.$siteConfig.survey.on) {
        return this.$siteConfig.survey.google.link
      }
      return this.$siteConfig.survey.custom.link
    }
  }
}
</script>
