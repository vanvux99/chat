<template>
  <div class="card text-center login" id="card">
    <!-- header -->
    <div class="card-header" id="card-header">CHAT CHAT</div>

    <!-- body -->
    <div class="card-body" id="card">
      <div v-for="(mess, index) in messengers" :key="index" :value="mess">
        <label class="col" id="nameLablel" for="name">{{ getNameAccount(mess.AccountsID) }} said:</label>
        <input
          class="form-control col"
          id="form-control"
          type="text"
          :value="mess.Content"
          readonly
        />
        <br />
      </div>
    </div>

    <!-- footer -->
    <div class="card-footer text-muted" id="card-footer">
      <div class="input-group mb-3">
        <input
          type="text"
          id="okee"
          class="form-control"
          placeholder="Nhập gì đó và ấn nút bên cạnh để gửi ..."/>
        <div class="input-group-append">
          <button
            class="btn btn-outline-primary"
            type="button"
            @click="setMessenger()">
            Send
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
html,
body {
  background-image: url("http://file.vforum.vn/hinh/2016/05/apple-ios-mountains-and-galaxy-wallpaper-1920x1080.jpg");
  background-size: 100%;
}
</style>
