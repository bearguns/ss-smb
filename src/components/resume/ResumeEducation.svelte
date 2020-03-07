<script>
  const education = [
      {
	  title: 'Web Development Intensive',
	  school: 'Galvanize',
	  time: '2015-2016',
	  bullets: [
	      'Graduated with certificate.',
	      'Received strong recommendations from instructors and staff.',
	  ]
      }
  ]
</script>

<h2 class="section-title is-size-6">EDUCATION</h2>
{#each education as edu}
<h3 class="is-size-6">{edu.school}</h3>
<h4 class="is-size-7">{edu.title} {edu.time}</h4>
<ul>
  {#each edu.bullets as bullet}
  <li>{bullet}</li>
  {/each}
</ul>
{/each}
