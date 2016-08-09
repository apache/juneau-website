---
layout: page 
title: Downloads
permalink: /downloads/

menu-title:  Downloads
menu-weight: 0
menu-class:  download
---

Provide information about releases.  The below table will render the contents of _releases for you

<table class="releases">
    <tr>
        <th>Version</th>
        <th>Summary</th>
        <th>Release Date</th>
    </tr>
    {% assign releases = site.releases | sort: 'date' %}
    {% for release in releases reversed %}
        {% if release.title %}
            <tr>
                <td><a href="{{ release.url | prepend: site.baseurl }}">{{ release.title }}</a></td>
                <td>{{ release.summary }}</td>
                <td>{{ release.date | date: "%Y-%m-%d" }}</td>
            </tr>
        {% endif %}
    {% endfor %}
</table>

