<template>
  <div class="hello">
    <h1>{{ title }}</h1>
    <p>{{ message }}</p>
    <hr>
    <p>Number: {{ num }}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld2',
  props: {
    title: String,
    num: {
      type:Number,
      default: 100,
      validator: function (value) {
        return value == parseInt(value)
          && value >= 0 && value <= 100
      }
    }
  },
  data:function() {
    return {
      message: 'バリデーションチェック',
    }
  }
}
</script>

<style scoped>
div {
  margin: 0px;
  padding: 0px;
  text-align: left;
}

h1 {
  font-size: 72px;
  font-weight: bold;
  text-align: right;
  letter-spacing: -8px;
  color: #f0f0f0;
  margin: 0px;
}

p {
  margin: 0px;
  color: #666;
  font-size: 16px;
}
</style>
