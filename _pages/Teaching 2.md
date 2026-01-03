<!---
layout: page
permalink: /teaching2/
title: Teaching2
description: 
nav: true
nav_order: 3
--->

## University of Georgia

<div class="mb-4">
  {% for course in site.data.teaching.instructor %}
  <div class="card hoverable mb-3 z-depth-1" style="border-left: 5px solid #008080;">
    <div class="card-body">
      <div class="row align-items-center">
        <div class="col-2 col-md-1 text-center">
           <i class="fas fa-chalkboard-teacher fa-2x" style="color: #008080;"></i>
        </div>
        <div class="col-10 col-md-11">
          <div class="d-flex justify-content-between align-items-center mb-1">
             <h5 class="card-title font-weight-bold mb-0">{{ course.title }}</h5>
             <span class="badge text-white" style="background-color: #008080;">{{ course.code }}</span>
          </div>
          <p class="card-text text-muted mb-1 font-weight-bold" style="font-size: 0.9rem;">
            INSTRUCTOR OF RECORD
          </p>
          <p class="card-text">{{ course.info }}</p>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>

<div class="row mt-5 mb-4 align-items-center">
    <div class="col">
        <hr class="my-0">
    </div>
    <div class="col-auto">
        <h5 class="mb-0 text-muted font-weight-bold text-uppercase">
            <i class="fas fa-pencil-alt mr-2"></i> Grading & TA
        </h5>
    </div>
    <div class="col">
        <hr class="my-0">
    </div>
</div>

<div class="row">
  {% for course in site.data.teaching.grader %}
  <div class="col-12 col-md-6 mb-3">
    <div class="card hoverable h-100 z-depth-1" style="border-top: 4px solid #ba0c2f;">
      <div class="card-body">
        <div class="d-flex justify-content-between align-items-start">
          <div>
            <h6 class="font-weight-bold mb-1">{{ course.title }}</h6>
            <div class="small mb-2 font-weight-bold" style="color: #ba0c2f;">{{ course.code }}</div>
          </div>
          <i class="fas fa-check-circle fa-lg opacity-25" style="color: #ba0c2f; opacity: 0.3;"></i>
        </div>
        
        <hr class="my-2 opacity-25">
        
        <div class="small text-muted">
          <div class="d-flex align-items-center mb-1">
            <i class="far fa-calendar-alt mr-2" style="width: 20px;"></i>
            <span>{{ course.term }}</span>
          </div>
          <div class="d-flex align-items-center">
            <i class="far fa-user mr-2" style="width: 20px;"></i>
            <span>Prof. {{ course.instructor }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
</div>