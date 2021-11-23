---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
# Prime Minister 1832-1900
<div id="primeminister">
<ul>
{% for election in site.data.simplified_election_data %}
{% assign winner = site.data.parties | find: "pm", election.pm %}
{% assign incident = site.data.events | find: "year", election.year %}
<li>{{ election.pm }}, who belonged to {{ winner.party }}, won the elections in {{ election.year }}, which is also the year in which {{ incident.event }}.</li>
{% endfor %}
</ul>
</div>