<template>
  <section>
    <base-card>
      <h1>Notes</h1>
      <div>
        <base-button>Notları Görüntüle</base-button>
      </div>
      <ul>
        <note-result
          v-for="result in results"
          :key="result.id"
          :note="result.note"
          :onemlilikDerecesi="result.onemlilikDerecesi"
        >
        </note-result>
      </ul>
    </base-card>
  </section>
</template>

<script>
import NoteResult from "./NoteResult.vue";
export default {
   props:['results'],
  components: {
    NoteResult,
  },
};
</script>

<style scoped>
.form-control {
  margin: 0.5rem 0;
}

h1 {
  color: rgb(25, 25, 112);
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 40px;
}

ul {
  list-style: none;
  margin: 0;
  padding: 0;
}
</style>