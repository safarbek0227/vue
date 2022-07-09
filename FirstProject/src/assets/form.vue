<script>
export default {
  data() {
    return {
      text: "",
      checked: false,
      checkedNames: ["safarbek"],
      picked: "One",
      selected: "A",
      multiSelected: ["A"],
    };
  },
};
</script>
<template>
  <div class="card">
    <h2>Text Input</h2>
    <div class="input-group">
      <input v-model="text" />
      <span>{{ text }}</span>
    </div>

    <h2>checkbox</h2>
    <div class="input-group">
      <input type="checkbox" id="checkbox" v-model="checked" />
      <span>Checked: {{ checked }}</span>
    </div>

    <h2>multi checkbox</h2>
    <div class="input-group">
      <input
        type="checkbox"
        id="safarbek"
        value="safarbek"
        v-model="checkedNames"
      />
      <label for="jack">safarbek</label>
      <input type="checkbox" id="john" value="John" v-model="checkedNames" />
      <label for="john">John</label>
      <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
      <label for="mike">Mike</label>
      <span>{{ checkedNames }}</span>
    </div>

    <h2>Radio</h2>
    <div class="input-group">
      <input type="radio" id="one" value="One" v-model="picked" />
      <label for="one">One</label>
      <br />
      <input type="radio" id="two" value="Two" v-model="picked" />
      <label for="two">Two</label>
      <br />
      <span>Picked: {{ picked }}</span>
    </div>

    <h2>select</h2>
    <div class="input-group">
      <select v-model="selected">
        <option disabled value="">Please select one</option>
        <option>A</option>
        <option>B</option>
        <option>C</option>
      </select>
      <span>Selected: {{ selected }}</span>
    </div>

    <h2>multiSelect</h2>
    <div class="input-group">
      <select v-model="multiSelected" multiple style="width: 100px">
        <option>A</option>
        <option>B</option>
        <option>C</option>
      </select>
      <span>Selected: {{ multiSelected }}</span>
    </div>
  </div>
</template>
<style>
.input-group {
  width: 100%;
  margin-bottom: 25px;
  display: flex;
  justify-content: space-around;
}
input,
select,
span {
  width: 300px;
  padding: 5px;
  border-radius: 8px;
  border: 4px solid #94b8ff;
  outline: none;
}
span {
  overflow: hidden;
  text-overflow: ellipsis;
}
label {
  font-size: large;
}
</style>