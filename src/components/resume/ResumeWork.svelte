<script>
  let history = [
      {
	  company: 'ReCharge Payments',
	  title: 'Front End Engineer',
	  time: 'January 2019 - March 2020',
	  bullets: [
	      'Designed and delivered all-new "batteries included" customer portal theme as a SPA written with VueJS, Vue Router, and Vuex.',
	      'Converted legacy UI components from vanilla JS/jQuery to VueJS.',
	      'Developed and maintained UI components following Agile/SCRUM methodologies.',
	      'Developed back-end features and enhancements in Python (Flask).',
	  ]
      },
      {
	  company: 'Digital Assets Data',
	  title: 'Front End Engineer',
	  time: 'July 2018 - December 2018',
	  bullets: [
	      'Developed cryptocurrency analytics and reporting dashboard for institutional investors and researchers.',
	      'Wrote and tested React components.',
	      'Developed GraphQL API endpoints and integrations.',
	      'Developed back-end services and endpoints in Python (Django).'
	  ]
      },
      {
	  company: 'T-Mobile (FKA Layer3TV)',
	  title: 'Web Development Engineer',
	  time: 'April 2016 - July 2018',
	  bullets: [
	      'Converted legacy UI components from jQuery/AngularJS to VueJS',
	      'Designed and deployed iPad-optimized SPA with VueJS, Vuex, and Vue Router for use in T-Mobile retail stores.',
	      'Developed payment delinquency tracking and notification system using NodeJS, Express, and MongoDB.'
	  ]
      }
  ];
</script>


<style>
  .resume-work {
      margin-bottom: 11px;
  }
</style>

<h2 class="section-title is-size-6">WORK HISTORY</h2>
{#each history as job}
<div class="resume-work">
  <h3 class="is-size-6">{job.title}</h3>
  <h3 class="is-size-7">{job.company} | {job.time}</h3>
  <ul>
    {#each job.bullets as bullet}
    <li>{bullet}</li>
    {/each}
  </ul>
</div>
{/each}
