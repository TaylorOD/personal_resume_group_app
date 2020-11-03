<template>
  <div class="resume-show">
    <h1> {{ user.first_name }}'s resume</h1>
    <img v-bind:src="user.photo">
    <h2>Education</h2>
    <p>{{ user.educations }}</p>
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
            "created_at": "2020-11-03T00:32:55.138Z",
            "updated_at": "2020-11-03T00:32:55.138Z"
          }
        ],
        "experiences": [{
          "id":1,
          "start_date": "06/1/16",
          "end_date": "06/1/20",
          "type": "Volunteer",
          "description": "I volunteered to save puppies.",
          "employer": "The volunteer Group",
          "user_id": 1,
          "created_at": "2020-11-03T00:32:55.138Z",
          "updated_at": "2020-11-03T00:32:55.138Z"
        }],
        "projects": [{
          "id":1,
          "start_date": "06/30/16",
          "end_date": "06/30/20",
          "description": "I made some awesome thing.",
          "user_id": 1,
          "created_at": "2020-11-03T00:32:55.138Z",
          "updated_at": "2020-11-03T00:32:55.138Z"
        }],
        "skills": ["JavaScript", "CSS", "Git", "Comedy"]
      },
    };
  },
  created: function() {
    // this.showResume();
  },
  methods: {
    // showResume: function() {
    //   axios.get("/api/resumes" + this.$route.params.id).then((response) => {
    //     console.log("Userinfo:", response.data );
    //     this.user = response.data;
    //   });
    // }
  }
};
</script>