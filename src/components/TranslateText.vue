<template>
  <div class="main-container">
    <div class="left-side">
      <div class="navbar">
        <ul class="navbar-list">
          <li>Detect Language</li>
          <li>English</li>
          <li>Español</li>
          <li>Français</li>
        </ul>
        <div class="dropdown">
          <button class="dropbtn"><span class="material-symbols-outlined">expand_more</span></button>
          <div class="dropdown-content">
              <a href="#">Português</a>
              <a href="#">Deutsch</a>
              <a href="#">Nederlandse</a>
              <a href="#">Svenska</a>
              <a href="#">Català</a>
              <a href="#">Polsky</a>
              <a href="#">Magyar</a>
              <a href="#">Русский</a>
              <a href="#">ελληνική</a>
          </div>
        </div>
      </div>
      <div class="text-container left">
        <textarea class="textarea" id="to-translate" type="text" name="to-translate" rows="6" v-model="message" @keyup="countCharacters()"></textarea>
        <div class="footer">
            <span class="footer-ele1 material-symbols-outlined">mic</span>
            <p class="footer-ele2">{{ totalcharacters }}/5000</p>
        </div>
      </div>
    </div>
    <div class="left-side">
      <div class="navbar">
        <ul class="navbar-list">
          <li>Detect Language</li>
          <li>English</li>
          <li>Español</li>
          <li>Français</li>
        </ul>
        <div class="dropdown">
          <button class="dropbtn"><span class="material-symbols-outlined">expand_more</span></button>
          <div class="dropdown-content">
            <a href="#">Português</a>
              <a href="#">Deutsch</a>
              <a href="#">Nederlandse</a>
              <a href="#">Svenska</a>
              <a href="#">Català</a>
              <a href="#">Polsky</a>
              <a href="#">Magyar</a>
              <a href="#">Русский</a>
              <a href="#">ελληνική</a>
          </div>
        </div>
      </div>
      <div class="text-container right">
        <textarea class="textarea" id="to-translate" type="text" name="to-translate" rows="6"></textarea>
        <div class="footer">
            <span class="footer-ele1 material-symbols-outlined">mic</span>
            <p class="footer-ele2">0/5000</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TranslateText',
  data() {
    return {
      message: '',
      totalcharacters: 0
    }
  },
  methods: {
    countCharacters () {
      this.totalcharacters = this.message.length;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main-container {
  margin: 0 auto;
  display: flex;
  border: 1px solid #bbb;
  border-radius: 8px;
  width: 1260px;
  height: 225px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
}

.left-side {
  margin: 0;
  height: 100%;
  width: 50%;
  background-color: white;
  border-radius: 4px 0 0 4px;
}

.navbar {
  display: flex;
  height: 60px;
  border-bottom: 1px solid #bbb;
}

.navbar-list {
  width: 580px;
  margin: 0;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.navbar-list li {
  font-weight: bold;
  font-size: 16px;
  color: #666
}

h3 {
  margin: 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.dropbtn {
    height: 60px;
    width: 60px;
    background-color: #fff;
    padding: 8px;
    border: none;
}

.dropbtn img {
    opacity: 0.6;
    width: 24px;
    height: auto;
}

.dropdown {
    position: relative;
    display: inline-block;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f1f1f1;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 3;
}

.dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}

.dropdown-content a:hover {background-color: #ddd;}

.dropdown:hover .dropdown-content {display: block;}

.dropdown:hover .dropbtn {background-color: #bbb;}

.material-symbols-outlined {
  color: #666;
  font-variation-settings:
  'FILL' 0,
  'wght' 400,
  'GRAD' 0,
  'opsz' 48
}

.left {
  border-right: 1px solid #bbb;
}

.textarea {
  width: 561px;
  height: 70px;
  margin: 30px auto 0;
  border: none;
  font-size: 24px;
  color: #333;
  resize: none;
}

.textarea:focus {
  outline: none;
}

.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-ele1 {
  margin-left: 30px;
}
.footer-ele2 {
  margin-right: 30px;
  font-size: 12px;
}

</style>
