<template lang="html">
  <div class="con-select-example">
    <vs-select
      class="selectExample"
      label="Default"
      v-model="select1"
      >
      <vs-select-item :key="index" :value="item.value" :text="item.text" :icon="item.icon" v-for="item,index in options1" />
    </vs-select>
    <vs-select
      class="selectExample"
      label="Multiple"
      multiple
      v-model="select2"
      >
      <vs-select-item :key="index" :value="item.value" :text="item.text" :icon="item.icon" v-for="item,index in options2" />
    </vs-select>
    <vs-select
      autocomplete
      class="selectExample"
      label="Autocomplete"
      v-model="select3"
      >
      <vs-select-item :key="index" :value="item.value" :text="item.text" :icon="item.icon" v-for="item,index in options3" />
    </vs-select>
  </div>
</template>

<script>
export default {
  name:'',
  data(){
    return {
      select1:2,
      select2:[1,3,4,6],
      select3:4,
      options1:[
        {text:'Edit',value:1,icon:'edit'},
        {text:'Delete',value:2,icon:'delete'},
        {text:'Nothing',value:3},
      ],
      options2:[
        {text: 'Play', value: 1},
        {text: 'Pause', value: 2, icon: 'pause'},
        {text: 'Replay', value: 3, icon: 'replay'},
        {text: 'Rewind', value: 4},
        {text: 'Playlist', value: 5},
        {text: 'Tv', value: 6, icon: 'tv'},
        {text: 'Video Library', value: 7, icon: 'video_library'},
        {text: 'Queue', value: 8},
        {text: 'Fast forword', value: 9, icon: 'fast_forward'},
        {text: 'Fast rewind', value: 10, icon: 'fast_rewind'},
        {text: 'Record', value: 11},
        {text: 'Freeze', value: 12}
      ],
      options3:[
        {text:'North',value:1,icon:'north'},
        {text:'West',value:2,icon:'west'},
        {text:'East',value:3,icon:'east'},
        {text:'South',value:4,icon:'south'},
        {text:'Nowhere',value:5},
      ]
    }
  }
}
</script>

<style lang="css">
.selectExample {
  margin: 10px;
}
.con-select-example {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap
}
.con-select .vs-select {
  width: 100%
}
@media (max-width: 550px) {
  .con-select {
    flex-direction: column;
  }
  .con-select .vs-select {
    width: 100%
  }
}
</style>
