---
layout: main
main: true
title: 소개
---

<div class="loading-animation">
    <div class="about">
        <div class="about_me">
            <span class="sub_title">About Me</span>
            <div class="content">
                <img class="profile" src="/meta/jurirang.jpg"/>
                <span class="description">
                    안녕하세요! 언제나 활발하고 재기발랄한 개발자 주리랑입니다!<br/> 
                    Front-end와 UI/UX에 관심이 많은 아직 햇병아리 개발자입니다 🐣
                </span>    
            </div>          
        </div>
        <div class="experience">
            <span class="sub_title">Experience</span>
            <div class="content">
                <div class="timeline">
                {% assign experiences = site.data.experience%}
                {% for experience in experiences %}
                    <div class="entry">
                        <div class="period">
                          <p class="title">{{ experience.period }}</p>
                        </div>
                        <div class="content">
                            {% for content in experience.content %}
                                <span class="company">{{ content.company }}</span>
                                <p class="title"> {{ content.title }}</p>
                                {% if content.description  != null %}
                                    <ul>
                                        <li>{{ content.description }}</li>
                                    </ul>
                                {% endif %}
                            {% endfor %}
                        </div>
                     </div>
                {% endfor %}
            </div>
            </div>
        </div>
        <div class="skill">
            <span class="sub_title">Skill<br/></span>
            <div class="content"> 
            {% assign skills = site.data.skill %}
             {% for skill in skills %}
             <div class="set">
                {{ skill.language }}
             </div>
            {% endfor %}
            </div>
        </div>
    </div>
</div>

