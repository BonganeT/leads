<template>
  <div >
    <div class="container">
      <div class="drag">
        <h2>Leads</h2>
        <draggable v-model="list" class="dragArea" :options="{group:'people'}">
          <div :data-id="element.name" :data-name="element.name" @click="mama" v-for="element in list">{{element.name}}</div>
        </draggable>
      </div>

      <div class="drag">
        <h2>Scheduled</h2>
        <draggable v-model="list2" class="dragArea" :options="{group:'people'}">
          <div :data-id="element.name" :data-name="element.name" @click="mama" v-for="element in list2">{{element.name}}</div>
        </draggable>
      </div>

      <div class="drag">
        <h2>Progress</h2>
        <draggable v-model="list3" class="dragArea" :options="{group:'people'}">
          <div :data-id="element.name" :data-name="element.name" @click="mama" v-for="element in list3">{{element.name}}</div>
        </draggable>
      </div>

      <div class="drag">
        <h2>Done</h2>
        <draggable v-model="list4" class="dragArea" :options="{group:'people'}">
          <div :data-id="element.name" :data-name="element.name" @click="mama" v-for="element in list4">{{element.name}}</div>
        </draggable>
      </div>

    </div>


  </div>

</template>

<script>
import draggable from 'vuedraggable';

export default {
  data() {
    return {
      list: [{
        name: "John"
      }, {
        name: "Joao"
      }, {
        name: "Jean"
      }],
      list2: [{
        name: "Juan"
      }, {
        name: "Edgard"
      }, {
        name: "Johnson"
      }],
      list3: [{
        name: "Wole"
      }, {
        name: "Ayo"
      }, {
        name: "Emma"
      }],
      list4: [{
        name: "Yao"
      }, {
        name: "Kel"
      }, {
        name: "Life"
      }],
    }
  },
  methods: {
    mama(ev){
      console.log(ev.target.dataset);
    },
    add: function() {
      this.list.push({
        name: 'Juan'
      });
    },
    replace: function() {
      this.list = [{
        name: 'Edgard'
      }]
    }
  },
  components: {
    draggable
  }
}

</script>

<style lang="scss">

.container {
  display: flex;
  border: 1px solid;
  width: 100%;
  padding: 20px;
}

.drag {
  width: 20%;
  display: flex;
  flex-direction: column;
  padding: 20px

}
.dragArea {
  display: flex;
  flex-direction: column;
  border: 1px solid;
}

.dragArea div{
  background: #eee;
  padding: 12px;
  margin: 6px;
}

</style>
