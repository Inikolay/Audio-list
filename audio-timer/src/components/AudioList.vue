<template>
    <div>
        <div class="list">
        <ul class="list-position">
            <li><List
            v-for="audiu of lists"
            v-bind:audiu="audiu"
            v-bind:key="audiu.id"
            v-on:remove-audiu="removeAudiu"
            />
             </li>
        </ul>
    </div>
    </div>
</template>

<script>
import '../style/audio-list.css'
import List from '../components/List.vue'


export default {
    props: ['lists'],
    components: {
        List
    },
    methods: {
        removeAudiu(id) {
            this.$emit('remove-audiu', id)
            
        }
    }
}

</script>