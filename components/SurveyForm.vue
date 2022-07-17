<template>
  <div>
      <div class="field has-addons is-fullwidth">
        <p class="control has-icons-left">
          <span class="icon is-small is-left">
            <i class="fas fa-envelope"></i>
          </span>
        </p>
        <div class="control">
          <a href="https://forms.gle/wigPpZHCAuBwcwyt5" target="_blank" rel="noopener noreferrer" style="text-decoration:none;">
            <button type="button" class="button is-primary survey-button">
              {{ $siteConfig.survey.btnText || 'Plant money Seeds' }}
            </button>
          </a>
        </div>
      </div>
  </div>
</template>

<style lang="scss" scoped>

.survey-button {
  width: 100%;
  padding: 0.2rem;
  border-radius: 8px;
}

</style>
