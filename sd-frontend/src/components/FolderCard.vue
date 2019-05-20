<template>
    <!-- Folder Card -->
    <div class="column" :class="[generateCardSize]">
        <div class="card">
          <span class="card-loader" v-if="value != displayValue && valueSent == true"><loader-icon class="spinner"></loader-icon></span>
          <span class="dot" :class="{'active': activity}"></span>
          <div class="card-content has-text-centered">
            <header><h5>{{name}}</h5></header>
            
            <h2>{{displayValue}}</h2>
          </div>
        </div>
    </div>
</template>

<script>
    import { LoaderIcon } from 'vue-feather-icons'
    import EventBus from '@/event-bus.js';
    import { setTimeout } from 'timers';
    
    export default {
        props:['id', 'name' , 'type', 'value'],
        
       components: {
           
            LoaderIcon
        },

        data () {
          return {
            activity: true,
            msg:"",
            displayValue: this.value,
            valueSent: false
          }
        },

        watch: {
          value:function() {
              this.displayValue = this.value;
              this.valueSent = false;
              this.activity = true;
              setTimeout(() => {this.activity = false}, 100);
          } 
        },

        methods: {
          sendValue() {
              this.msg = {
                "id": this.id,
                "value": this.displayValue
              };
              
              EventBus.$emit('folderChanged', this.msg);
              this.valueSent = true;
              this.activity = true;
              setTimeout(() => { this.activity = false }, 100);                
          }
       },

       computed:{
        generateCardSize:function(){
          if (this.type == 2) {
            return "is-4";
          }else if (this.type == 3) {
            return "is-4";
          }else{
            return "is-2";
          }
        },

        
       },

       mounted(){
          setTimeout(() => { this.activity = false }, 500);
       }
    }
</script>

<style>

</style>
