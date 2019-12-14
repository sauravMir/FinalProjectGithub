<template>
  <div class="is-vertical">
    <div
      class="tile is-ancestor is-horizontal"
      v-for="(itemsInRow, index) in reStructureData()"
      :key="index"
    >
      <div :class="gridColumnWidth" v-for="(items, itemIndex) in itemsInRow" :key="itemIndex">
        <card :title="items.header" icon="items.description"></card>
      </div>
    </div>
  </div>
</template>


<script>
import Card from "./Card";
export default {
  props: {
    itemData: {
      //send header and description i.e : I think its better to use type script here
      type: Array,
      required: true
    },
    itemsInEachRow: {
      type: Number,
      required: true
    },
    columnWidthWithIn12: {
      type: Number,
      required: true
    }
  },
  data() {
    return {
      //use data if necessary
    };
  },
  computed: {
    gridColumnWidth: function() {
      return "tile is-" + this.columnWidthWithIn12;
    }
  },
  methods: {
    reStructureData: function() {
      var itemsInARow = [];
      var eachRowWithItsItems = [];
      for (var loop1i = 0; loop1i < this.itemData.length; loop1i++) {
        itemsInARow.push(this.itemData[loop1i]);
        if ((loop1i + 1) % this.itemsInEachRow == 0) {
          eachRowWithItsItems.push(itemsInARow);
          itemsInARow = [];
        }
      }
      //now add the remaining of the items
      eachRowWithItsItems.push(itemsInARow);
      console.log(eachRowWithItsItems);
      return eachRowWithItsItems;
    }
  },
  components: {
    Card
  }
};
</script>