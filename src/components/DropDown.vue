<template>
  <div>
    <button @click="toggle()" class="dropdown-button" ref="button">Menu</button>
  <div v-if="isOpen" v-outside-click="{exclude: ['button'],
    handler: 'close'}" class="dropdown-body">
      <ul>
        <li>Account Settings</li>
        <li>Notifications</li>
        <li>Log Out</li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Dropdown',
  data() {
    return {
      isOpen: false,
      }
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    },
    close() {
      this.isOpen = false;
    }
  }
}
</script>
<style scoped>
button {
  margin: 0 auto;
  border: 2px solid #42b983;
  width: 100px;
  height: 30px;
  border-radius: 10px;
  cursor: pointer;
}
.dropdown-body {
  width: 200px;
  border: 1px solid #42b983;
  background: #FFFFFF;
  margin: 5px auto;
}

ul li {
  list-style: none;
  text-align: left;
}
</style>