<template>
  <div class="item-container">
    <img :src="items.image" alt="Item Image" class="item-image" />
    <div class="item-details">
      <h3><b>Item Name: {{ items.item_name }}</b></h3>
      <h4>Item Price: {{ items.price }}</h4>
      <h4>Quantity Left: {{ items.quantity }}</h4>
      <h4>Item Category: {{ items.category }}</h4>
      <h4>Likes for Item: {{ items.likes }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "DeliItem",
  props: {
    items: Object
  }
};
</script>

<style scoped>
.item-container {
  display: grid;
  grid-template-columns: 200px 1fr; 
  gap: 20px; 
  align-items: center; 
  background-color: #364d56;
  color: rgb(248, 242, 242);
  padding: 2em;
  text-align: left;
  width: 1000px;
  margin: auto;
  border-radius: 8px;
}


.item-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
  object-fit: cover;
}


.item-details {
  display: flex;
  flex-direction: column;
  gap: 8px; 
}

h3, h4 {
  
  margin: 0;
}
</style>
