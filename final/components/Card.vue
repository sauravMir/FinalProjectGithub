<template>
  <div class="column">
    <div class="card">
      <header class="card-header">
        <p class="card-header-title has-text-grey">
          {{ title }}
        </p>
      </header>
      <div class="card-content">
        <div class="content has-text-centered">
          <b-icon :icon="icon" size="is-large" type="is-primary" />
        </div>
      </div>

      <div class="tile-container ">
        <div class="tile">
          <button class="block" style="background-color: orange;">Cancel</button>
        </div>
        <div class="tile">
          <button class="block" style="background-color: green;">Add</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    icon: {
      type: String,
      required: true
    }
  }
};
</script>

<style scoped>
.tile-container {
  position: relative;
  width: 100%;
  font-size: 0; /* add */
}

.tile {
  font-size: 20px; /* or whatever you want */
  width: 50%;
  min-height: 40px;
  display: inline-block;
  color: white;
  
}
.center-button {
  width: 50%px; 
  margin: 0 auto;
}
.block {
  display: block;
  width: 100%;
  height: 50px;
  border: 1px grey;
  border-style: solid;
  text-align: center;
  margin: auto;
  color: white;
  font-weight: bold;
}
</style>
