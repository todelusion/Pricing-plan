<template>
<div class="absolute top-0 left-0 bg-black/70 w-full h-full flex justify-center items-start">
    <div class="w-[70%] p-4 bg-white mt-[155px] rounded-md lg:w-[30%]">
        <h3>標題</h3>
        <p>內文</p>
        <button
            @click="closeModal"
            class="mt-4 w-full bg-primary py-3 text-white rounded-lg tracking-wider text-lg"
            >close
        </button>
    </div>
</div>

</template>

<script>
export default {
    methods: {
        closeModal(){
            this.$emit('close')
        }
    }
}
</script>