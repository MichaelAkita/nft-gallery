<template>
  <div class="container mb-1">
      <section>
        <h1 class="title is-2">Top Collection</h1>
        <p class="subtitle is-size-5">The top NFTs on RMRK, ranked by score, volume, floor price and other statistics.</p>

        <SeriesTable />
      </section>
  </div>
</template>
<script lang="ts" >
import { Component, Vue } from 'vue-property-decorator'

@Component<Series>({
  metaInfo() {
    return {
      meta: [
        {
          property: 'og:title',
          content: 'KodaDot | Kusama NFT Market explorer'
        },
        { property: 'og:url', content: 'https://nft.kodadot.xyz' },
        {
          property: 'og:description',
          content: 'Discover new artists based on rank'
        },
        {
          property: 'og:site_name',
          content: 'Low fees and low carbon minting'
        },
        {
          property: 'og:image',
          content: 'https://nft.kodadot.xyz/kodadot_community.jpeg'
        },
        {
          property: 'twitter:title',
          content: 'NFT artist rank'
        },
        {
          property: 'twitter:description',
          content: 'Discover new artists based on rank'
        },
        {
          property: 'twitter:image',
          content: 'https://nft.kodadot.xyz/kodadot_community.jpeg'
        }
      ]
    }
  },
  components: {
    Identity: () => import('@/components/shared/format/Identity.vue'),
    SeriesTable: () => import('@/components/series/SeriesTable.vue')
  }
})
export default class Series extends Vue {}
</script>
