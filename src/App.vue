<template>
 <div>
  <h1>Rick and Morty</h1>
  <FilterByStatu/>
  <ListCharacters />
  <FilterByName/>
 </div>
</template>

<script>
import ListCharacters from './components/ListCharacters';
import FilterByStatu from './components/FilterByStatu';
import FilterByName from './components/FilterByName';

export default {
  components: {
    FilterByStatu,
    ListCharacters,
    FilterByName
  }
}
</script>

<style lang="scss">
.character{
  background-color: var(--background-card);
  border-radius: 20px;
  box-shadow: 0 0 10px 1px var(--background-body);
  overflow: hidden;
  cursor: pointer;
  transition:transform 200ms ease-in-out;
  height:100%;
  &:hover{
    transform: scale(1.05);
    h3{
      color:var(--text-orange);

    }
  }
  span{
    color: var(--text-gray);
  }
  h3{
    margin-bottom: 0.5rem;
  }
  &__info{
    padding:1.5rem;
    .status{
      display:flex;
      align-items: center;
      margin-bottom:0.5rem;
      span{
        color:var(--text-gray);
        &:first-child{
          width: 10px;
          height: 10px;
          border-radius: 50%;
          margin-right: 0.5rem;
        }
      }
      .alive{
        background-color: green;
      }
      .dead{
        background-color: red;
      }
      .default{
        background-color: white;
      }
    }
    .origen{
      margin-bottom: 0.5rem;
    }
  }
}
</style>
