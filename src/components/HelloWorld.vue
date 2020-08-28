<template>
  <div class="hello">
    <h2>locales file</h2>
    <select v-model="$i18n.locale">
      <option v-for="(lang, i) in langs" :key="`Lang${i}`" :value="lang">{{ lang }}</option>
    </select>
    <p>{{ $t('hello', { name: name }) }}</p>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      langs: ['en', 'ko']
    }
  },
  computed: {
    name() {
      // 변수 사용시 
      if(this.$i18n.locale=='en'){
        return 'hanna' 
      }else{
        return '한나'
      }
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
