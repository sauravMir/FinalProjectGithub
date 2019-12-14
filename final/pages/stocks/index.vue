<template>
  <div class="is-vertical is-12">
    <grid-box :itemData = "itemData" :itemsInEachRow = 4 :columnWidthWithIn12 = 3></grid-box>
  </div>
</template>

<script>
import Card from "../../components/Card";
import GridBox from "../../components/GridBox";
export default {
  data() {
    return {
      isCollapsible: false,
      itemData: [
        {
          header: "thai",
          description: "its amazing neeeeee"
        }
      ]
    }
  },
  methods: {
  },
  components: {
    Card,GridBox
  }
};
</script>