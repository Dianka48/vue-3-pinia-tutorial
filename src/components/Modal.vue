<template>
    <teleport to=".modals-container">
        <div class="modal">
            <h1>{{ title }}</h1>
            <slot />
            <!-- <pre>{{ $slots.title() }}</pre> -->
            <button @click="handleButtonClick">Hide modal</button>
        </div>
    </teleport>
</template>

<script setup>
// import { useSlots } from "vue";

// props
const props = defineProps({
    title: {
        type: String,
        default: "No title specified",
    },
});
// console.log(props.title);

// emits
const emit = defineEmits(["hideModal"]);

// handle button click
const handleButtonClick = () => {
    emit("hideModal");
};

// const slots = useSlots();

// console.log(slots.title());
</script>

<style scoped>
.modal {
    background: beige;
    padding: 10px;
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    z-index: 1;
}
</style>
