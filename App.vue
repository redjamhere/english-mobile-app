<template>
  <view class="container">
    <text class="text-color-primary" :style="{fontSize: 24, textAlign: 'center'}">Мобильное приложение на {{message}}</text>
    <text-input
        :style="{height: 50, width: 200, borderColor: '#3498db', borderWidth: 1, borderRadius: 7, marginTop: 50, marginBottom: 50}"
        v-model="text"/>
    <button title="Определить язык" :on-press="checkLang"/>
    <text :style="{marginTop: 50, fontSize: 18, color: '#7f8c8d'}">by Займанов Айнур</text>
    </view>
</template>
 
<script>
export default {
  data () {
    return {
      message: 'JavaScript',
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

<style lang="scss">
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}

.text-color-primary {
  color: #3498db;
}

.my-button {
  width: 400;
}
</style>

