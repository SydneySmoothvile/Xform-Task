<template>
  <div>XForm template</div>
  <div>
    <input
      v-for="field in fields"
      :key="fields.field"
      v-bind:fields="fields.field"
      {{
      fields.component
      }}
    />

    {{ fields.component }}
  </div>

  <div>
    My Input:
    <input v-model="inputVal" />
  </div>

  <input type="text" :value="myObject1" />
</template>

<script>
export default {
  props: ['fields'],
  computed: {
    inputVal: {
      get() {
        return this.value;
      },
      set(val) {
        this.$emit('input', val);
      },
    },
  },
};
</script>
