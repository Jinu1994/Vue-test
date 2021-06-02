<template>
    <div id="child2">
        <div class="header">
            <slot name="header"></slot>
        </div>
        <div class="body">
            <slot name="body"></slot>
        </div>
    </div>
</template>
<style>
.header {
    margin:20px;
    background: beige;
    min-height: 50px;
}
.body{
    margin:20px;
    background: lightblue;
    min-height: 50px;
}
</style>

