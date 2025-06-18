<template>
    <form>
        <label>Email: </label>
        <input type="email" required v-model="email" />
        <label>Password: </label>
        <input type="password" required v-model="password" />
        <label>Role:</label>
        <select v-model="role">
            <option value="developer" >Web Developer</option>
            <option value="designer">Web Designer</option>
        </select>
        <label>Skills:</label>
        <input type="text" v-model="TempSkill" @keyup="AddSkill"/>
        <div class="terms">
            <input type="checkbox" id="terms" required v-model="terms"/>
            <label for="terms">Accept Terms and Conditions</label>
        </div>
        <button type="submit">Submit</button>
    </form>
    <p>Role: {{role}}</p>
    <p>Email: {{ email }}</p>
    <p>Password: {{ password }}</p>
    <p>Skills: {{ skills.join(', ') }}</p>
    <p v-if="TempSkill">Current Skill Input: {{ TempSkill }}</p>
    <p v-if="terms">You have accepted the terms and conditions.</p>
</template>

<script>
export default {
  data () {
    return {
      email: '',
      password: '',
      role: 'None', // Default role
      terms: false,
      TempSkill: '',
      skills: []
    }
  },
  methods: {
    addSkill (e) {
      console.log(e)
    }
  }
}
</script>

<style>
 form{
    max-width: 420px;
    margin: 30px auto;
    background: white;
    text-align: left;
    padding: 40px;
    border-radius: 10px;
  }
  label, button {
    color: #2d2d30;
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
  }
  input, select {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
  }
  input[type="checkbox"] {
    display: inline-block;
    margin: 0px 10px 0 0;
    width: 16px;
    position: relative;
    margin-right: 10px;
    top: 2px;
  }
</style>
