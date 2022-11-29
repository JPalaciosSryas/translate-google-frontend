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
        </div>
        <div class="right-side">
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
        </div>
        <div class="browser-container">
            <div class="web-browser">
                <input type="text" id="web" name="web" required/>
                <span class="floating-label">Web Sites</span>
                <label for="web"><span class="material-symbols-outlined">arrow_forward</span></label>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'WebSites',
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

<style scoped>
.main-container {
  margin: 0 auto;
  display: flex;
  border: 1px solid #bbb;
  border-radius: 8px;
  width: 1260px;
  height: 260px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
}

.left-side, .right-side {
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

.browser-container {
  width: inherit;
  margin: 120px auto;
  position: absolute;
}

.web-browser {
  margin: 0 auto;
  width: 900px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.web-browser h1 {
  font-size: 24px;
  margin-bottom: 16px;
  color: #111;
}

.web-browser p {
  color: #666;
  font-size: 15px;
  font-weight: 600;
  margin-bottom: 32px;
}

.web-browser a {
  color: #1a73e8;
  text-decoration: none;
}

.input {
  display: block;
}

.web-browser input[type="text"] {
    border: 2px solid #1a73e8;
    border-radius: 8px;
    width: 540px;
    height: 24px;
    font-size: 16px;
    padding: 12px;
}

.web-browser input[type="text"] {
    border: 1px solid #666;
    border-radius: 8px;
    width: 540px;
    height: 24px;
    font-size: 16px;
    padding: 12px;
}

.web-browser input[type="text"]:focus {
    outline: none;
    border: 2px solid #1a73e8;
    border-radius: 8px;
    width: 540px;
    height: 24px;
    font-size: 16px;
    padding: 12px;
}

.web-browser input[type="text"]:focus ~ .floating-label,
.web-browser input[type="text"]:not(:focus):valid ~ .floating-label {
  top: 2px;
  margin-top: -14px;
  bottom: 6px;
  font-size: 11px;
  opacity: 1;
  background-color: #fff;
  padding: 2px;
  color:  #1a73e8;
}

.floating-label {
  height: 30px;
  margin-top: -4px;
  margin-right: 532px;
  position: absolute;
  pointer-events: none;
  top: 18px;
  transition: 0.2s ease all;
}

.web-browser label {
  margin-left: 16px;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  padding: 11px 11px;
  background-color: #1a73e8;
  cursor: pointer;
  font-weight: bold;
}
.material-symbols-outlined {
  color: #ddd;
  font-variation-settings:
  'FILL' 0,
  'wght' 400,
  'GRAD' 0,
  'opsz' 48
}

</style>