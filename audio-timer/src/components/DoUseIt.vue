<template>
    <div>
        <div class="use-block">
            <h5><span>Why</span> do we use it?</h5>
            <p>This sounded nonsense to Alice, so she said nothing,
             but set off at once toward<br> the Red Queen. To her surprise,
             she lost sight of her in a moment.</p>
        </div>
        <div class="border-play-audio">
            <Forms ref="foo"
            @add-list="addList"
             />
            <div>
              <AudioList
                v-bind:lists="lists"
                @remove-audiu="removeAudiu"
               />
            </div>
        </div>
        <Footer />
    </div>
</template>



<script>

import '../style/do-use-it.css'
import AudioList from '../components/AudioList.vue'
import Forms from '../components/Forms.vue'
import Footer from '../components/Footer.vue'

export default {
  name: 'DoUseIt',
  data() {
    return{
      lists: [
        {id: 1, title: 'Timer name 1', time: '00:00:35', completed: false},
        {id: 2, title: 'Timer name 2', time: '00:00:47', completed: false},
        {id: 3, title: 'Timer name 3', time: '00:01:49', completed: false},
      ]
    }
  },
  methods: {
    removeAudiu(id) {
      this.lists = this.lists.filter(t => t.id !==id )
    }
  },
  addList(audiu) {
    this.lists.push(audiu)
           
  },
  components: {
   AudioList,
   Forms,
   Footer
  }
}
</script>