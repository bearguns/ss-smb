<script>
  let techSkills = {
      languages: [
	  'JavaScript',
	  'Python',
	  'TypeScript'
      ],
      'front-end': [
	  'VueJS',
	  'React',
	  'Svelte',
	  'HTML/CSS',
	  'SASS'
      ],
      'back-end': [
	  'PostgreSQL',
	  'Linux',
	  'Heroku',
	  'Express',
	  'Flask',
      ]
  };
  let softSkills = [
      'Written & Verbal Communication',
      'Public Speaking & Product Demos',
      'Customer Focus',
  ];
</script>

<style>
  .resume-skills {
      border-bottom: 1px solid black;
  }
  .resume-skills__category {
      text-transform: uppercase;
  }

  .resume-skills__list {
      font-size: 12px;
  }

  .resume-skills__title {
      margin-bottom: 8px;
  }
</style>

<h1 class="subtitle section-title">RELEVANT SKILLS</h1>
<div class="columns resume-skills">
  <div class="column is-two-thirds">
    <h2>TECH SKILLS</h2>
    <div class="columns">
      {#each Object.keys(techSkills) as category}
      <div class="column is-one-quarter">
	<ul class="resume-skills__list">
	  {#each techSkills[category] as skill}
	  <li>{skill}</li>
	  {/each}
	</ul>
      </div>
      {/each}
    </div>
  </div>
  <div class="column">
    <h2>SOFT SKILLS</h2>
    <ul class="resume-skills__list">
      {#each softSkills as skill}
      <li>{skill}</li>
      {/each}
    </ul>
  </div>
</div>

