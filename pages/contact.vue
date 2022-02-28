<template>
  <div id="contact-page" class="page-wrapper contact-page content-page">
    <site-hero
      title="Contact Us"
      subtitle="Example Contact Page"
      image="/uploads/contact-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Hello!
              </p>
              <p class="subtitle">
                What can I do for you?
              </p>
              <figure class="image is-1by1 ">
                <opti-image
                  :src="require('~/assets/uploads/contact-person.jpg').src"
                  :srcset="
                    require('~/assets/uploads/contact-person.jpg').srcSet
                  "
                />
              </figure>
              <br />
              <div class="content">
                <p>
                  <strong>
                    If you want to send us some feedback,request a collaboration,
                    or submit an article, contact us via this form.
                  </strong>
                </p>

                <p>
                Follow and engage us on all our social media:
                <ul>
                  <li>
                    <a href="https://twitter.com/afrikakesho">
                      <font-awesome-icon icon="twitter" />
                    </a>
                  </li>

                  <li>
                    <a href="https://www.facebook.com/OfficialAfrikaKesho">
                      <font-awesome-icon icon="facebook" />
                    </a>
                  </li>

                  <li>
                    <a href="https://www.instagram.com/afrikakesho/">
                      <font-awesome-icon icon="instagram" />
                    </a>
                  </li>

                </ul>
                </p>
              </div>
            </article>
          </div>
          <div class="tile is-parent is-8">
            <article class="tile is-child box">
              <contact-form />
            </article>
          </div>
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import ContactForm from '~/components/ContactForm'
export default {
  head() {
    return {
      title: `Contact | ${this.$siteConfig.siteName}`
    }
  },
  components: { ContactForm }
}
</script>
