<script setup>
const props = defineProps({
    incomes: { type: Number, required: true },
    expenses: { type: Number, required: true },
});

const formattedExpenses = (expense) => Math.abs(expense);
</script>

<template>
    <div class="inc-exp-container">
        <div>
            <h4>Income</h4>
            <p id="money-plus" class="money plus">+${{ incomes }}</p>
        </div>
        
        <div>
            <h4>Expense</h4>
            <p id="money-minus" class="money minus">-${{ formattedExpenses(expenses) }}</p>
        </div>
    </div>
</template>