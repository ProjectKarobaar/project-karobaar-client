<template>
  <div class="container">
    <vs-card v-for="(member, index) in members" :key="index" type="1">
      <template #title>
        <h3>{{ member.name }}</h3>
      </template>
      <template #img>
        <img :src="member.img" alt="" />
      </template>
      <template #text>
        <p>{{ member.role }}</p>
      </template>
      <template #interactions>
        <a :href="member.insta" target="_blank">
          <vs-button danger icon>
            <img class="insta" src="instagram.svg" />
          </vs-button>
        </a>
      </template>
    </vs-card>
  </div>
</template>

<script>
export default {
  name: 'Team',
  data() {
    return {
      members: [
        {
          name: 'Pruthvi Shetty',
          role: 'Frontend, Backend',
          img: 'team/pruthvi.png',
          insta: 'https://www.instagram.com/p_ruth_vi/',
        },
        {
          name: 'Soham Tamboli',
          role: 'Frontend, Design',
          img: 'team/soham.png',
          insta: 'https://www.instagram.com/soham_tamboli/',
        },
        {
          name: 'Mitanshu Salvi',
          role: 'Design, AR/3D',
          img: 'team/mitanshu.png',
          insta: 'https://www.instagram.com/mitanshu_salvi/',
        },
        {
          name: 'Huzaif Quazi',
          role: 'Backend, CI/CD',
          img: 'team/huzaif.png',
          insta: 'https://www.instagram.com/qazi_958/',
        },
        {
          name: 'Shubhangi Mohite',
          role: 'Blockchain, Data Analysis',
          img: 'team/shubhangi.png',
          insta: 'https://www.instagram.com/_shubhangi_mohite/',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.container {
  display: grid;
  width: 80%;
  margin: 0 auto;
  place-items: center;
  gap: 1.5rem;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
}
.insta {
  width: 20px;
  height: 20px;
}
</style>
