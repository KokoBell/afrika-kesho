<template>
  <div id="contact-page" class="page-wrapper contact-page content-page">
    <site-hero
      title="Contact Us"
      subtitle=""
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
                    If you want to send us some feedback, request a collaboration,
                     or submit an article, get in touch using the contact form.
                  </strong>
                </p>

                <div class="social-media-grid">
                  <ul>
                        <li><a href="https://www.facebook.com/OfficialAfrikaKesho"><span></span></a></li>
                        <li><a href="https://twitter.com/afrikakesho"><span></span></a></li>
                        <li><a href="https://www.instagram.com/afrikakesho/"><span></span></a></li>
                  </ul>
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

<style scoped>

@import url('https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css');

body {
    margin: 0;
    padding: 0;
}

ul {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
}

ul li {
    position: relative;
    list-style: none;
    margin: 0 2px;
}

ul li::before {
    content: '';
    position: absolute;
    left: 0;
    bottom: -4px;
    width: 40px;
    height: 8px;
    background: #000;
    border-radius: 50%;
    transition: 0.5s;
    opacity: 0;
    filter: blur(2px);
    transform: scale(0.8);
}

ul li:hover::before {
    transition-delay: 0.2s;
    opacity: 0.2;
    transform: scale(1);
}

ul li a {
    width: 40px;
    height: 40px;
    display: block;
    transition: 0.5s;
}

ul li:hover a {
    transform: translateY(-10px);
}

ul li a span  {
    width: 100%;
    height: 100%;
}

ul li a span::before {
    font-family: fontAwesome;
    text-align: center;
    line-height: 40px;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #fff;
    color: #262626;
    transform-origin: top;
    transition: transform 0.5s;
}

ul li:hover a span::before {
    transform: rotateX(90deg) translateY(-50%);
}

ul li a span::after {
    font-family: fontAwesome;
    text-align: center;
    line-height: 40px;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    /* background: #fff;
    color: #262626; */
    transform-origin: bottom;
    transition: transform 0.5s;
    transform: rotateX(90deg) translateY(50%);
}

ul li:hover a span::after {
    transform: rotateX(0deg) translateY(0);
}

ul li:nth-child(1) a span::before,
ul li:nth-child(1) a span::after {
    content: '\f09a';
}

ul li:nth-child(2) a span::before,
ul li:nth-child(2) a span::after {
    content: '\f099';
}

ul li:nth-child(3) a span::before,
ul li:nth-child(3) a span::after {
    content: '\f16d';
}
ul li:nth-child(1) a span::after {
    background: #3b5999;
    color: #fff;
}
ul li:nth-child(2) a span::after {
    background: #55acce;
    color: #fff;
}
ul li:nth-child(3) a span::after {
    background: radial-gradient(circle farthest-corner at 35% 90%, #fec564, transparent 50%), radial-gradient(circle farthest-corner at 0 140%, #fec564, transparent 50%), radial-gradient(ellipse farthest-corner at 0 -25%, #5258cf, transparent 50%), radial-gradient(ellipse farthest-corner at 20% -50%, #5258cf, transparent 50%), radial-gradient(ellipse farthest-corner at 100% 0, #893dc2, transparent 50%), radial-gradient(ellipse farthest-corner at 60% -20%, #893dc2, transparent 50%), radial-gradient(ellipse farthest-corner at 100% 100%, #d9317a, transparent), linear-gradient(#6559ca, #bc318f 30%, #e33f5f 50%, #f77638 70%, #fec66d 100%);
    color: #fff;
}

</style>
