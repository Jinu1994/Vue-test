<template>
    <div>
        <h5>Question 1</h5>
        <span>Original Price: {{originalPrice}}</span>
        <br>
        <span>Discount: {{discount}}</span>
        <br>
        <span>Selling Price: {{originalPrice - discount}}</span>
        <!-- render the data here using string interpolation -->
    </div>
</template>
<script>
export default {
    // update the model with data here
    data() {
    return {
        originalPrice : 200,
        discount : 100

        
    };
  }
}
</script>

