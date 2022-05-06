<template>
    <div class="modals">
        <h1>Modals</h1>
        <button @click="showModal = true">Show modal</button>
        <Modal
            @hideModal="showModal = false"
            v-if="showModal"
            title="My modal title (via prop)"
        >
            <!-- <template #title>My new title</template> -->
            <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Reiciendis exercitationem corporis deleniti a totam, enim
                dignissimos doloribus? Nam modi quo facere consequatur,
                obcaecati recusandae adipisci, quidem distinctio minus, fugit
                reprehenderit?
            </p>
        </Modal>
    </div>
</template>

<script setup>
import { ref } from "vue";
import Modal from "../components/Modal.vue";

// modal
const showModal = ref(false);
</script>
