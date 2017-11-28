<template>
  <!-- if you want automatic padding use "layout-padding" class -->
  <div>
    <!-- your content -->
    <div slot="left">left</div>
    <div slot="cpu"> cpu is news here </div>
  </div>
</template>

<script>
import {
  QBtn,
  QIcon,
  QToolbar,
  QToolbarTitle
} from 'quasar'

export default {
  components: {
    QBtn,
    QIcon,
    QToolbar,
    QToolbarTitle
  },
  data () {
    return {
      title: '新闻',
      subtitle: '中文游戏社区'
    }
  },
  created () {
    this.$emit('child-say', this.title, this.subtitle)
  }
}
</script>

<style>
</style>
