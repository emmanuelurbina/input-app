<template>
  <div class="content">
    <inputComponent :style_input="type" />

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
                <option value="default" selected>Select Size</option>
                <option
                  v-for="(type,index) in types"
                  :key="index"
                  :value="type"
                >
                  {{ type }}
                </option>
              </select>
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
      types: [
          "default",
          "error"
      ],  
      type: "default",
    };
  },
  components: {
    inputComponent,
  },
  methods: {
      typeChange: function(){
          this.type = event.target.value;
      }
  }
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

.select__input {
    outline: none;
    padding: .6em 1em;
    width: 100%;
    border-radius: 8px;
    text-transform: capitalize;
}
</style>