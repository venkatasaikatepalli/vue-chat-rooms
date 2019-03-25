<template>
  <div class="home">
    <h1>Socket</h1>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'home',
  sockets: {
    connect: function () {
      console.log('socket connected');
      this.$socket.emit('register', { email: 'venkatasaisoft@gmail.com' });
    },
    message: function (data) {
      console.log('this method was fired by the socket server. eg: io.emit("customEmit", data)');
      console.log(data);
    },
  }
};
</script>
