<template>
  <div class="row">
    <div class="col-12">
      <ul class="list-group">
        <draggable v-model="myArray" @change="saveList" group="people" @start="drag=true" @end="drag=false">
          <li class="list-group-item my-1 border" v-for="item in myArray"
              :key="item.order"> {{item.name}} ({{item.order}})
          </li>
        </draggable>
      </ul>

    </div>

  </div>
</template>

<script>
    import draggable from 'vuedraggable'

    export default {
        components: {draggable},
        name: 'HelloWorld',
        data() {
            return {
                drag: true,
                myArray: [
                    {
                        "name": "Moawia",
                        "order": 0,
                    },
                    {
                        "name": "Secound",
                        "order": 1,
                    },
                    {
                        "name": "draggable",
                        "order": 2,
                    },
                    {
                        "name": "component",
                        "order": 3,
                    },
                    {
                        "name": "for",
                        "order": 4,
                    }
                ]
            }
        },
        props: {
            msg: String
        },
        methods: {
            saveList() {
                this.myArray.forEach((item, key) => {
                    this.myArray[key].order = key
                })
                console.table(this.myArray)
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .container {
    height: 2500px;
  }

  .card {
    padding: 10px;
    border: 1px solid #aaa;
    background: #fff;
    border-radius: 10px;
    margin-bottom: 10px;
    cursor: pointer;
    width: 250px;
  }
</style>
