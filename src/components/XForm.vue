<template>
  <div>XForm template</div>
  <div>
    <input
      v-for="field in fields"
      :key="fields.field"
      v-bind:fields="fields.field"
    />

    {{ fields.component }}
  </div>

  <li v-for="item in items" :key="item.message">
    {{ item.message }}
  </li>

  <div v-for="object1 in myObject1">
    My Input:
    <input v-model="inputVal" />
  </div>

  <div v-for="object1 in myObject1">
        {{object1.name}}
      </div>

  <input type="text" :fields="myObject1" />
</template>

<script>
export default {
  props: ['fields'],
  computed: {
    inputVal: {
      get() {
        return this.fields;
      },
      set(val) {
        this.$emit('input', val);
      },
    },
  },
};
</script>
