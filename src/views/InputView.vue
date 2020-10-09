<template>
    <div class="content">
        <inputComponent  />
    </div>
</template>



<script>
import inputComponent from "@/components/InputComponent.vue"
export default {
    data() {
        return {
            types: [
                "default",
                "error"
            ]
        }
    },
    components: {
        inputComponent
    }
}
</script>

<style scoped>
.content {
    display: flex;
    flex-direction: row;
    justify-content: center;
}
</style>