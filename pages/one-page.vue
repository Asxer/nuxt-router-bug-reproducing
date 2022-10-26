<template>
  <div>
    <h1>One page</h1>

    <nuxt-link to="/another-page">
      Go to another page
    </nuxt-link>
  </div>
</template>

<script lang="ts" setup>
import { useRouter } from "#imports";

const router = useRouter()

async function setSearchFilters() {
  await router.push({
    query: {
      test: 1,
      some: 'complex',
      query: 1
    }
  })
}

await setSearchFilters()
</script>