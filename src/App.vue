<script>
// import TheCounter from './components/TheCounter.vue'
import TheInput from './components/TheInput.vue'
import TheFreeInptBox from './components/TheFreeInptBox.vue'
import TheDateInput from './components/TheDateInput.vue'
import TheTime from './components/TheTime.vue'
import { v4 as uuidv4 } from 'uuid'
export default {
  components: {
    TheInput,
    TheFreeInptBox,
    TheDateInput,
    TheTime
  },
  data: () => ({
    todoList: [],
    parentCount: 10,
    thingsText: '',
    dateTime: '',
    timeslot: '',
    jsonRes: []
  }),

  methods: {
    increment() {
      return this.parentCount++
    },
    decrement() {
      return this.parentCount--
    },
    handleAdd() {
      this.todoList.push({
        id: uuidv4(),
        thing: this.thingsText,
        fullTime: this.dateTime + this.timeslot
      })
    },
    handleInput(event) {
      const name = event.target.name
      const value = event.target.value
      this[name] = value
    },
    handleDelete(id) {
      const updatedList = this.todoList.filter((item) => {
        return item.id !== id
      })
      this.todoList = updatedList
    }
  },
  created() {
    const apiCall = async () => {
      const resp = await fetch('https://jsonplaceholder.typicode.com/posts')
      const res = await resp.json()
      this.jsonRes = res
    }
    apiCall()
  },
  Mounted() {
    console.log(jsonRes)
  },
  watch: {
    //watch a state change
    async thingsText(newValue, oldvalue) {
      //watch the dependency "thingsText" variable, if newValue !=oldValue, then execute function
      //new Value,old Value

      const resp = await fetch('https://jsonplaceholder.typicode.com/posts')
      const res = await resp.json()
      console.log(res)
      this.jsonRes = res
    }
  }
}
</script>

<template>
  <h1 class="Text">Hello World</h1>
  <div class="parent_btn_gp">
    <!--tried pass a props to child component -->
    <!-- <TheCounter :parentCount="parentCount" :parentIncrement="increment" /> -->
    <!-- <button class="parentIncrement" @click="increment">Parent Increment</button> -->
    <!-- <button class="parentDecrement" @click="decrement">Parent Decrement</button> --->
  </div>
  <!--  -->
  <section>
    <TheInput />
  </section>
  <section class="todoContainer">
    <div class="innerContainer">
      <h1>備忘錄</h1>
      <TheFreeInptBox @handle-input-emit="handleInput" />
      <TheDateInput :handleInput="handleInput" />
      <TheTime :handleInput="handleInput" />
      <button class="AddBtn" @click="handleAdd">新增</button>
    </div>

    <div class="todoList" v-for="todo in todoList" :key="todo.id">
      <div class="todolist-inner">
        <div>{{ todo.thing }}</div>
        <div><button class="deleteBtn" @click="handleDelete(todo.id)">Delete</button></div>
      </div>

      <div>{{ todo.fullTime }}</div>
    </div>
  </section>
  <section>
    <div class="res" v-for="post in jsonRes" :key="post.id">
      <div>{{ post.title }}</div>
    </div>
  </section>
</template>

<style scoped>
.res {
  text-align: center;
  min-width: 10px;
  border: 1px solid orange;
}
.todoContainer {
  margin: 4rem auto;
  width: 300px;
  height: auto;
  border: solid 1px;
}
.innerContainer {
  margin: 15px;
  border: solid 1px green;
}
.todoList {
  margin: 15px;
}
.todoList-inner {
  display: flex;
  justify-content: space-between;
}
.AddBtn {
  background-color: black;
  color: white;
}
.deleteBtn {
  background-color: red;
}
.Text {
  text-align: center;
}
.parent_btn_gp {
  text-align: center;
}
.parentDecrement {
  background-color: aquamarine;
}
.parentIncrement {
  background-color: blueviolet;
}
</style>
