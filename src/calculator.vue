<template>
  <div class="calculator">
    <div class="gender">
      <input type="radio" id="woman" value="Woman" v-model="picked" />
      <label for="woman">Woman</label>
      <br />
      <input type="radio" id="man" value="Man" v-model="picked" />
      <label for="man">Man</label>
      <br />
      <span>Picked: {{ picked }}</span>
    </div>
    <div class="height">
      <input v-model.number="age" type="number" min="0" placeholder="edit me" />
      <p>Zadejte váš věk: {{ age }}</p>
      <button v-on:click></button>
    </div>
    <div class="menu__item">
      <input v-model.number="weight" type="number" min="0" placeholder="edit me" />
      <p>Zadej svou váhu: {{ weight }}</p>
    </div>
    <div class="menu__item">
      <input v-model.number="age" type="number" min="0" placeholder="edit me" />
      <p>Zadejte váší výšku: {{ height }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Menu",
  data() {
    return {
      picked: "",
      age: "",
      height: "",
      weight: ""
    };
  },
  methods: {
    tvujbazal() {
      return `Tvuj bazal je ${this.age * 5}`;
    }
  }
};
</script>

<style lang="css">
.calculator {
  display: flex;
  border: 2px solid black;
  background-color: lightblue;
  height: 1000px;
  width: 1000px;
  margin-left: 100px;
}
</style>