<template>

    <body class="bg-[#F5F5F5] min-h-screen relative">
        <div class="pt-5 px-16 lg:p-8">
            <!-- header -->
            <div class="flex justify-between items-start lg:max-w-[1280px] lg:mx-auto">
                <div class="border-gray-500">
                    <h1 class="text-4xl text-gray-800 tracking-wide">Start now</h1>
                    <p class="text-4xl text-gray-800 tracking-wide">your <span class="font-bold">free plan</span></p>
                </div>
                <button @click="toggleShowModal"
                    class="bg-primary text-white py-2 px-4 tracking-widest rounded-sm ring-primary ring-offset-2 active:ring-2 duration-100">LOGIN</button>
            </div>

            <!-- main -->
            <div class="lg:grid lg:grid-cols-3 lg:justify-evenly lg:gap-8 lg:max-w-[1280px] lg:mx-auto">
                <div class="w-full p-8 mt-16 bg-secondary rounded-2xl hover:scale-105 duration-150 shadow-2xl">
                    <p class="text-3xl font-bold">Free $0 <span class="text-base text-gray-600 font-medium">per
                            mounth</span></p>
                    <div class="w-[30px] h-[3px] bg-primary mt-4"></div>
                    <p class="mt-8 font-bold text-lg">Plan includes:</p>

                    <!-- 嘗試使用v-for -->
                    <ul id="list1" class="text-lg mb-20">
                        <Clist />
                        <Clist />
                        <Clist />
                    </ul>

                    <a href="#" class="block w-full mb-8 font-bold text-center">view all the features</a>
                    <button
                        class="w-full bg-primary py-3 text-white rounded-lg tracking-wider text-lg">subscribe</button>
                </div>
                <div class="w-full p-8 mt-16 bg-primary rounded-2xl hover:scale-105 duration-150 text-white shadow-2xl">
                    <p class="text-3xl font-bold">Standard 20$ <span class="text-base text-white font-medium">per
                            mounth</span></p>
                    <div class="w-[30px] h-[3px] bg-white mt-4"></div>
                    <p class="mt-8 font-bold text-lg">Plan includes:</p>

                    <!-- 嘗試使用v-for -->
                    <ul id="list1" class="text-lg mb-20">
                        <Clist color="text-white" />
                        <Clist color="text-white" />
                        <Clist color="text-white" />
                    </ul>

                    <a href="#" class="block w-full mb-8 font-bold text-center">view all the features</a>
                    <button
                        class="w-full bg-white py-3 text-black rounded-lg tracking-wider text-lg">subscribe</button>
                </div>
                <div class="w-full p-8 mt-16 bg-secondary rounded-2xl hover:scale-105 duration-150 shadow-2xl">
                    <p class="text-3xl font-bold">Pro $90 <span class="text-base text-gray-600 font-medium">per
                            mounth</span></p>
                    <div class="w-[30px] h-[3px] bg-primary mt-4"></div>
                    <p class="mt-8 font-bold text-lg">Plan includes:</p>

                    <!-- 嘗試使用v-for -->
                    <ul id="list1" class="text-lg mb-20">
                        <Clist />
                        <Clist />
                        <Clist />
                    </ul>

                    <a href="#" class="block w-full mb-8 font-bold text-center">view all the features</a>
                    <button
                        class="w-full bg-primary py-3 text-white rounded-lg tracking-wider text-lg">subscribe</button>
                </div>
            </div>

            <!-- modal -->
            <Modal v-show="showModal" @close="toggleShowModal"/>


        </div>
    </body>
</template>

<script>
    import Clist from './Clist.vue'
    import Modal from './Modal.vue'
    export default {
        data(){
            return{
                showModal: true
            }
        },
        methods: {
        toggleShowModal(){
            this.showModal = !this.showModal
        }
    },
        components: {
            Clist,Modal
        }
    }
</script>