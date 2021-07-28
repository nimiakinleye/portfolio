<template>
  <div>
    <div v-for="(job, i) in jobs" :key="i" class="job">
      <div class="flex flex-col shadow-2xl">
        <img
          class="rounded-t-lg"
          :src="
            'https://api.apiflash.com/v1/urltoimage?access_key=' +
            access_key +
            '&format=png&url=https://' +
            job.url
          "
          alt="website_snapshot"
        />
        <a
          class="flex justify-between my-bg py-4 p-2 rounded-b-lg"
          :href="'https://' + job.url"
          target="_blank"
        >
          <div>https://{{ job.url }}</div>
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M21 3L13.93 19.97L11.42 12.58L4.03 10.07L21 3Z"
              stroke="white"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              d="M11 13L5 19"
              stroke="white"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </a>
      </div>
      <h4 class="firm">{{ job.firm }}</h4>
      <p class="job_description">
        {{ job.job_description }}
      </p>
    </div>
  </div>
</template>

<script>
import axios from '@nuxtjs/axios'
export default {
  data() {
    return {
      jobs: [
        {
          firm: 'Cashdrive',
          job_description: `Was solely responsible for the development of the product’s app user
      intercace, ranging from the User App to the Admin App. The afore mentioned
      was achieved with NuxtJs, an extended framework of VueJs which is a
      framework of JavaScript.`,
          url: 'cashdrive.co',
        },
        {
          firm: 'Credit-Card',
          job_description: `I worked on this project which is yet to be released by the company as the UI and Front-end developer. I was completely
responsible for the user interface's development as well as
API consumption`,
          url: 'creditcard.cashdrive.co',
        },
        {
          firm: 'Self-paced',
          job_description: `I designed a webapp to display weather information of desired locations, using open weather API`,
          url: 'nimi-weather-app.netlify.com',
        },
        {
          firm: 'Self-paced',
          job_description: `Built a sample landing page`,
          url: 'nimi-paynyce.netlify.app',
        },
        {
          firm: 'Self-paced',
          job_description: `Built a sample app to display employee info`,
          url: 'nimi-flipstaff.netlify.app/home/',
        },
      ],
      snapshots: [],
      snapshots_updated: false,
      access_key: '1c8139ae2cca40e28c8cc585bbc75bd5',
      // access_key: '1Furfhe8BFbkEhXn1xcYPr8jYAACNpfV7p'
    }
  },
  // methods: {
  //   async updateSnapshots() {
  //     let url_list = this.jobs
  //     url_list.map(job => {
  //       fetch(`https://api.apiflash.com/v1/urltoimage?access_key=${this.access_key}&format=png&url=https://${job.url}`)
  //       .then(res => {
  //         console.log(res)
  //       })
  //     })
  //   }
  // },
  // mounted() {
  //   this.updateSnapshots()
  // }
}
</script>

<style>
.my-bg {
  background-color: #374151;
}

.job {
  @apply mb-10
   w-10/12 
   mx-auto 
  lg:ml-auto;
}

.job a:hover {
  @apply bg-gray-800;
}

a {
  color: white;
}

.firm {
  @apply font-bold
  my-1;
  color: #374151;
}

.job_description {
  @apply text-sm;
}
</style>