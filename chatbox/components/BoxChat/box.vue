<template>
  <div id="card" class="card text-center login">
    <!-- header -->
    <div id="card-header" class="card-header">
      CHAT CHAT
    </div>

    <!-- body -->
    <div id="card" class="card-body">
      <div v-for="(mess, index) in messengers" :key="index" :value="mess">
        <label id="nameLablel" class="col" for="name">{{ getNameAccount(mess.AccountsID) }} said:</label>
        <input
          id="form-control"
          class="form-control col"
          type="text"
          :value="mess.Content"
          readonly
        >
        <br>
      </div>
    </div>

    <!-- footer -->
    <div id="card-footer" class="card-footer text-muted">
      <div class="input-group mb-3">
        <input
          id="okee"
          type="text"
          class="form-control"
          placeholder="Nhập gì đó và ấn nút bên cạnh để gửi ..."
        >
        <div class="input-group-append">
          <button
            class="btn btn-outline-primary"
            type="button"
            @click="setMessenger()"
          >
            Send
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style>
html,
body {
  /* background-image: url("http://file.vforum.vn/hinh/2016/05/apple-ios-mountains-and-galaxy-wallpaper-1920x1080.jpg"); */
  background-size: 100%;
}
</style>
