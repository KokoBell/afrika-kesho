<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About Us"
      subtitle=""
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>The Context</h3>
          <p>
            A majority of South Africa’s population is living near or below the poverty line.
            This is due a myriad of reasons, and primarily the country’s colonial history and
            present and is inherently systemic to the extent that public education does not
            provide for financial literacy and does not encourage self-sufficiency. Basic skills
            such as budgeting and personal tax management are not readily accessible to every
            learner in the traditional public schooling system, let alone more complex ideas like
            investments and entrepreneurship. This intentional withholding of information is
            exacerbating the issue of the widening wealth gap between the colonial minority and
            native majority, in South Africa and the rest of Africa.
          </p>

          <h3>The Aim</h3>
          <p>
            Our aim as Afrika Kesho is the re-education of African communities in how they manage their
            personal and community finances. We envision African communities that are self-sufficient and
            both socially and economically independent. The self-sufficiency will come from us shifting
            our focus and historical positioning from being primary sector employees to primary, secondary
            and tertiary sector business owners. This would include having businesses that not only mine raw
            materials, but also refine and make products from them, and others that not only grow crops and
            livestock, but extract raw materials from them and produce clothing, refined foods and other
            products. This will circulate money within African economies and ground our roots as an
            independent continent.
            </p>

            <p>
            The minds that are most malleable are young minds, but in the same vein it takes a level of
            understanding to comprehend and apply the subject matter that we will be discussing.
            Such a group of young but capable minds can be found in the age group of 19 to 35 year olds.
            As such, we’ll be targeting African people in the tertiary education spaces – these are the
            people who will be leading the country in future and they should find themselves applying
            different methodologies than that of our current elders – and they should be more intentional
            in their pursuit of African unity and collective wealth. However, all of that begins with the
            re-education of ourselves as individuals and the re-education of our future leaders.
          </p>
        </div>


      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>
