 <script setup>
    import { ref, defineProps, defineEmits, onMounted } from 'vue';
    const StarWarsOwen = {
      // The code for the StarWarsOwen component goes here
    };
  
    const emit = defineEmits(['bigError']);
    const starWarsData = ref(null);
  
    // Props
    const { id } = defineProps(['id']);
  
    // Function to fetch data from SWAPI
    const fetchStarWarsData = async () => {
      try {
        if (id) {
          // Fetch data based on the provided id prop
          const response = await fetch(`https://swapi.dev/api/people/${id}/`);
          if (!response.ok) {
            throw new Error('Failed to fetch data');
          }
          const data = await response.json();
          starWarsData.value = data;
        }
        // Add logic for other cases if needed
      } catch (error) {
        emit('bigError', error.message);
      }
    };
  
    // Fetch the data on component mount
    onMounted(() => {
      fetchStarWarsData();
    });
  </script>
  
  <template>
      <!-- Display SWAPI DATA -->
      <div v-if="starWarsData">
        <h1>Star Wars Owen</h1>
        <h3>Star Wars Character: {{ starWarsData.name }}</h3>
        <p>Birth Year: {{ starWarsData.birth_year }}</p>
        <p>Height: {{ starWarsData.height }}</p>
        <p>Mass: {{ starWarsData.mass }}</p>
        <p>Hair Color: {{ starWarsData.hair_color }}</p>
        <p>Skin Color: {{ starWarsData.skin_color }}</p>
        <p>Eye Color: {{ starWarsData.eye_color }}</p>
      </div>
  </template>