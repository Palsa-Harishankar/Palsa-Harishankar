<template>
  <div id="div1">
    <h1>Simple Form</h1>

    <form>
      <label>Email</label>
      <input
        v-model="form.email"
        class="input"
        type="email"
        placeholder="Enter Your Email"
        required
      />
      <br /><br />
      <label>password</label>
      <input
        class="input"
        type="password"
        placeholder="Enter Your Password"
        required
        v-model="form.password"
      /><br /><br />
      <select v-model="form.country">
        <option>INDIA</option>
        <option>USA</option>
      </select>
      <br /><br />
      <h3>Gender</h3>
      <label>Male</label>
      <input
        class="radio"
        type="radio"
        name="gender"
        value="male"
        v-model="form.gender"
      />

      <label>Female</label>

      <input
        class="radio"
        type="radio"
        name="gender"
        value="female"
        v-model="form.gender"
      />
      <br />
      <h3>Technology</h3>
      <label>Java</label>
      <input
        class="check"
        type="checkbox"
        value="java"
        v-model="form.technology"
      />
      <label>.Net</label>
      <input
        class="check"
        type="checkbox"
        value=".net"
        v-model="form.technology"
      />
      <label>Vue.js</label>
      <input
        class="check"
        type="checkbox"
        value="vue.js"
        v-model="form.technology"
      />

      <br /><br />
      <button class="loginbutton" v-on:click="login()" type="button">
        Login
      </button>
      <button class="resetbutton" type="reset">reset</button>
    </form>
  </div>
  <p>{{ form }}</p>
</template>
<script>
export default {
  data() {
    return {
      form: {
        email: "",
        password: "",
        country: "",
        gender: "",
        technology: [],
      },
    };
  },

  methods: {
    login() {
      console.warn(this.form);
    },
  },
};
</script>
<style>
.loginbutton,
.resetbutton {
  color: rgb(0, 0, 0);
  background-color: rgb(153, 219, 173);
  margin-left: 120px;
  margin-top: 30px;
  width: 60px;
  height: 30px;
  border-radius: 5px 3px;
  cursor: pointer;
  display: inline-block;
  margin: 20px;
}
.resetbutton {
  background-color: rgb(216, 138, 138);
}
.check,
.radio {
  margin-left: 120px;
  margin-top: 30px;

  display: inline-block;
  margin: 20px;
}
.input {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
}
form {
  max-width: 420px;
  margin: 30px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}
label {
  color: #aaa;
  display: inline-block;
  margin: 25px 0 15px;
}
h1 {
  color: rgb(8, 87, 87);
  font: 3.6em sans-serif;
  width: 100%;
  margin-top: 20px;
  margin-right: 8px 0;
  text-align: center;
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}
#div1 {
  border: solid black 2px;
  justify-items: centers;
}
</style>
