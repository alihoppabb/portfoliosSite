<template>
  <div>
    <kinesis-container event="move">
      <kinesis-element
          :strength="15"
          :transformOrigin="0.5"
          axis = "x"
          minX="0.5"
          type="depth">
        <img src="../assets/site.png" alt="">
      </kinesis-element>
    </kinesis-container>
  </div>
</template>

<script>
import { KinesisContainer, KinesisElement} from "vue-kinesis"
export default {
  name: "threePanel",
  components:{KinesisContainer, KinesisElement},
  mounted() {

  }
}
</script>

<style scoped>

</style>