<template>
  <div style="background-color: rgb(8, 177, 193) !important">
    <div class="row">
      <div class="col-lg-1 col-md-1"></div>
      <div class="col-lg-5 col-md-5 col-sm-12 col-xs-12">
        <q-space></q-space>
        <q-item>
          <q-chat-message
            class="chat_msg"
            text-color="primary"
            :text="['Full time, Part time']"
            sent
          />
        </q-item>
        <q-item>
          <h4 class="main_header">
            with the best skills Are you looking for foreign talent?
          </h4>
        </q-item>
        <q-item>
          <h6 class="sub_header">
            Legal and personnel management without any hassle Get hired remotely
            within 1 week.
          </h6>
        </q-item>
        <q-item class="sub_header1">
          <a href="#" target="_blank">
            <p>Do developers need it?</p>
          </a>
        </q-item>
        <div class="row">
          <div class="col-4">
            <q-separator color="grey-4" size="2px" inset class="separator" />

            <q-item>
              <p class="description_content">
                Average monthly salary of 120 million won is calculated based on
                the relevant country.
              </p>
            </q-item>
          </div>
          <div class="col-4">
            <q-separator color="grey-4" size="2px" inset class="separator" />

            <q-item>
              <p class="description_content">
                Don't worry if you don't get a job up to 30 days.
              </p>
            </q-item>
          </div>
          <div class="col-4">
            <q-separator color="grey-4" size="2px" inset class="separator" />
            <q-item>
              <p class="description_content">
                Average 3 days, maximum 10 days, quick recruitment is possible
                even if a person is required
              </p>
            </q-item>
          </div>
        </div>
      </div>
      <div class="col-1"></div>

      <div class="q-pa-md main col-lg-5 col-md-5 col-sm-12 col-xs-12">
        <q-carousel
          v-model="slide"
          transition-prev="scale"
          transition-next="scale"
          swipeable
          animated
          control-color="blue"
          navigation
          padding
          arrows
          height="340px"
          class="bg-grey-1 text-black shadow-1 rounded-borders"
        >
          <q-carousel-slide
            :name="user.name"
            v-for="(user, index) in userData"
            :key="index"
            class="column no-wrap flex-center"
          >
            <q-avatar size="85px">
              <img :src="user.profileImage" :name="user.name" />
            </q-avatar>
            <q-item class="title item_padding">{{ user.name }}</q-item>
            <q-item class="sub_title item_padding">
              {{ user.role }} . {{ user.expirience }}
            </q-item>
            <div class="text-center row" style="justify-content: center">
              <q-item
                class="sub_item_padding"
                :class="skill.name.length >= 20 ? col - 12 : col - 6"
                v-for="(skill, index) in user.skills"
                :key="index"
              >
                <q-chip
                  outline
                  square
                  color="grey-14"
                  text-color="white"
                  class="btn"
                  style="font-size: 13px !important"
                >
                  {{ skill.name }}
                </q-chip>
              </q-item>
            </div>
          </q-carousel-slide>
        </q-carousel>
      </div>
      <div
        v-if="!isMobile()"
        class="isCheckbox q-pa-md main col-lg-5 col-md-5 col-sm-12 col-xs-12"
      >
        <div class="q-gutter-sm">
          <q-checkbox v-model="teal" label="Competence" color="indigo-10" />
          <q-checkbox
            v-model="orange"
            label="ability to perform work"
            color="indigo-10"
          />
          <q-checkbox
            v-model="red"
            label="whether there is modesty"
            color="indigo-10"
          />
          <q-checkbox v-model="cyan" label="tablet review" color="indigo-10" />
        </div>
      </div>
      <!-- <div class="col-1"></div> -->
    </div>
    <div class="row contentdata">
      <div class="col-1"></div>
      <div class="col-lg-10 col-md-10 col-sm-12 col-xs-12">
        <q-btn class="btn_list" flat size="md">
          <q-btn square class="btn_sub" icon="shopping_cart" />
          overseas marketing
        </q-btn>
        <q-btn class="btn_list" flat size="md">
          <q-btn square class="btn_sub" icon="directions" />
          public
        </q-btn>
        <q-btn class="btn_list" flat size="md">
          <q-btn square class="btn_sub" icon="my_location" />
          overseas sales
        </q-btn>
        <q-btn class="btn_list" flat size="md">
          <q-btn square class="btn_sub" icon="shopping_cart" />
          overseas marketing
        </q-btn>
      </div>
      <div class="col-1"></div>
    </div>
  </div>
</template>
<script>
import { ref } from "vue";

