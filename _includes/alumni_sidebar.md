Alumni
{% assign sorted = (site.alumni | sort: "enddate") | reverse %} {% for member in sorted %}

{{member.name}} - {{member.position}}
{% if member.pronouns %} {{member.pronouns}}
{% endif %}

{% assign start = member.startdate | date:"%Y" %} {% assign end = member.enddate | date:"%Y" %} {% if start == end %} {{ start }}
{% else %} {{ start }} - {{ end }}
{% endif %} {% if member.subsequent %} Subsequently: {{ member.subsequent }}
{% endif %}

{% if member.cv %} curriculum vitae
{% endif %} {% if member.email %} {% unless member.email contains "scripps.edu" %} {{member.email}}
{% endunless %} {%endif%} {% if member.website %} {{member.website}}
{% endif %} {% if member.orcid %}  {{member.orcid}}
{% endif %} {% if member.linkedin %}  LinkedIn
{% endif %} {% if member.scholar %}  Scholar Citations
{% endif %} {% if member.twitter %}  @{{member.twitter}}
{% endif %} {% if member.github %} {% octicon mark-github %} {{member.github}}
{% endif %}

{% endfor %}
