---
title: Program
layout: page
slide_id: 4
---

#### Program Overview

{% if site.data.conference.program_link %}
[<i class="fa fa-external-link fa-fw" aria-hidden="true"></i>**Printed program**]({{ site.data.conference.program_link }})

{% else %}
#### Technical Program

TBD

{% endif %}

{% for day in site.data.schedule %}
    <div>
        <h4 class="schedule-table-heading">{{ day.dateReadable }} - Day {{ forloop.index }}</h4>
        <table class="table table-bordered table-striped table-hover table-responsive table-sm">
        {% for timeslot in day.timeslots %}
          <thead>
            <tr>
              <th class="bg-info text-center">
                <div>{{timeslot.startTime}}-{{timeslot.endTime}}</div>
              </th>
              {% if timeslot.type == "service" %}
                <th class="bg-warning text-center">
                  <p class="text-muted">{{timeslot.title}}</p>
                </th>
              {% else %}
                <th class="bg-primary text-center">
                  <h5>{{timeslot.title}}</h5>
                  {% if timeslot.speaker %}
                  <h5>{{timeslot.speaker}}</h5>
                  {% endif %}
                  {% if timeslot.chair %}
                      <h6>Session chair:{{timeslot.chair}}</h6>
                  {% endif %}
                </th>
              {% endif %}
            </tr>
          </thead>
          {% if timeslot.events %}
          <tbody>
            {% for event in timeslot.events %}
              <tr>
                <td width="20%">
                </td>
                <td>
                  <p><b>{{event.title}}</b></p>
                  <p><i>{{event.speakers}}</i></p>
                </td>
              </tr>
            {% endfor %}
          </tbody>
          {% endif %}
        {% endfor %}
        </table>
    </div>

{% endfor %}
