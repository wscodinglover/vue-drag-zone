<template>
  <md-card>
    <md-card-actions>
      <div class="md-subhead">
        <span>Vertical MinHeight and MaxHeight</span>
      </div>
      <md-button class="md-icon-button"
                 target="_blank"
                 href="https://github.com/surmon-china/vue-drag-zone/tree/master/examples/04-example.vue">
        <md-icon>code</md-icon>
      </md-button>
    </md-card-actions>
    <md-card-media>
      <!-- drag-zone -->
      <drag-zone class="zone" :options="{ direction: 'vertical' }">
        <drag-content class="content c1">
          <div class="item i1">min-height: 60px max-height: 20rem</div>
        </drag-content>
        <drag-handle class="handle"></drag-handle>
        <drag-content class="content c2">
          <div class="item i2">item 2</div>
        </drag-content>
        <drag-handle class="handle"></drag-handle>
        <drag-content class="content c3">
          <div class="item i3">min-height: 70px</div>
        </drag-content>
        <drag-content class="content c4">
          <div class="item i4">item 4</div>
        </drag-content>
        <drag-handle class="handle"></drag-handle>
        <drag-content class="content c5">
          <div class="item i5">min-height: 5em</div>
        </drag-content>
      </drag-zone>
    </md-card-media>
  </md-card>
</template>

<script>
  export default {
    data() {
      return {
      }
    }
  }
</script>

<style scoped>
  .zone {
    width: 100%;
    height: 500px;
    margin: 0 auto;
    position: relative;
    clear: both;
    text-align: center;
    color: white;
    background: #eee;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
  }
  .zone .handle {
    width: 100%;
    height: 10px;
    background: #2196f3;
  }
  .zone .item {
    width: 100%;
  }
  .zone .content {
    width: 100%;
    height: calc((100% - 30px) / 4);
    overflow: hidden;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .zone .content.c1 {
    min-height: 60px;
    max-height: 20rem;
    background: #999;
  }
  .zone .content.c2 {
    background: #777;
  }
  .zone .content.c3 {
    min-height: 70px;
    background: #555;
  }
  .zone .content.c4 {
    background: #333;
  }
  .zone .content.c5 {
    min-height: 5em;
    background: #000;
  }
</style>
