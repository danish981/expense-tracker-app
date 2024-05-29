<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <!-- a unique key has to be defined when rendering lists or data with v-for -->
    <!-- and instead of v-bind:key we can use :key attribute, its short and cleaner -->
    <li v-for="transaction in transactions" :key="transaction.id">
      {{ transaction.text }} <span>-$ {{ transaction.amount }} </span
      ><button class="delete-btn">x</button>
    </li>

    <!-- THE HARD CODED ELEMENTS -->
    <!-- class minus gives red border -->
    <!-- <li class="minus">
      Cash <span>-$400</span><button class="delete-btn">x</button>
    </li> -->

    <!-- class plus gives green border -->
    <!-- <li class="plus">
      Paycheck <span>$800</span><button class="delete-btn">x</button>
    </li> -->
  </ul>
</template>




<script>
// ! this is the options API being used, will be changed to the latest way later
export default {
  data() {
    return {
      transactions: [
        { id: 1, text: "Flower", amount: -20 },
        { id: 2, text: "Salary", amount: 300 },
        { id: 3, text: "Book", amount: -10 },
        { id: 4, text: "Camera", amount: 150 },
        { id: 5, text: "Phone", amount: 200 },
        { id: 6, text: "Rent", amount: -800 },
        { id: 7, text: "Laptop", amount: 1200 },
        { id: 8, text: "Food", amount: -50 },
        { id: 9, text: "Guitar", amount: 250 },
        { id: 10, text: "Car", amount: 10000 },
        { id: 11, text: "Bike", amount: 500 },
        { id: 12, text: "Shoes", amount: -30 },
        { id: 13, text: "TV", amount: 800 },
        { id: 14, text: "Vacation", amount: -2000 },
      ],
    };
  },
};
</script>

