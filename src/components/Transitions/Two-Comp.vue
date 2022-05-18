<template>
    <div>
        <button class="btn btn-primary" @click="status = !status">
            Toggle status
        </button>
        <br><br>
        <transition mode="out-in" name="custom" enter-active-class="dog" leave-active-class="cat">
            <div class="p-3 mb-2 bg-danger text-white" v-if="!status" key="status_off">OFF</div>
            <div class="p-3 mb-2 bg-success text-white" key="status_on" v-else>ON</div>
        </transition>

    </div>
</template>

<script>
export default {
    data() {
        return {
            status: false
        }
    }
}
</script>

<style>
.custom-enter-from,
.custom-leave-to {
    opacity: 0;
}

.dog,
.cat {
    transition: .3s;
}

.custom-enter-to,
.custom-leave-from {
    opacity: 1;
}
</style>