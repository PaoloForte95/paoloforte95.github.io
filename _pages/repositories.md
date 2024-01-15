---
layout: page
permalink: /repositories/
title: Repositories
description: GitHub repositories.
nav: true
nav_order: 4
---

## GitHub Profile

{% if site.data.repositories.github_users %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

## GitHub Public Repositories

{% if site.data.repositories.github_repos %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

## GitHub Private Repositories

### **Athena**

A task planning framework designed to solve, dispatch, and execute PDDL and HDDL planning problems.

The library contains:

* A PDDL 3.1 and HDDL 1.0 parser based on the [PDDL4j library](https://github.com/pellierd/pddl4j).

* A set of task planning algorithms to compute plans for PDDL and HDDL planning problems.

* Three different types of execution plans: Total Order, Partial Order, and Concurrent.

* Several examples.