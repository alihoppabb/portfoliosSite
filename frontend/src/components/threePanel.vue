<template>
  <div>
    <kinesis-container event="move">
      <kinesis-element
          tag="svg"
          :transformOrigin="center"
          :strength="20"
          type="depth">
        <img src="../assets/phone.svg" width="500px" height="500px" alt="">
      </kinesis-element>
    </kinesis-container>
  </div>
</template>

<script>
import { KinesisContainer, KinesisElement} from "vue-kinesis"
export default {
  name: "threePanel",
  components: { KinesisContainer, KinesisElement }
}
</script>

<style scoped>

</style>