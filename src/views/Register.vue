<template>
  <div class="split-screen">
    <div class="left">
      <section class="copy">
        <!-- Gambar di pojok kiri atas -->
        <!-- <img src="/src/assets/kkclogo.jpg" class="imgtop" alt="Logo Atas" /> -->
      </section>
    </div>
    <div class="right">
      <form>
        <section class="copy">
          <h2>Daftar</h2>
        </section>
        <div class="input-container name">
          <input id="username" name="username" type="text" placeholder="Username" />
        </div>
        <div class="input-container name">
          <input id="nama" name="nama" type="text" placeholder="Nama" />
        </div>
        <div class="input-container role">
          <select id="role" name="role">
            <option value="" disabled selected>Role</option>
            <option value="admin">Admin</option>
            <option value="user">User</option>
          </select>
        </div>
        <div class="input-container password">
          <input id="password" name="password" type="password" placeholder="Password" />
          <i class="fa fa-eye-slash"></i>
        </div>
        <div class="input-container password">
          <input id="confirm_password" name="confirm_password" type="password" placeholder="Confirm Password" />
          <i class="fa fa-eye-slash"></i>
        </div>
        <button class="signup-btn" type="submit"><router-link to="/Login">Daftar</router-link></button>
        <!-- Gambar di pojok kiri bawah -->
        <img src="/src/assets/fitxcoe.jpg" class="imgbottom" alt="Logo Bawah" />
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Register',
};
</script>


<style lang="scss" scoped>
body {
  padding: 0;
  margin: 0;
  font-weight: 500;
}

h1 {
  font-size: 2.25rem;
  font-weight: 700;
}

h2 {
  text-align: left;
  padding-bottom: 1.4rem;
  font-size: 1.8rem;
  font-weight: 700;
}

a {
  text-decoration: none;
  color: var(--primary-blue);
}

a:hover {
  text-decoration: none;
}

.split-screen {
  display: flex;
  flex-direction: column;
}

.left {
  height: 200px;
}

.left,
.right {
  display: flex;
  justify-content: center;
  align-items: center;
}

/* BG IMAGE */
.left {
  background: linear-gradient(rgba(247, 228, 85, 0.5), rgba(223, 186, 21, 0.9)),
    url('/src/assets/bg.jpg');
  background-size: cover;
}

.right .copy {
  color: black;
  text-align: center;
}

.right .copy p {
  margin: 1.5em 0;
  font-size: 0.875rem;
}
.right form {
  width: 328px;
}

/* BOX INPUT FORM */
form input[type='text'],
form input[type='email'],
form input[type='password'],
form select {
  display: block;
  width: 100%;
  box-sizing: border-box;
  border-radius: 8px;
  border: 2px solid var(--outline);
  padding: 1em;
  margin-bottom: 1.25rem;
  font-size: 0.875rem;
}

label {
  display: block;
  margin-bottom: 0.5rem;
  font-size: 0.75rem;
}

.input-container.password {
  position: relative;
}

.input-container.password i {
  position: absolute;
  top: 42px;
  right: 16px;
}

/* TOMBOL DAFTAR */
.signup-btn {
  display: block;
  width: 100%;
  background: var(--black);
  color: var(--white);
  font-weight: 700;
  border: none;
  padding: 1rem;
  border-radius: 14px;
  font-size: 0.9rem;
  letter-spacing: 0.1rem;
  transition: 0.3s;
}

.signup-btn:hover {
  background: var(--green-kkc);
  cursor: pointer;
}

.login-container {
  padding-top: 1.4rem;
  text-align: center;

  strong {
    color: var(--blue-coe);
  }
}

.right {
  .imgtop, .imgbottom {
  width: 250px;
  max-width: 100%;
  height: auto;
  margin-top: 3rem;
  margin-left: 2.4rem;
}
}

/* RESPONSIVE PAGE SETT */
@media screen and (min-width: 900px) {
  .split-screen {
    flex-direction: row;
    height: 100vh;
  }
  .left,
  .right {
    display: flex;
    width: 50%;
    height: auto;
  }
}
</style>
