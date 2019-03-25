<template>
  <view class="container">
    <text class="text-color-primary">{{message}}</text>
    <text>Мобильное приложение на JavaScript</text>
    <text-input
        :style="{height: 40, width: 150, borderColor: 'gray', borderWidth: 1}"
        v-model="text"/>
    <button
      :on-press="checkLang"
      title="Learn More"
      color="#841584"
      accessibility-label="Learn more about this purple button"
    />
    </view>
</template>
 
<script>
export default {
  data () {
    return {
      message: 'Dictionary+',
      text: ''
    }
  },
  methods: {
    checkLang() {
      (this.text.search(/[А-яЁё]/) === -1) ? alert('English language') : alert('Русский язык') 
    }
  },
}
</script>

<style>
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
