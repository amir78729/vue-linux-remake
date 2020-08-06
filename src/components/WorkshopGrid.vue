<template>
  <div style="    border-bottom:5px solid rgb(242,169,56);">

<!--    <h1>{{items}}</h1>-->

    <h2 style="cursor: default">کارگاه‌ها و سخنرانی‌ها</h2>
    <div class="row align-content-center" style="padding: 0 80px 0 80px; justify-content: center">
      <div class="col-md-6 col-sm-12" v-for="item in items">
        <grid-workshop-item
        :title="item.title"
        :imageURL="item.imageURL"
        :teachers="item.teacher"></grid-workshop-item>
      </div>
    </div>
  </div>
</template>
<script>
  import WorkshopItem from "./WorkshopItem.vue";
  import data from "./../data/data.js"

  export default {
    components: {
      gridWorkshopItem: WorkshopItem,
    },
    data() {
      return {
        items: [
          {
            title: 'مقدماتی',
            teacher: [
              {
                teacherName: 'علیرضا بختیاری',
                teacherInfo: 'دانشجوی مهندسی کامپیوتر دانشگاه صنعتی امیرکبیر',
                teacherImageURL: '',
              },
              {
                teacherName: 'شایان شقفی',
                teacherInfo: 'دانشجوی مهندسی کامپیوتر دانشگاه صنعتی امیرکبیر',
                teacherImageURL: '',
              },
              {
                teacherName: 'محمد فاطمی',
                teacherInfo: 'دانشجوی مهندسی کامپیوتر دانشگاه صنعتی امیرکبیر',
                teacherImageURL: '',
              },
            ],
            imageURL: 'https://d341ezm4iqaae0.cloudfront.net/assets/2020/01/12193251/How-to-Run-Better-Office-Meetings-1.jpg',
          },
          {
            title: 'Docker',
            teacher: [
              {
                teacherName: 'احمد انواری',
                teacherInfo: 'Back-end Developer at Snapp, Bsc. Student at Amirkabir University of Technology, ارائه دهنده در سه دوره پیشین جشنواره لینوکس امیرکبیر و مدرس سایت مکتب خونه',
                teacherImageURL: '',
              },
            ],
            imageURL: 'https://cdn.hipwallpaper.com/i/72/14/7qMgZu.jpg',
          },
          {
            title: 'Cloud: A solution to infrastructure problem',
            teacher: [
              {
                teacherName: 'محمد کریمی',
                teacherInfo: 'Senior Cloud Engineer at Snapp, Former Site Reliability Engineer at Quiz of Kings and IT student at Amirkabir University of Technology',
                teacherImageURL: '',
              },
            ],
            imageURL: 'https://enterprise-cio.com/wp-content/uploads/sites/4/2020/03/cloud-database-over-computer-chip-moterboard-background-data-center-vector-id839394694.jpg',
          },
          {
            title: 'Kernel',
            teacher: [
              {
                teacherName: 'بهادر بخشی',
                teacherInfo: 'استاد دانشکده مهندسی کامپیوتر دانشگاه صنعتی امیرکبیر',
                teacherImageURL: '',
              },
            ],
            imageURL: 'https://tuxnews.it/wp-content/uploads/2017/05/kernel-4.12.jpg',
          },
          {
            title: 'Penetration Testing with Kali Linux',
            teacher: [
              {
                teacherName: 'احسان عدالت',
                teacherInfo: 'دانشجوی دکترای دانشکده مهندسی کامپیوتر دانشگاه امیرکبیر',
                teacherImageURL: '',
              },
            ],
            imageURL: 'https://raw.githubusercontent.com/dorianpro/kaliwallpapers/master/kali-linux-wallpaper-v4.png',
          },
          {
            title: 'Virtualization',
            teacher: [
              {
                teacherName: 'پرهام الوانی',
                teacherInfo: 'Back-end (Golang) Developer at Snapp, PhD Student at Amirkabir University of Technology',
                teacherImageURL: '',
              },
            ],
            imageURL: 'https://www.multapplied.net/wp-content/uploads/2019/11/header-virtualization-best-practice.jpg',
          },
          {
            title: 'Container Orchestration in Cloud',
            teacher: [
              {
                teacherName: 'امید رجب‌آقا',
                teacherInfo: 'Senior Cloud Engineer at Snapp. Former Site Reliability Engineer at Quiz of Kings',
                teacherImageURL: '',
              },
            ],
            imageURL: 'https://images5.alphacoders.com/874/874813.jpg',
          },
          {
            title: 'اسنپ‌کلود:‌ دلایل بنیادین و نحوه ساخت',
            teacher: [
              {
                teacherName: 'حسین مرادقلی',
                teacherInfo: 'Cloud Team Lead at Snapp, former CTO at Snapp',
                teacherImageURL: '',
              },
            ],
            imageURL: 'https://images.unsplash.com/photo-1536514498073-50e69d39c6cf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1951&q=80',
          },
          {
            title: 'Service Discovery',
            teacher: [
              {
                teacherName: 'محمد عبدلی‌راد',
                teacherInfo: 'Senior Software and DevOps Engineer at Snapp',
                teacherImageURL: '',
              },
              {
                teacherName: 'نرگس احمدی',
                teacherInfo: 'DevOps Engineer at Snapp, former Linux System Engineer at Ztel',
                teacherImageURL: '',
              },
            ],
            imageURL: 'http://thecookiezen.com/blog/images/ha-1.jpg',
          },
        ]
      }
    },
  }
</script>
<style scoped>
  h2 {
    margin: 50px;
    font-size: 36px;
    color: #521C39;
    text-align: center;
    font-weight: bolder;
  }
</style>
