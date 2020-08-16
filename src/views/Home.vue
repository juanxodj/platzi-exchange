<template>
  <PxAssetsTable :assets="assets"></PxAssetsTable>
</template>

<script>
import PxAssetsTable from '@/components/PxAssetsTable'
import api from '@/api'

export default {
  name: 'Home',
  components: { PxAssetsTable },
  data() {
    return {
      assets: []
    }
  },
  created() {
    api.getAssets().then(assets => (this.assets = assets))
  }
}
</script>

<style></style>
