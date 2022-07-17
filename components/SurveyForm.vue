<template>
  <div>
      <div class="field has-addons is-fullwidth">
        <p class="control has-icons-left">
          <span class="icon is-small is-left">
            <i class="fas fa-envelope"></i>
          </span>
        </p>
        <div class="control">
          <a href="$siteConfig.survey.link" _target="blank">
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