export default {
  data() {
    return {
      isCheckbox: true,
      contentdata: true,
      teal: ref(true),
      orange: ref(false),
      red: ref(false),
      cyan: ref(true),
      slide: ref("Jyoti Desai"),
      // slide: 1,
      userData: [
        {
          id: 1,
          name: "Jyoti Desai",
          profileImage: "https://cdn.quasar.dev/img/avatar.png",
          role: "FrontEndDeveloper",
          expirience: "3y+",
          skills: [
            {
              id: 1,
              name: "Twitter management",
            },
            {
              id: 2,
              name: "blog writing",
            },
            {
              id: 3,
              name: "marketing content creation",
            },
            {
              id: 4,
              name: "Instagram management",
            },
          ],
        },
        {
          slide_id: 2,
          name: "karuna D",
          profileImage: "https://cdn.quasar.dev/img/avatar2.jpg",
          role: "FullStackDeveloper",
          expirience: "5y+",
          skills: [
            {
              id: 1,
              name: "Twitter management",
            },
            {
              id: 2,
              name: "blog writing",
            },
            {
              id: 3,
              name: "marketing content creation",
            },
            {
              id: 4,
              name: "Instagram management",
            },
          ],
        },
        {
          slide_id: 3,
          name: "Aditi Gupta",
          profileImage: "https://cdn.quasar.dev/img/avatar.png",
          role: "Marketing",
          expirience: "2y+",
          skills: [
            {
              id: 1,
              name: "Twitter management",
            },
            {
              id: 2,
              name: "blog writing",
            },
            {
              id: 3,
              name: "marketing content creation",
            },
            {
              id: 4,
              name: "Instagram management",
            },
          ],
        },
        {
          slide_id: 4,
          name: "Priti Sharma",
          profileImage: "https://cdn.quasar.dev/img/avatar2.jpg",
          role: "Banking",
          expirience: "1y+",
          skills: [
            {
              id: 1,
              name: "Twitter management",
            },
            {
              id: 2,
              name: "blog writing",
            },
            {
              id: 3,
              name: "marketing content creation",
            },
            {
              id: 4,
              name: "Instagram management",
            },
          ],
        },
        {
          slide_id: 5,
          name: "Saee Patil",
          profileImage: "https://cdn.quasar.dev/img/avatar2.jpg",
          role: "Modeling",
          expirience: "4y+",
          skills: [
            {
              id: 1,
              name: "Twitter management",
            },
            {
              id: 2,
              name: "blog writing",
            },
            {
              id: 3,
              name: "marketing content creation",
            },
            {
              id: 4,
              name: "Instagram management",
            },
          ],
        },
      ],
      lorem:
        "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.",
    };
  },
  methods: {
    isMobile() {
      if (screen.width > 760) {
        console.log(screen.width);
        return true;
      } else {
        return false;
      }
    },
  },
};
</script>

<style scoped>
.main {
  width: 37% !important;
  justify-content: center;
}
.separator {
  font-size: 2px !important;
}
@media only screen and (min-width: 700px) {
  .isCheckbox {
    display: none;
  }
}
@media only screen and (max-width: 700px) {
  .contentdata {
    display: none;
  }
  /* For desktop: */
  .main {
    width: 100% !important;
  }
  .description_content {
    display: none !important;
  }
  .separator {
    display: none;
  }
  .sub_header1 {
    display: none;
  }
}
.title {
  font-weight: 900;
  font-size: x-large;
}
.sub_title {
  font-weight: 400;
  font-size: 14px;
  letter-spacing: 0.2px;
}
.item_padding {
  min-height: 30px !important;
  padding: 4px 16px !important;
}
.sub_item_padding {
  padding: 0px 0px !important;
  min-height: 0px !important;
}
.btn {
  text-transform: capitalize;
  line-height: 1em !important;
}
.chat_msg {
  font-weight: 600;
  font-size: 14px;
  color: blue !important;
}
q-message-text-content--sent {
  color: blue !important;
}
.main_header {
  text-transform: capitalize !important;
  font-weight: 600 !important;
  color: white !important;
  letter-spacing: 0.5px !important;
  margin: 0px !important;
}
.sub_header {
  text-transform: capitalize !important;
  font-weight: 400 !important;
  color: white !important;
  /* letter-spacing: 0.2px !important; */
  margin: 0px !important;
}
.sub_header1 {
  text-transform: capitalize !important;
  font-weight: 400 !important;
  color: white !important;
  letter-spacing: 0.2px !important;
  margin: 0px !important;
  font-size: 1.05em !important;
}
.description_content {
  color: white !important;
  line-height: 18px !important;
  font-weight: 500 !important;
}
.btn_list {
  background-color: #ffffff35;
  margin: 10px !important;
  border-radius: 5px !important;
  color: white;
  padding: 0px 10px 0px 4px !important;
}

.btn_sub {
  margin: 8px 12px 8px 6px !important;
  padding: 8px 10px 8px 10px;
  background-color: #ffffff50 !important;
  border-radius: 5px !important;
}
.isCheckbox {
  color: white;
  font-weight: 500 !important;
  letter-spacing: 0.2px !important;
}
.align_box {
  display: flex;
  justify-content: center;
}
</style>
