<script>
  import ResumeHeader from '../components/resume/ResumeHeader.svelte';
  import ResumeSkills from '../components/resume/ResumeSkills.svelte';
  import ResumeWork from '../components/resume/ResumeWork.svelte';
  import ResumeEducation from '../components/resume/ResumeEducation.svelte';
  import { hideSidebar } from '../stores.js';
  import { onMount } from 'svelte';

  onMount(() => {
      hideSidebar.update(value => true);
      setTimeout(() => window.print(), 1500);
  });
</script>

<style>

</style>

<svelte:head>
	<title>Resume | Sean M Brage</title>
</svelte:head>

<div class="container">
<ResumeHeader />
<div class="columns">
  <div class="column">
    <ResumeSkills />
  </div>
</div>
<div class="columns">
  <div class="column is-two-thirds">
    <ResumeWork />
  </div>
  <div class="column">
    <ResumeEducation />
  </div>
</div>
</div>

