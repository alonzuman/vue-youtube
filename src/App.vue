<template>
  <div id="app">
    <Navbar v-bind:me="dummyData.me"></Navbar>
    <VideoPage v-bind:dummyData="dummyData"></VideoPage>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import VideoPage from "./components/VideoPage.vue";

export default {
  name: "App",
  components: {
    Navbar,
    VideoPage
  },
  data() {
    // Dummy main video and videos data
    return {
      dummyData: {
        me: {
          name: "Alon Zuman",
          avatar:
            "https://yt3.ggpht.com/a-/AOh14GiV_Avk6ZxrgZiIxCdmsASPVijX9JUsT28Kji4h=s88-c-k-c0xffffffff-no-rj-mo"
        },
        mainVideo: {
          title: "Nested Components in vuejs - Vuejs tutorials - Tutorial 24",
          views: "110,990",
          datePosted: "14 Apr 2019",
          user: {
            name: "The Digital Sight",
            subscribers: 836
          },
          description:
            "Nested Components in vuejs - Nested component is component nested in its parent component. When one component has another component rendered in self. It is called nesting components. The component which has another component in self is called a parent component. Another component which is get rendered in other component is called child component. This is a simple definition of what is nested components. Any component can have child components. Nesting component can be of any level. The main component can have child component and that child component can have another child component which makes it parent component and so far.",
          comments: [
            {
              id: 1,
              user: "username1",
              content: "Such valuable information! Thanks for the UK :D",
              datePosted: "2 Feb 2020",
              avatar:
                "https://yt3.ggpht.com/a/AATXAJwtbijcDZ5iie-UXhIfwwKy2oTag3lpeFXGqw=s48-c-k-c0xffffffff-no-rj-mo"
            },
            {
              id: 2,
              user: "username2",
              content: "Such valuable information! Thanks for the UK :D",
              datePosted: "2 Feb 2020",
              avatar:
                "https://yt3.ggpht.com/a/AATXAJwtbijcDZ5iie-UXhIfwwKy2oTag3lpeFXGqw=s48-c-k-c0xffffffff-no-rj-mo"
            }
          ]
        },
        videos: [
          {
            id: 1,
            title: "Video 1",
            username: "Username2",
            views: "104,022",
            datePosted: "3 Years ago",
            image: "https://picsum.photos/200/300"
          },
          {
            id: 2,
            title: "Video 2",
            username: "Username2",
            views: "104,022",
            datePosted: "1 Years ago",
            image: "https://picsum.photos/200/300"
          }
        ]
      }
    };
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --border: 1px solid #d6d6d6;
  --red: #cc0000;
  --extra-light: #ebebeb;
  --light: #c5c5c5;
  --light-gray: #626262;
  --dark-gray: black;
}

button,
input {
  padding: 8px 16px;
  font-size: 12px;
}

input:focus {
  outline: none;
}

button {
  font-size: 12px;
}

button:focus {
  outline: none;
}

button:hover {
  cursor: pointer;
}

.icon-button {
  border: none;
  background-color: transparent;
  color: var(--light-gray);
}

.icon-button:hover {
  color: var(--dark-gray);
}

body {
  background-color: #f4f4f4;
  font-family: Arial, Helvetica, sans-serif;
}

li {
  list-style: none;
}

h1 {
  color: pink;
}

h2 {
  font-size: 18px;
  margin-top: 16px;
}

h3 {
  font-weight: 600;
  font-size: 14px;
}

h4 {
  color: var(--light-gray);
  font-size: 12px;
  font-weight: 300;
}

p {
  font-weight: 300;
  font-size: 14px;
}
</style>
