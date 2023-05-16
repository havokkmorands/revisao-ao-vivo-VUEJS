<script setup>
    const props = defineProps(['operacao', 'num1', 'num2'])
</script>


<template>
        <div class="operation">
            <h2>Selecione a operação para o resultado</h2>
            <select @change="props.operacao">
                <option value="+">+</option>
                <option value="-">-</option>
                <option value="*">*</option>
                <option value="/">/</option>
            </select>
        </div>
        <div>
            <input @keyup="props.num1" required type="number" placeholder="Insira o número 1"/>
            <input @keyup="props.num2" required type="number" placeholder="Insira o número 2"/>
        </div>
</template>

<style scope>
    input {
        margin: 30px;
        padding: 4px;
        border-radius: 4px;
    }
</style>