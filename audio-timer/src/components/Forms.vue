<template>
    <form @submit.prevent="onSubmit">
        <input type="text" v-model="title" class="input-timer-name" placeholder="Timer Name">
        <button class="btn-create-timer">Create Timer</button>
    </form>
</template>

<script>

import '../style/forms.css'

export default {
    data() {
        return{
            title:''
        }
    },
    methods: {
        onSubmit () {
           if (this.title.trim()) {
               const newList = {
                   id: Date.now(),
                   title: this.title,
                   completed: false
               }
               this.$emit('add-list', newList)
               this.title = ''
           }
            
        }
    } 
}
</script>