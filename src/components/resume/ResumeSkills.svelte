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
	  'NodeJS',
	  'Flask',
	  'Django'
      ]
  };
  let softSkills = [
      'Learning on the fly',
      'Written & verbal communication',
      'Public speaking',
      'Internal training & knowledge transfer',
      'Customer focus',
  ];
</script>

<style>
  .resume-skills {
      border-bottom: 1px solid black;
  }
</style>

<h1 class="section-title">RELEVANT SKILLS</h1>
<div class="columns resume-skills">
  <div class="column is-two-thirds">
    <h2 class="is-size-7">TECH SKILLS</h2>
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
    <h2 class="is-size-7">SOFT SKILLS</h2>
    <ul>
      {#each softSkills as skill}
      <li>{skill}</li>
      {/each}
    </ul>
  </div>
</div>

