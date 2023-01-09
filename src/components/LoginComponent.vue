<template>
  <div id="login">
      <h1>Login</h1>
      <div class="form-inputs">
          <label for="username">Username</label>
          <input type="text" id="username" name="username" placeholder="Username" />
      </div>
      <div class="form-inputs">
          <label for="password">Password</label>
          <input type="password" id="password" name="password" placeholder="Password" />
      </div>
      <button type="button" >Login</button>
  </div>
</template>

<script>
export default {
  name: 'LoginComponent'

}
</script>
