<template>
  <div class="character">
    <img :src="character.image" alt="character.name">
    <div class="character__info">
        <h3>{{ character.name }}</h3>
        <div class="status">
            <span 
                :class="
                    character.status=='Alive' ? 'alive':
                    character.status=='Dead' ? 'dead':
                    'default'
                "
            ></span>
            <span>{{ character.status }}-{{ character.species}}</span>
        </div>
        <div class="origin">
            <span>
                Origin:
                {{ character.origin.name }}
            </span>
        </div>
        <div class="location">
            Location:
            {{ character.location.name }}
        </div>
    </div>
  </div>
</template>

<script>
export default {
    props:['character']
}
</script>

<style>
:root{
    --background-body:#24282f;
    --background-card:#3c3e44;
    --text-white:#FFFFFF;
    --text-gray:#c0c0c0;
    --text-orange:#ff9800;

}
*{
    box-sizing: border-box;
    margin:0;
    padding:0;

}
body{
    background-color: var(--background-body);
    color: var(--text-white);
    font-family: 'Segoe UI', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
h1{
    margin-bottom: 3rem;
    text-align: center;
}
.container{
    width: 980px;
    max-width: 90%;
    margin: 5rem auto;
}
img{
    width: 100%;
}
</style>