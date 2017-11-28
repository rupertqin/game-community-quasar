<template>
  <!-- if you want automatic padding use "layout-padding" class -->
  <div>
    <!-- your content -->
    <q-carousel class="text-white">
      <div slot="slide" class="bg-primary">
        Slide 1
      </div>
      <div slot="slide" class="bg-secondary">
        Slide 2
      </div>
      <div slot="slide" class="bg-tertiary">
        Slide 3
      </div>
    </q-carousel>

    <div class="doc-container">
      <div class="row">
        <div class="col"> 首页 </div> 
        <div class="col">资讯 </div> 
        <div class="col">资讯 </div> 
        <div class="col">资讯 </div> 
        <div class="col">资讯 </div> 
        <div class="col">资讯 </div> 
        <div class="col">资讯 </div> 
        <div class="col">资讯 </div> 
      </div> 
    </div>
    <q-list>
      <q-item>
        <q-item-side icon="phone" color="primary" />
        <q-item-main>
          <q-item-tile label>(650) 555 - 1234</q-item-tile>
          <q-item-tile sublabel>Mobile</q-item-tile>
        </q-item-main>
        <q-item-side right icon="chat_bubble" />
      </q-item>
      <q-item>
        <q-item-main inset>
          <q-item-tile label>(650) 555 - 1234</q-item-tile>
          <q-item-tile sublabel>Mobile</q-item-tile>
        </q-item-main>
        <q-item-side right icon="chat_bubble" />
      </q-item>
      <q-item-separator inset />
      <q-item>
        <q-item-side icon="mail" color="primary" />
        <q-item-main>
          <q-item-tile label>john@doe.com</q-item-tile>
          <q-item-tile sublabel>Personal</q-item-tile>
        </q-item-main>
      </q-item>
      <q-item>
        <q-item-main inset>
          <q-item-tile label>john@doe.com</q-item-tile>
          <q-item-tile sublabel>Personal</q-item-tile>
        </q-item-main>
      </q-item>
    </q-list>

    <div slot="left">left</div>
    <div slot="cpu"> cpu is news here </div>
  </div>
</template>

<script>
import {
  QList,
  QItem,
  QItemMain,
  QItemTile,
  QItemSide,
  QItemSeparator,
  QCarousel,
  QBtn,
  QIcon,
  QToolbar,
  QToolbarTitle
} from 'quasar'

export default {
  components: {
    QList,
    QItem,
    QItemMain,
    QItemTile,
    QItemSide,
    QItemSeparator,
    QCarousel,
    QBtn,
    QIcon,
    QToolbar,
    QToolbarTitle
  },
  data () {
    return {
      title: '首页',
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
