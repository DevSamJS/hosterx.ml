<template>
  <div class="learnmoreSection fullSizeSection" :id="id">
    <h3>{{title}}:-<a href="#" style="float: right;color: aliceblue; text-decoration: none">X</a></h3>
    <hr>
    <div class="content">
      <featureCard
        :key="featureCard.src"
        v-for="featureCard in featureCards"
        :src="featureCard.src"
        :title="featureCard.cardTitle"
        :discription="featureCard.discription"
      />
    </div>
  </div>
</template>

<script>
import featureCard from './cards/featureCard'
export default {
  name: 'learnmoreSection',
  props: {
      title: String,
      id: String
  },
  data: function(){
    return {
      featureCards: [
        {
          cardTitle: "Fastest Free Hosting",
          discription: "Our hosting was independently tested and found to be the fastest free hosting in the world.",
          src: "/imgs/icons/speed.svg"
        },
        {
          cardTitle: "99.9% Uptime",
          discription: "Uptime is our main priority, which is why we can proudly say we offer 99.9% uptime.",
          src: "/imgs/icons/lightning.svg"
        },
        {
          cardTitle: "Unlimited Hosting",
          discription: "Hosterx.ml is website hosting with unlimited disk space and unlimited bandwidth.",
          src: "/imgs/icons/processor.svg"
        },
        {
          cardTitle: "Completely Free",
          discription: "InfinityFree is completely free, no credit card required, no time limits and no hidden fees.",
          src: "/imgs/icons/coin.svg"
        },
        {
          cardTitle: "No Forced Ads",
          discription: "Your website is your own, we will never force advertisements on your website.",
          src: "/imgs/icons/eraser.svg"
        },
        {
          cardTitle: "Host Any Domain",
          discription: "Bring your own domain name or pick a free subdomain name from over 25 domain extensions.",
          src: "/imgs/icons/www.svg"
        }
      ]
    }
  },
  components: {
    featureCard
  }
}
</script>

<style scoped>

</style>
