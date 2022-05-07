<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
    props: {
        msg: {
            type: String,
            required: true
        }
    },
    setup({ msg }) {
        return {
            msg
        }
    }
})
</script>

<template>
    <div>
        <h3>{{ msg }}</h3>
        <h5>You’ve successfully created a project.</h5>
    </div>
</template>

<style scoped>
div {
    margin-top: 30px;
    color: gray;
}

h3 {
    color: hsla(160, 100%, 37%, 1);
}
</style>
