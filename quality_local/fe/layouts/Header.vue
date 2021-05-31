<template>
  <div class="header">
    <a-row>
      <a-col :span="21">
        <sider-menu />
      </a-col>
      <a-col :span="3">
        <user-menu />
      </a-col>
    </a-row>
  </div>
</template>

<script>
import SiderMenu from './SiderMenu'

export default {
  components: {
    SiderMenu,
  },
  methods: {
    localeChange({ key }) {
      this.$router.push({ query: { ...this.$route.query, locale: key } })
      this.$i18n.locale = key
    },
  },
}
</script>
