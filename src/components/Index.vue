<template>
  <div>
    <div id="top-bar"></div>
    <div class="container">
      <br/>
      {{msg}}
      <br/>

      Tags | <span v-on:click="getRepos">Repos</span> | <span v-on:click="getStars">Stars</span>

      <ul id="repos" class="container">
        <li v-for="repo in repos">
          <a target="_blank" v-bind:href="repo.html_url">{{ repo.name }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        msg: 'Welcome to Your GithubTags',
        api: 'http://localhost:3000/repos',
        apiStarred: 'http://localhost:3000/repos/starred',
        repos: []
      }
    },
    methods: {
      getRepos () {
        this.$http.get(this.api).then(response => {
          this.repos = response.data
        }, response => {
        })
      },
      getStars () {
        this.$http.get(this.apiStarred).then(response => {
          this.repos = response.data
        }, response => {
        })
      }
    },
    created () {
      this.getRepos()
    }
  }
</script>


