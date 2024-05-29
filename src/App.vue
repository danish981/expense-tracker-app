<template>
  <Header />
  <div class="container">
    <Balance />
    <IncomeExpenses />
    <!-- passing the transactions array to the component as props from this App.vue parent component to the TransactionList child component -->
    <TransactionList :transactions="transactions" />
    <AddTransaction />
  </div>
</template>


<!-- we dont have to export the components when we are using setup script, just import and use them in the template -->
<script setup>
import Header from "./components/Header.vue";
import Balance from "./components/Balance.vue";
import IncomeExpenses from "./components/IncomeExpenses.vue";
import TransactionList from "./components/TransactionList.vue";
import AddTransaction from "./components/AddTransaction.vue";

import { ref } from "vue";

// todo : we want this array to be reactive
const transactions = ref([
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
]);
</script>