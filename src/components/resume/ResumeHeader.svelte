<script>
  import ResumeContact from './ResumeContact.svelte';
  import ResumeTitle from './ResumeTitle.svelte';
</script>

<style>
  .resume-header {
      border-bottom: 1px solid black;
  }
</style>

<div class="columns resume-header">
  <div class="column is-two-thirds">
    <ResumeTitle />
  </div>
  <div class="column">
    <ResumeContact />
  </div>
</div>
