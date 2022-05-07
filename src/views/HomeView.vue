<script lang="ts">
import { defineComponent } from 'vue'
import { useCounterStore } from './../stores/counter'
import HelloWorld from './../components/HelloWorld.vue'

export default defineComponent({
    components: {
        HelloWorld
    },
    setup() {
        const store = useCounterStore()
        return {
            // you can return the whole store instance to use it in the template
            store,
        }
    }
})
</script>

<template>
    <div>
        <HelloWorld msg="You did it!" />
    </div>
    <div>
        <button @click="store.increment">Count</button>
        <span>{{ store.counter }}</span>
    </div>
</template>

<style scoped>
div {
    text-align: center;
}

button {
    color: hsla(160, 100%, 37%, 1);
    border: 1px solid hsla(160, 100%, 37%, 1);
}

span {
    padding: 0 20px;
    font-weight: bold;
    color: gray;
}
</style>