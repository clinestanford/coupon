<template>
  <div class="hello">
    <img src="https://media.giphy.com/media/pa83tvcKjgQUM/giphy.gif">
    <div class="coupon">
      <h3>Congratulations! You have received a coupon!</h3>
      <h4>Redemption Code: {{ uuid }}</h4>
      <h5>This coupon entitles the owner to one free dinner at the time of their convenience</h5>
      <h5>Directions for redemption:</h5>
      <ol>
        <li>take a screenshot of this webpage</li>
        <li>when time allows attach screenshot in text message and send it to whomever shared the link</li>
      </ol>
    </div>
    <p>Terms and conditions may apply ©Stanford Cline</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      uuid: this.uuidv4()
    }
  },
  methods: {
    logUser: function() {
      console.log("hit the endpoint");
    },
    uuidv4: function() {
      return 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
        var r = Math.random() * 16 | 0, v = c == 'x' ? r : (r & 0x3 | 0x8);
        return v.toString(16);
      });
    }
  },
  created() {
    this.logUser();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  text-align: left;
  padding: 0;
}
li {
  text-align: left;
}
.coupon {
  border: 2px dashed gray;
  background-color: lightgray;
  width: 75%;
  display: inline-block;
}
a {
  color: #42b983;
}
</style>
