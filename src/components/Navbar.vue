<template>
<div>
    <nav>
        <ul>
            <ol>
                <li><a href="#"></a>Home</li>
                <li><a href="#"></a>Home</li>
                <li><a href="#"></a>Home</li>
                <li><a href="#"></a>Home</li>
            </ol>
        </ul>
    </nav>
</div>
</template>


<script>
export default {
  name: 'Navbar',
  props: {
    msg: String
  }
}


</script>

<style>

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