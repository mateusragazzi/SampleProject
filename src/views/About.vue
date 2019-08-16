<template>
  <v-layout align-center justify-center column fill-height>
    <v-flex pa-5 md12 align-center>
      <img class="me" src="../assets/me.png"/>
      <h2><b>Thanks for usign this project!</b></h2>
      <p>I work as a developer since 2016 and I'm always creating things and tools to help the community.</p>
      <p>Feel free to send a message:</p>
      <v-list>
        <v-list-item-content v-for="item in social_medias" :key="item.name">
          <v-list-item-title>
            <span>
              <v-icon :color="item.color" dark>{{item.icon}}</v-icon>
            </span>
            <a :href="item.link">{{item.name}}</a>
          </v-list-item-title>
        </v-list-item-content>
      </v-list>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      social_medias: [
        {
          name: "www.mateusragazzi.com",
          icon: "language",
          link: "http://mateusragazzi.com/",
          color: "orange"
        },
        {
          name: "mateusragazzi.b@gmail.com",
          icon: "mail",
          link: "malito:mateusragazzi.b@gmail.com",
          color: "pink"
        },
        {
          name: "+55 67 992256827",
          icon: "message",
          link:
            "https://api.whatsapp.com/send?phone=5567992256827&text=Hi%2C%20",
          color: "green"
        },
        {
          name: "@r_mateus39",
          icon: "alternate_email",
          link: "http://mateusragazzi.com/",
          color: "blue"
        }
      ]
    };
  }
};
</script>

<style scoped>
.v-icon {
  margin-right: 5px;
}
.me {
  width: 40%;
  max-width: 200px;
}
h2 {
  margin-bottom: 15px;
}
</style>
