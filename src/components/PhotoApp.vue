<template>
  <div class="grid">
       <input type="text" placeholder="Search"/>
    <div class="img-item">
    <div v-for="(item, index) in items" :key="index">
       
      <img :src="item.Url"/>
      <h2>{{item.Name}}</h2>
      <h2>{{item.Type}}</h2>
      <form v-on:submit.prevent="submitForm">
       <button type="submit">Delete</button>
      </form>
    </div>
    </div>
  </div>
</template>
 <script>
export default {
  name: "PhotoApp",
  data() {
    return {
      items: [
        {
          Name: "John Frusciante",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Reservoir Dogs",
          Type: "movie",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Foo Fighters",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Pearl Jam",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Sublime",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Inglourious Basterds",
          Type: "movie",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Incubus",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Audioslave",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Jackie Brown",
          Type: "movie",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Nirvana",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "The Big Lebowski",
          Type: "movie",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Goodfellas",
          Type: "movie",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Guns N' Roses",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Death Proof",
          Type: "movie",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "The Offspring",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Django Unchained",
          Type: "movie",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Rage Against The Machine",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Snatch",
          Type: "movie",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Trainspotting",
          Type: "movie",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        },
        {
          Name: "Weezer",
          Type: "music",
          Url:
            "http://static.tvmaze.com/uploads/images/original_untouched/60/151357.jpg"
        }
      ]
    };
  },
  methods: {
      submitForm() {
      this.clearForm();
    },
       deleteButton(index) {
    //   this.$emit('Delete')
      this.item.splice(index, 1);
    }
  }
}
</script> 
<style scoped>
.grid img {
   width: 400px;
   height: 400px;
}

.img-item {
    display: grid;
    grid-template-columns: auto auto auto;
    column-gap: 10px;
    row-gap: 10px;
}
input {
    margin: 1em;
    width: 50%;
    padding: .5em;
    font-size: 1.2em;
}
</style> 
   