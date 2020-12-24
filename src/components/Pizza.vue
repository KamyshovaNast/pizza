<template>
    <div id="pizza">
        <h2>Название: {{pizzaName}}</h2>
        <p><b>Цена</b>: {{pizzaPrice}}</p>
        <p><b>Размер</b>: {{pizzaSize}}</p>
        <p><b>Состав</b>:
            <slot></slot>
        </p>
    </div>
</template>

<script>
export default {
    props: ['pizzaName','pizzaPrice', 'pizzaSize']   
}
</script>

<style>
#pizza {
    width: 400px;
    padding: 30px;
    background-color: white;
    border-radius: 20px;
    box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
}
</style>