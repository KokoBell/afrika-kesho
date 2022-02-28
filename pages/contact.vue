<template>
  <head>
    <style>
      .btn {
        clear:both;
        white-space:nowrap;
        font-size:.8em;
        display:inline-block;
        border-radius:5px;
        box-shadow: 0 1px 5px 0 rgba(0, 0, 0, 0.35);
        margin:2px;
        -webkit-transition:all .5s;
        -moz-transition:all .5s;
        transition:all .5s;
        overflow:hidden
      }

      .btn:hover {
        box-shadow: 0 5px 15px 0 rgba(0, 0, 0, 0.45);
      }

      .btn:focus {
        box-shadow: 0 3px 10px 0 rgba(0, 0, 0, 0.4);
      }

      .btn > span,.btn-icon > i {
        float:left;
        padding:13px;
        -webkit-transition:all .5s;
        -moz-transition:all .5s;
        transition:all .5s;
        line-height:1em
      }

      .btn > span {
        padding:14px 18px 16px;
        white-space:nowrap;
        color:#FFF;
        background:#b8b8b8
      }

      .btn:focus > span {
        background:#9a9a9a
      }

      .btn-icon > i {
        border-radius:5px 0 0 5px;
        position:relative;
        width:13px;
        text-align:center;
        font-size:1.25em;
        color:#fff;
        background:#212121
      }

      .btn-icon > i:after {
        content:"";
        border:8px solid;
        border-color:transparent transparent transparent #222;
        position:absolute;
        top:13px;
        right:-15px
      }

      .btn-icon:hover > i,.btn-icon:focus > i {
        color:#FFF
      }

      .btn-icon > span {
        border-radius:0 5px 5px 0
      }

      /*Facebook*/
      .btn-facebook:hover > i,.btn-facebook:focus > i {
        color:#3b5998
      }

      .btn-facebook > span {
        background:#3b5998
      }

      /*Twitter*/
      .btn-twitter:hover > i,.btn-twitter:focus > i {
        color:#55acee
      }

      .btn-twitter > span {
        background:#55acee
      }

      /*Pinterest*/
      .btn-instagram:hover > i,.btn-pinterest:focus > i {
        color:#cb2028
      }

      .btn-instagram > span {
        background:#cb2028
      }

    </style>
  </head>
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
                    <a href="">
                      <a class="btn btn-icon btn-twitter" href="https://twitter.com/afrikakesho" target="_blank"><i class="fa fa-twitter"></i><span>Twitter</span></a>
                    </a>
                  </li>

                  <li>
                    <a class="btn btn-icon btn-facebook" href="https://www.facebook.com/OfficialAfrikaKesho" target="_blank"><i class="fa fa-facebook"></i><span>Facebook</span></a>
                  </li>

                  <li>
                    <a class="btn btn-icon btn-instagram" href="https://www.instagram.com/afrikakesho/" target="_blank"><i class="fa fa-instagram"></i><span>Instagram</span></a>
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
