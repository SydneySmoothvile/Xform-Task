<template>
  <div>XForm template</div>
  <div>
    <h1 v-for="field in fields" :key="field.component" >
      {{field.field}}
    </h1>
  </div>
</template>

<script>
export default {
  props: ['fields']
};
</script>
