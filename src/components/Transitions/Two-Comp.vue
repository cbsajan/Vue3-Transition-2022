<template>
    <div>
        <button class="btn btn-primary" @click="status = !status">
            Toggle status
        </button>
        <br><br>
        <transition mode="out-in" name="custom" enter-active-class="dog_new" leave-active-class="cat">
            <div class="p-3 mb-2 bg-danger text-white" v-if="!status" key="status_off">OFF</div>
            <div class="p-3 mb-2 bg-success text-white" key="status_on" v-else>ON</div>
        </transition>
        <hr>
        <button class="btn btn-primary" @click="libary = !libary">Toggle Animate</button>
        <br><br>
        <transition name="custom-class-not-to-confuse-with-other-ones"
            enter-active-class="animate__animated animate__backInDown"
            leave-active-class="animate__animated animate__backOutLeft">
            <div class="p-3 mb-2 bg-info text-white" v-if="libary">Hello</div>

        </transition>
    </div>
</template>

<script>
export default {
    data() {
        return {
            status: false,
            libary: false
        }
    }
}
</script>

<style>
.custom-enter-from,
.custom-leave-to {
    opacity: 0;
}

.dog_new,
.cat {
    transition: .3s;
}

.custom-enter-to,
.custom-leave-from {
    opacity: 1;
}
</style>