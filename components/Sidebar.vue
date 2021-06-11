<template>
  <div class="sidebar" data-color="green" data-background-color="white">
    <div class="logo">
      コーチングプラス
    </div>
    <div class="sidebar-wrapper">
      <ul class="nav">
        <li v-for="(link, i) in links" :key="`bad-sample_${i}`" class="nav-item">
          <a class="nav-link" href="javascript:void(0)" @click.prevent="onClick(link.path)">
            <i class="material-icons">{{ link.icon }}</i>
            <p>{{ link.label }}</p>
          </a>
        </li>
      </ul> 
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      links: [
        { label: 'ミーティング画面', icon:'dashboard', path: '/' },
        { label: 'マイページ', icon:'location_ons', path: '/map' }
      ]
    }
  },
  methods: {
    isInternalLink (path) {
      return !/^https?:\/\//.test(path)
    },
    onClick (path) {
      if (this.isInternalLink(path)) {
        this.$router.push(path)
      } else {
        location.href = path
      }
    }
  }
}
</script>