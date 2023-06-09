<template>
    <div>
        <h2>About</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
            Nobis aut similique, quia ipsa, ducimus molestiae voluptatibus ex cupiditate vero ullam distinctio magni placeat repellendus illum aliquid quae, officia veniam quo laborum saepe! Dolorum quisquam eos nam.
             Error laboriosam, autem voluptatum provident harum reiciendis. 
             Quia consequuntur nihil quis quae mollitia autem corporis, non aperiam reprehenderit atque fuga quo, asperiores porro quibusdam laborum magnam? Earum, enim numquam.
              Sit dignissimos, praesentium eum, minus id excepturi doloribus tenetur vitae ipsam molestiae magnam quo nesciunt modi autem corrupti eaque accusamus doloremque, assumenda numquam aspernatur cumque inventore esse iusto placeat? 
              Inventore quisquam voluptatem perspiciatis adipisci ut!</p>
              <div>{{data}}</div>
    </div>
</template>

<script setup>
const {data}=await useFetch('/api/ninja?name=mario')
 

</script>

<style scoped>
h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

p {
    margin: 20px 0;
}</style>