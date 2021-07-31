<template>
  <div class="card">
    <div class="card-title">
      {{ card_title }}
    </div>
    <div class="card-body">
      <slot>
        Default data
      </slot>
    </div>
    <div class="card-footer">
      <slot name="card-footer">
        Default footer
      </slot>
    </div>
  </div>
</template>

<script>
export default {
  name : "Card",
  props: ['card_title']
}
</script>

<style>
.card {
  width: 200px;
  border: 1px solid #1d6c04;
  min-height: 100px;
  margin: 22px auto;
}

.card-title {
  background: #0b6204;
  padding: 5px 11px;
  color: white;
}

.card-body {
  padding: 11px;
}

.card-body img {
  height: 111px;
}

.card-footer {
  background: #8f8372;
  padding: 5px 11px;
  text-align: center;
}
</style>
