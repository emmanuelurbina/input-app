<template>
    <div class="input-content">
        <input type="text">
        <label class="label__input"> {{ label }} </label>
    </div>
</template>


<script>
export default {
    data(){
        return{
            label: "default input"
        }
    }
}
</script>

<style  scoped>
.input-component {
    display: block;
    margin: 0;
}

</style>