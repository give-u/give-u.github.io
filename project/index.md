---
layout: main
title: 프로젝트
main: true
---

<div class="project">
    {% assign projects = site.data.project%}
    {% for project in projects %}
    <div class="container">
        <img class="image" src="{{ project.image }}"/>
        <div class="content">
            <div class="category">
            {% for category in project.category %}
             <div class="set">
                {{ category }}
             </div>
            {% endfor %}
            </div>
            <div class="title">{{project.title}}</div>
            <div class="service">{{project.service}}</div>
            <div class="period">{{project.period}}</div>
            <ul>
                <li>- {{project.description}}</li>
            </ul>
            <div class="language">
            {% for skill in project.langauge %}
             <div class="set">
                {{ skill }}
             </div>
            {% endfor %}
            </div>
        </div>
    </div>
    {% endfor %}
</div>