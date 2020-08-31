<template>
  <CSidebar 
    fixed 
    :minimize="minimize"
    :show="show"
    @update:show="(value) => $store.commit('set', ['sidebarShow', value])"
  >
    <CSidebarBrand class="d-md-down-none" to="/">
      <CIcon 
        class="c-sidebar-brand-full" 
        src="http://kotabogor.go.id/uploads/images/logokotabogor.gif" 
        size="custom-size" 
        :height="35" 
        viewBox="0 0 556 134"
      />
      <h5 style="margin-left: 10px">Inspektorat Kota Bogor</h5>
      <CIcon 
        class="c-sidebar-brand-minimized" 
        src="http://kotabogor.go.id/uploads/images/logokotabogor.gif" 
        size="custom-size" 
        :height="35" 
        viewBox="0 0 110 134"
      />
    </CSidebarBrand>
   
    <CRenderFunction flat :content-to-render="$options.nav"/>
    
  </CSidebar>
</template>

<script>
import nav from './_nav'

export default {
  name: 'TheSidebar',
  nav,
  computed: {
    show () {
      return this.$store.state.sidebarShow 
    },
    minimize () {
      return this.$store.state.sidebarMinimize 
    }
  }
}
</script>
