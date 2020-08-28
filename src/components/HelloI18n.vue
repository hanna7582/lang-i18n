
<i18n>
{
  "ko": {
    "hello": "안녕하세요!"
  },
  "en": {
    "hello": "hello world!"
  }
}
</i18n>

<template>
  <div>
    <h2>SFC</h2>
    <select v-model="locale">
      <option>en</option>
      <option>ko</option>
    </select>
    <p>message: {{ $t('hello') }}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloI18n',
  data () {
    this.$i18n.locale = 'en';
    return { 
      locale: 'en' 
    }
  },
  watch: {
    locale (val) {
      this.$i18n.locale = val
    }
  }
}
</script>
