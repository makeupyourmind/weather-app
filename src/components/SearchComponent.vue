<template>
  <form @submit.prevent="$emit('fetch-weather-for-city', city)">
    <input type="search" v-model="city" placeholder="Location" />
  </form>
</template>

<script>
export default {
  name: "SearchComponent",
  data: () => ({
    city: null,
  }),
};
</script>

<style lang="scss" scoped>
a {
  color: #69c;
  text-decoration: none;
}
a:hover {
  color: #f60;
}
h1 {
  font: 1.7em;
  line-height: 110%;
  color: #000;
}
p {
  margin: 0 0 20px;
}

input {
  outline: none;
}
input[type="search"] {
  font-family: inherit;
  font-size: 100%;
}

input[type="search"] {
  background: #ededed
    url(https://static.tumblr.com/ftv85bp/MIXmud4tx/search-icon.png) no-repeat
    9px center;
  border: solid 1px #ccc;
  padding: 9px 10px 9px 32px;
  width: 150px;

  border-radius: 10em;

  transition: all 0.5s;
}
input[type="search"]:focus {
  width: 200px;
  background-color: #fff;
  border-color: #66cc75;
  box-shadow: 0 0 5px rgba(109, 207, 246, 0.5);
}

input:-moz-placeholder {
  color: #999;
}
input::-webkit-input-placeholder {
  color: #999;
}
</style>
