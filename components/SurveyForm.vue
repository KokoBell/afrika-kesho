<template>
  <div>
      <div class="field has-addons is-fullwidth">
        <p class="control has-icons-left">
          <span class="icon is-small is-left">
            <i class="fas fa-envelope"></i>
          </span>
        </p>
        <div class="control">
          <a href="javascript:this.$siteConfig.survey.link" target="_blank" rel="noopener noreferrer">
            <button type="button" class="button is-primary">
              {{ $siteConfig.survey.btnText || 'Plant money Seeds' }}
            </button>
          </a>
        </div>
      </div>
  </div>
</template>

<script>
</script>
