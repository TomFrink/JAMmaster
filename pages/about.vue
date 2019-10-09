<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About JAMmaster"
      subtitle="In case you're wondering why..."
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>#Goals</h3>
          <p>
            <strong>
              Goal here is to learn & help others learn.
            </strong>
          </p>
          <p>
            Thomas Edison once remarked "I haven't failed. I've just found
            10,000 ways which won't work." I've found a number of ways in which
            'it' doesn't work. My goal is to reach 10,000.
          </p>

          <h3>Welcome What Comes</h3>
          <p>
            The stoics had a phrase "Amor fati" which loosely translates to
            "Love of Fate". This is the best way to frame what transpires in
            life. Because whatever happened cannot be altered. The only thing
            one can do is alter the actions you take today.
          </p>
          <quote-card />
          <h3>Why the JAMstack</h3>
          <p>
            Look.At the end of the day, no one really cares how you cook
            something. All that matters is how it tastes. There are a lot of
            different ways to build apps, sites, etc. What matters most is that
            they get built, not how they get built.
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
