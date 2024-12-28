<script setup lang="ts">


const show = ref(false);
const onClick = () => show.value = !show.value;

</script>

<template>
  <div>
    <MainHeader />
    <div>
      <ButtonSubmitButton />
      <button @click="onClick">
        {{ show ? 'Hide' : 'Show' }}
      </button>
      <LazyTestComp v-if="show" />
    </div>
    <MainFooter />
  </div>
</template>
