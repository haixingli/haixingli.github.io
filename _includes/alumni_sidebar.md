Alumni


{{member.name}} - {{member.position}}


{% assign start = member.startdate | date:"%Y" %} {% assign end = member.enddate | date:"%Y" %} {% if start == end %} {{ start }}
{% else %} {{ start }} - {{ end }}
{% endif %} {% if member.subsequent %} Subsequently: {{ member.subsequent }}
{% endif %}

{% if member.email %} {{member.email}} {%endif%}
{% if member.website %} {{member.website}}
{% endif %} {% if member.orcid %}  {{member.orcid}}
{% endif %} {% if member.linkedin %}  LinkedIn
{% endif %} {% if member.scholar %}  Scholar Citations
{% endif %} {% if member.twitter %}  @{{member.twitter}}
{% endif %} {% if member.github %} {% octicon mark-github %} {{member.github}}
{% endif %}
