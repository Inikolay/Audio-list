<template>
    <div>
        <div class="position-block">
            <li class="list-block">
             {{ audiu.title }}
            <span class="time">{{ audiu.time }}</span>
            <button class="btn-play">
               <img src="./../assets/Shape.png" alt="Shape">
            </button>
            <button class="btn-delete"
             v-on:click="$emit('remove-audiu', audiu.id)"
             > 
                <img src="./../assets/Delete.png" alt="Delete">
             </button>
    </li>
        </div>
    </div>
</template>

<script>

import '../style/list.css'
export default {
    props: {
        audiu: {
            type: Object,
            required: true
        }
    }
}
</script>