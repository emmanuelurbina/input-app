<template>
  <div class="content">
    <inputComponent
      :style_input="type"
      :style_size="size"
      :max_width="max_width"
    />

    <article class="table__content">
      <table class="table">
        <thead>
          <th>Description</th>
          <th>-</th>
        </thead>
        <tbody>
          <tr>
            <td>Type input</td>
            <td>
              <select class="select__input" @click="typeChange">
                <option value="default" selected>Select type</option>
                <option
                  v-for="(type, index) in types"
                  :key="index"
                  :value="type"
                >
                  {{ type }}
                </option>
              </select>
            </td>
          </tr>

          <tr>
            <td>Size input</td>
            <td>
              <select class="select__input" @click="sizeChange">
                <option value="default" selected>Select size</option>
                <option
                  v-for="(size, index) in sizes"
                  :key="index"
                  :value="index"
                >
                  {{ size }}
                </option>
              </select>
            </td>
          </tr>

          <tr>
            <td>Full width</td>
            <td>
              <input type="checkbox" v-model="max_width" />
            </td>
          </tr>
        </tbody>
      </table>
    </article>
  </div>
</template>



<script>
import inputComponent from "@/components/InputComponent.vue";
export default {
  data() {
    return {
      types: ["default", "error"],
      sizes: {
        input__sm: "Slim",
        input__md: "medium",
        input__lg: "Large",
      },
      max_width: false,
      size: "",
      type: "default",
    };
  },
  components: {
    inputComponent,
  },
  methods: {
    typeChange: function () {
      this.type = event.target.value;
    },
    sizeChange: function () {
      this.size = event.target.value;
    },
  },
};
</script>

<style scoped>
.content {
  display: grid;

  justify-content: center;
}
.table__content {
  width: 600px;
}

.table {
  margin-top: 5em;
  width: 100%;
  border: 1px solid #828282;
  border-radius: 8px;
  padding: 5px;
}
thead {
  text-align: left;
}
input[type=checkbox]{
  cursor: pointer;
  width: 20px;
  height: 20px;
}
.select__input {
  cursor: pointer;
  outline: none;
  padding: 0.6em 1em;
  width: 100%;
  border-radius: 8px;
  text-transform: capitalize;
}

@media screen and (max-width: 600px) {
  .table__content {
    width: 100%;
  }
}
</style>