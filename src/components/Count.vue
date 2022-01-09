<template>
  <div class="counter">
    Count: {{ count }}<br>
    Double Count: {{ doubleCount }}<br>
    <button @click="inc">Inc</button>
    <br>
    <button @click="dec">Dec</button>
    <br>
    Msg: {{ msg }}<br>
    <button @click="changedMessage">Change message</button>
  </div>
</template>
<script>

import {computed, ref, watch} from "vue";

export default {
  name: "Count",
  setup() {
    let count         = ref(0)
    const doubleCount = computed(() => count.value * 2)
    watch(count, newVal => {
      console.log("count changed", newVal)
    })
    const inc = () => {
      count.value += 1;
    }
    const dec = () => {
      if (count.value !== 0) {
        count.value -= 1
      }
    }
    /* ----------------------------*/
    let msg = ref("message")
    watch(msg, newMsg => {
      console.log("Change New Msg", newMsg)
    })
    const changedMessage = () => {
      msg.value = "new Message"
    }
    return {
      count,
      inc,
      dec,
      doubleCount,
      msg,
      changedMessage
    }
  }
}
</script>