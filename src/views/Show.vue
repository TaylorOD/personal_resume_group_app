<template>
  <div class="resume-show">
    <h1> {{ user.first_name }}'s resume</h1>
    <div><img v-bind:src="user.photo" style="height: 100px; width: 100px;"></div>
    <h2>Education</h2>
    <div v-for="education in user.educations">
      <ul>
      <li> <strong>Degree:</strong> {{ education.degree }}
        <p><strong>School: </strong>{{ education.university_name }}</p>
        <p><strong>Dates: </strong>{{ education.start_date }} - {{ education.end_date }}</p>
        <p><strong>Details: </strong>{{ education.details }} </p>
        </li>
      </ul>
      </div>
    <h2>Experience</h2>
    <p>{{ user.experiences }}</p>
    <h2>Projects</h2>
    <p>{{ user.projects }}</p>
    <h2>Skillz</h2>
    <p>{{ user.skills }}</p>
  </div>
</template>

<style>
</style>

<script>
import axios from "axios";
export default {
  name: "ResumeShow",
  data: function() {
    return {
      user: {
        
        "user_id": 1,
        "first_name": "John",
        "last_name": "Smith",
        "email": "John@example.com",
        "phone_number": "555-555-5555",
        "short_bio": "A short bio",
        "linkedin_url": "johnsmith1",
        "twitter_handle": "johnnysmith",
        "website_url": "john.com",
        "online_resume_url": "john.resume.com",
        "github_url": "johnsmith1",
        "photo": "https://www.history.com/.image/ar_1:1%2Cc_fill%2Ccs_srgb%2Cfl_progressive%2Cq_auto:good%2Cw_1200/MTU3ODc5MDgzNDc5NjcyNTQz/portrait-of-john-smith.jpg",
        "educations": [
          {
            "id": 1,
            "start_date": "06/20/16",
            "end_date": "06/20/20",
            "degree": "Bachelor of Arts",
            "university_name": "Stanford",
            "details": "degree in art",
            "user_id": 1,
            "created_at": "2020-11-03T02:01:04.793Z",
            "updated_at": "2020-11-03T02:01:04.793Z"
          }
        ],
        "experiences": [
          {
            "id": 1,
            "start_date": "07/20/2019",
            "end_date": "10/20/2020",
            "job_title": "dog walker",
            "company_name": "John's Dog's",
            "details": "Dog walker",
            "user_id": 1,
            "created_at": "2020-11-03T02:01:04.684Z",
            "updated_at": "2020-11-03T02:01:04.684Z"
          }
        ],
        "projects": [
          {
            "id": 1,
            "name": "Website",
            "description": "website about dogs",
            "url": "dogs.com",
            "screenshot": null,
            "user_id": 1,
            "created_at": "2020-11-03T02:01:04.568Z",
            "updated_at": "2020-11-03T02:01:04.568Z"
          }
        ],
        "skills": [
          {
            "id": 1,
            "name": "HTML",
            "user_id": 1,
            "created_at": "2020-11-03T02:01:04.464Z",
            "updated_at": "2020-11-03T02:01:04.464Z"
          }
        ]
      },
      
    };
  },
  created: function() {
    // this.showResume();
  },
  methods: {
    // showResume: function() {
    //   axios.get("api/users/" + this.$route.params.id).then((response) => {
    //     console.log("User info:", response.data );
    //     this.user = response.data;
    //   });
    // }
  }
};
</script>