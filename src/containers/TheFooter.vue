<template>
  <CFooter :fixed="false">
    <div>
      <a href="http://inspektorat.kotabogor.go.id" target="_blank">Inspektorat Kota Bogor</a>
      <span class="ml-1">&copy; {{new Date().getFullYear()}}</span>
    </div>
    <div class="ml-auto">
      <span class="mr-1">Dibuat Oleh</span>
      <a href="#" target="_blank">Summit Citra Teknologi</a>
    </div>
  </CFooter>
</template>

<script>
export default {
  name: 'TheFooter'
}
</script>
