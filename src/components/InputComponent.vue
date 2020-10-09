<template>
  <div class="input__content">
    <div class="group__input">
      <input type="text" :class="[style_input]"  />
      <label class="label__input"> {{ label }} </label>
    </div>
  </div>
</template>


<script>
export default {
  props: ["style_input"],
  data() {
    return {
      label: "Label",
    };
  },
};
</script>

<style  scoped>
/**
    general styles
 */
 
.group__input {
  position: relative;
  width: 600px;
}

.max__width {
    width: 100%!important;
}

.label__input {
  position: absolute;
  top: -20px;
  left: 0;
  color: #333333;
}
input[type="text"] {
  outline: none;
  padding: .8em 1em;
  border-radius: 5px;
}

/**input sizing
sm
0.4em 1em
 */

/**
    default style
    .hover
    .focus
 */
.default {
  color: #828282;
  border: 1px solid #828282;
}

.default:hover {
  border-color: #333333;
}

.default:focus {
  border-color: #2962ff;
}

.default:focus + .label__input {
  color: #2962ff;
}

/**
    error style
    .hover
    .focus
 */
.error {
  color: #828282;
  border: 1px solid #D32F2F;
}
.error + .label__input {
    color: #D32F2F;
}
.error:hover {
  border-color: #333333;
}

.error:hover + .label__input {
  color: #333333;
}

.error:focus {
  border-color: #D32F2F;
}

.error:focus + .label__input {
  color: #D32F2F;
}



</style>