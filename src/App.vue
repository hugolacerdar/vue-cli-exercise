<template>
  <h1>Your Upcoming Destinations</h1>
  <div class="location-contain">
    <div class="locations" v-for="loc in locations" :key="loc.name">
      <CityCard :name="loc.name" :image="loc.img" :description="loc.desc">
        <p>
          Buy tickets for {{ loc.name.toUpperCase() }}
          <a href="https://google.com" target="_blank">here!</a>
        </p>
      </CityCard>
    </div>
  </div>
</template>

<script>
import CityCard from "./components/CityCard.vue";

export default {
  name: "App",
  components: {
    CityCard,
  },
  data() {
    return {
      locations: [
        {
          name: "moscow",
          img: "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/moscow.svg",
          desc: `Moscow is the capital and most populous city of Russia, with 13.2 million residents within the city limits and 17.8 million within the urban area. Moscow has the status of a Russian federal city.`,
        },
        {
          name: "paris",
          img: "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/paris1.svg",
          desc: `Paris is the capital and most populous city of France. By the 17th century, Paris was one of Europe's major centres of finance, commerce, fashion, science, and the arts, and it retains that position still today.`,
        },
        {
          name: "rome",
          img: "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/rome.svg",
          desc: `Rome's history spans more than 2,500 years. While Roman mythology dates the founding of Rome at around 753 BC, the site has been inhabited for much longer, making it one of the oldest continuously occupied sites in Europe.`,
        },
        {
          name: "paris",
          img: "https://s3-us-west-2.amazonaws.com/s.cdpn.io/28963/paris2.svg",
          desc: `By the end of the 12th century, Paris had become the political, economic, religious, and cultural capital of France. Maurice de Sully undertook the construction of the Notre Dame Cathedral at its eastern extremity.`,
        },
      ],
    };
  },
};
</script>

<style lang="sass">
body
  width: 100vw
  height: 100vh
  font-family: 'NTR', sans-serif
  background: #eee

h1
  text-align: center

.location-contain
  display: flex
  justify-content: center

.place
  display: flex
  flex-direction: column
  width: 280px
  height: 400x
  justify-content: center
  background: white
  border: 1px solid #ddd
  padding: 20px 20px
  margin: 10px
  h2
    margin: 0
    text-align: center
    text-transform: capitalize

  img
    margin: 10px
    align-self: center
</style>
