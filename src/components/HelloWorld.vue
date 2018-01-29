<template>
  <div class="hello">
    <select @change="switchLang(lang)" v-model="lang">
      <option value="en">EN</option>
      <option value="cn">CN</option>
    </select>
    <p>{{$t('message.hello')}}</p>
    <div class="block">
      <span class="demonstration">默认</span>
      <el-date-picker
        v-model="date"
        type="date"
        placeholder="选择日期">
      </el-date-picker>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      lang: 'en',
      date: ''
    }
  },
  mounted () {
  },
  methods: {
    switchLang (value) {
      console.log(value)
      // localStorage.lang = value
      this.$i18n.locale = value
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
