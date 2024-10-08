<script setup>
const menuItems = [
  {
    id: 1,
    name: "Cappucino",
    price: 4.5,
    img: "https://images.immediate.co.uk/production/volatile/sites/30/2020/08/cappucino-32dbfba.jpg",
  },
  {
    id: 2,
    name: "Espresso",
    price: 3.5,
    img: "https://media.istockphoto.com/id/1126871442/es/foto/taza-de-caf%C3%A9.jpg?s=1024x1024&w=is&k=20&c=4yZsqvhd-3l3KhdKM9_Y0SIDttHacHSoUgvCb9zxn8g=",
  },
  {
    id: 3,
    name: "Latte",
    price: 4.2,
    img: "https://images.pexels.com/photos/302896/pexels-photo-302896.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
  },
];
console.log(menuItems);
</script>

<template>
  <section class="menu">
    <h2>Our Menu</h2>
    <p>Explore our delicious offering</p>
    <!-- Using v-for directive to display the items-->
    <ul>
      <li v-for="item in menuItems" :key="item.id">
        <img v-bind:src="item.img" v-bind:alt="item.name" class="menu-image" />
        <div class="item-description">
          {{ item.name }} <br />
          ${{ item.price }}
        </div>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.menu {
  padding: 20px;
  background-color: #f7f7f7;
  color: black;
}

ul {
  list-style-type: none; /* remove bullet point point*/
  padding: 0;
  margin: 20px;
  display: flex;
  justify-content: space-evenly;
}

.menu-items {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}
.menu-image {
  width: 200px;
  height: 200px;
  margin-right: 15px;
  border: 1.5px solid rgb(95, 25, 25);
  border-radius: 50%;
}

.item-description {
  text-align: center;
  font-size: 1.1em;
}

.menu-image:hover {
  border: 4px solid rgb(95, 25, 25);
}
</style>
