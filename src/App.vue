<template>
  <note-comp @note-result="notesList"></note-comp>
  <note-output :results="savedNotes"></note-output>
</template>

<script>
import NoteComp from "./components/Notes/NoteComp.vue";
import NoteOutput from "./components/Notes/NoteOutput.vue";
export default {
  components: {
    NoteComp,
    NoteOutput,
  },
  data(){
    return {
      savedNotes: [],
    }
  },
  methods: {
    notesList(listData){
      const listOutput = {
        note: listData.note,
        onemlilikDerecesi: listData.onemlilikDerecesi,
        id: new Date().toISOString(),
      }
      this.savedNotes.push(listOutput);
      console.log(listOutput);
    }
  }
};
</script>

<style>
</style>
