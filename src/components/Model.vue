<template>
    

    <div class="backdrop">
        <div class="backdrop" @click.self="closeModel">
        <div class="model" :class="{sale: theme === 'sale'}">
            <slot></slot>
            <div class="actions">
                <slot name="links"></slot>
            </div>
            </div>
            <div id="nav">
            <router-link to="/">Home</router-link>
            </div>
            <h1>Model Heading</h1>
            <h2> {{header}} </h2>
            <h2> {{text}} </h2>
            <p>Paragraph Content...</p>
        </div>
    </div>
</template>

<script>
export default {
    // props: ['header', 'text']
    props: [],
 
    methods: {
      closeModel() {
      this.$emit('close')
    }
    }
}
</script>


<style>
.model {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: #ffffff;
    border-radius: 10px;
}

.backdrop {
    top: 0;
    position: fixed;
    background: #d4cfcf38;
    width: 100%;
    height: 100%;

}

.model p {
    font-style: normal;
}

.model.sale {
    background: rgb(36, 180, 36);
    color: blue;
}

.model.sale h1 {
    color: white;
}
</style>