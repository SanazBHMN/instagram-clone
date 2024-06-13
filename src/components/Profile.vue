<script setup>
import Container from "./Container.vue";
import UserBar from "./UserBar.vue";
import ImageGallery from "./ImageGallery.vue";
</script>

<template>
  <Container>
    <div class="profile-container">
      <UserBar
        :username="'SanazBahmani'"
        :userInfo="{
          posts: 4,
          followers: 100,
          following: 300,
        }"
      />
      <ImageGallery
        :posts="[
          {
            id: 1,
            image:
              'https://img.pixers.pics/pho_wat(s3:700/FO/38/98/97/35/700_FO38989735_f91f2e4addad2e46d859153e02c6c0fd.jpg,700,686,cms:2018/10/5bd1b6b8d04b8_220x50-watermark.png,over,480,636,jpg)/wall-murals-happy-cartoon-monster.jpg.jpg',
          },
          {
            id: 2,
            image:
              'https://tophinhanhdep.com/wp-content/uploads/2021/10/Cartoon-Monster-Wallpapers.jpg',
          },
          {
            id: 3,
            image:
              'https://t3.ftcdn.net/jpg/02/17/31/70/360_F_217317087_pJpHTLb5eIyKwp7HNAfLw4sFVMPaRzc7.jpg',
          },
          {
            id: 4,
            image:
              'https://c8.alamy.com/comp/T8TBPC/happy-cartoon-monster-vector-halloween-illustration-big-set-of-cartoon-monsters-T8TBPC.jpg',
          },
          {
            id: 5,
            image:
              'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSV6XXUZjUQYpzqCg3PCG_N9Xise9HpeJBTPQ&s',
          },
        ]"
      />
    </div>
  </Container>
</template>

<style scoped>
.profile-container {
  display: flex;
  flex-direction: column;
  padding: 20px 0;
}
</style>
