<template>
  <div>
    <h2>{{ a }}</h2>
    <nuxt-child />
  </div>
</template>

<script>
export default {
  async asyncData() {
    let a = 1;
    const p = new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve(2);
      }, 3000)
    })
    a = await p;
    return {
      a
    }
  }
}
</script>
