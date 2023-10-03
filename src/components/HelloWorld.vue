<template>
  <div class="hello">
  <h1>{{ msg }}</h1>
      <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  };
  mounted() {
    <button id="btn">Duplicate</button>
  <button id="colorBtn">BGColorChanger</button>
  <button id="Headingbtn">HeadingChanger</button>
  <button id ="dltbtn">DeleteCard</button>
  
 <script>
  document.querySelector('#btn').addEventListener('click', function(e){
    const clone = document.querySelector('#card').cloneNode('card');
    document.body.appendChild(clone);
  })
</script>
  <script>
  var numbers = ["1", "2", "3", "4", "5", "6", "7", "8", "9"];
        var letters = ["A", "B", "C", "D", "E", "F"];
        function randomColor() {
            var color = "";
            for (var i = 0; i < 3; i++) {
                var index = Math.floor(Math.random() * (numbers.length + letters.length));
                color += (index < numbers.length) ? numbers[index] : letters[index - numbers.length];
            }
            return color;
        }
        document.querySelector('#colorBtn').addEventListener('click', function (e) {
            const card = document.querySelector('.card');
            // Check the current background color
            const currentColor = card.style.backgroundColor;
            // Change background color
            card.style.backgroundColor = '#' + randomColor();
        });
    </script>
  <script>
    //HEADING CHANGER
    document.querySelector('#Headingbtn').addEventListener('click', function(e){
      const title = document.querySelector('h2');
      title.innerText = "Super Pod 2 Realty";
    })
  </script>
  <script>
    //card delete
    document.querySelector('#dltbtn').addEventListener('click', function(e){
      const cards = document.querySelectorAll('.card');
      //GPT Assist:
      // Check if there are cards to delete
    if (cards.length > 2) {
        const lastCard = cards[cards.length - 1];
        lastCard.parentNode.removeChild(lastCard);}
    })
  </script>
  <script>
    var original= document.querySelector('#description').innerText;
document.querySelector('#detailsBtn').addEventListener('click', function(e) {
    const description = document.querySelector('#description');
    // Toggle the visibility of the description
    if (description.innerText === 'none' || description.innerText=== '') {
        description.innerText = original; // Show the description
    } else {
        description.innerText = ''; 
    }
});
  }}
</script>
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
</style>
