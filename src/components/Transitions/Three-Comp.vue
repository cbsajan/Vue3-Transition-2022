<template>
    <div class="form-group">
        <input v-model="name" class="form-control">
    </div>
    <button class="btn btn-primary" @click="addOne">
        Add one
    </button>
    <hr />
    <div>
        <ul class="pl-0">
            <transition-group name="fade">
                <li class="list-group-item" v-for="(item, index) in list" @click="removeItem(index)" :key="item">
                    {{ item }}
                </li>
            </transition-group>
        </ul>
    </div>

</template>


<script>
export default {
    data() {
        return {
            list: ['Francis', 'Ron', 'Martha'],
            name: ''
        }
    },
    methods: {
        addOne() {
            if (!this.list.includes(this.name)) {
                this.list.unshift(this.name)
            } else {
                alert("The Name is already in the list")
            }
        },
        removeItem(index) {
            this.list.splice(index, 1)
        }
    }
}
</script>



<style>
.fade-enter-from,
.fade-leave-to {
    opacity: 0;
}

.fade-enter-active {
    transition: 1s;
}

.fade-leave-active {
    width: 100%;
    transition: 1s;
    position: absolute;
}

.fade-enter-to,
.fade-leave-from {
    opacity: 1;
}

.fade-move {
    transition: transform 1s;
}
</style>