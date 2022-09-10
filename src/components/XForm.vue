<template>
  <div>XForm template</div>

  <div>
    <label> Name </label>
    <input v-model="fields.myfields1" />
    <form>
      <input v-model="myObject1.name" type="text" placeholder="Name" />
    </form>
  </div>

  <div>
    <label> Date of Birth </label>
    <input type="datetime" placeholder="Input" />
  </div>

  <div>
    <label>Eye color </label>
  </div>

  <div name="id"></div>

  <div>
    <label> Created </label>
    <input name="created" type="datetime" placeholder="Input" />
  </div>

  <div>
    <label> Updated </label>
    <input name="updated" type="datetime" placeholder="Input" />
  </div>

  <div>
    <label> Label </label>
    <input name="label" type="text" placeholder="Input" />
  </div>

  <div>
    <label> Name </label>
    <input name="name" type="text" placeholder="Input" />
  </div>
</template>

<script>
export default {
  props: {
    propsA:['myObject1', 'myfields1'],
    propsB:['myObject2', 'myfields2'],
    propsC:['myObject3', 'myfields3']
  }
};
</script>
