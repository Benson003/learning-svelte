<script>
let people = [
  {name:'yoshi',age:35,id:1, beltColor:'black'},
  {name:'lugi',age:40,id:2, beltColor:'red'},
  {name:'mario',age:45,id:3, beltColor:'blue'}
]

const handleClick = (id) =>{
  people = people.filter((person) => person.id != id)
}
</script>

<main>
  {#each people as person(person.id)}
     <div>
      <h3>{person.name} is a {person.beltColor} belt</h3>
      <button on:click={()=> {handleClick(person.id)}}>delete</button>
     </div>
  {/each}

</main>

<style>
</style>
