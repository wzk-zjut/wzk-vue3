<template>
    <button @click="toggleModalState">Open Modal</button>
    <modal v-if="modalOption">
        <p>Hello, I'm a modal window.</p>
    </modal>
</template>

<script>
import Modal from './views/Modal.vue'
import { ref } from 'vue'

export default {
    components: {
        Modal
    },
    setup() {
        const modalOption = ref(false)
        const toggleModalState = () => {
            modalOption.value = !modalOption.value
        }
        return {
            modalOption,
            toggleModalState
        }
    }
}
</script>

<style scoped>
</style>
