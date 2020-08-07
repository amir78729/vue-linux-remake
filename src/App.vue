<template>
  <div>
    <app-header style="position: fixed; width: 100%" class="always-on-top"></app-header>
<!--    <app-event-title></app-event-title>-->
<!--    <app-about-event></app-about-event>-->
<!--    <app-workshop-grid :items="items"></app-workshop-grid>-->
<!--    <app-snapp></app-snapp>-->
    <app-workshop-component :data="items"></app-workshop-component>
  </div>
</template>

<script>
  import Header from "./components/Header.vue";
  import EventTitle from "./components/EventTitle.vue";
  import AboutEvent from "./components/AboutEvent.vue";
  import WorkshopGrid from "./components/WorkshopGrid.vue";
  import Snapp from "./components/Snapp.vue";
  import WorkshopComponent from "./components/workshop info/WorkshopComponent.vue"



  export default {

    components: {
      appHeader: Header,
      appEventTitle: EventTitle,
      appAboutEvent: AboutEvent,
      appWorkshopGrid: WorkshopGrid,
      appSnapp: Snapp,
      appWorkshopComponent: WorkshopComponent,
    },
    data() {
      return {
        items: [
          {
            title: 'مقدماتی',
            info: 'Day 1:\n' +
              'What is linux\n' +
              'History of linux\n' +
              'Linux distributions\n' +
              'Installing linux on a virtual machine\n' +
              'Day 2:\n' +
              'Linux directory structure\n' +
              'using shell\n' +
              'shell builtins and aliases\n' +
              'ENV variables\n' +
              'finding your way in shell ( man and help )\n' +
              'commonly used shell commands\n' +
              'manipulating files and directories\n' +
              'list files and directories\n' +
              'finding and searching for files\n' +
              'deleting, copying and moving files\n' +
              'wildcards\n' +
              'permissions\n' +
              'working with text files\n' +
              'reading and processing text files\n' +
              'editing text files and streams\n' +
              'I/O and redirection\n' +
              'Day 3:\n' +
              'Installing and managing packages\n' +
              'using apt\n' +
              'dpkg and it\'s usages\n' +
              'Users and Groups\n' +
              'Cron and automation\n' +
              'cron jobs\n' +
              'rc files\n' +
              'Manipulating processes\n' +
              'process structure\n' +
              'killing a process\n' +
              'start a job in the background\n' +
              'Networking',
            time: '1. چهارشنبه 1398/11/30 | ساعت: 16:00 تا 19:00\n' +
              '\n' +
              '2. پنج‌شنبه 1398/12/01 | ساعت: 09:30 تا 17:00\n' +
              '\n' +
              '3. جمعه 1398/12/02 | ساعت: 09:30 تا 17:00',
            price: '500000 ریال',
            teacher: [
              {
                teacherName: 'علیرضا بختیاری',
                teacherInfo: 'دانشجوی مهندسی کامپیوتر دانشگاه صنعتی امیرکبیر',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae4fcc726a17d72f5a75f/mainPic.png',
              },
              {
                teacherName: 'شایان شقفی',
                teacherInfo: 'دانشجوی مهندسی کامپیوتر دانشگاه صنعتی امیرکبیر',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae507c726a17d72f5a760/mainPic.png',
              },
              {
                teacherName: 'محمد فاطمی',
                teacherInfo: 'دانشجوی مهندسی کامپیوتر دانشگاه صنعتی امیرکبیر',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae51ac726a17d72f5a761/mainPic.png',
              },
            ],
            imageURL: 'https://d341ezm4iqaae0.cloudfront.net/assets/2020/01/12193251/How-to-Run-Better-Office-Meetings-1.jpg',
          },
          {
            title: 'Docker',
            info: '',
            time: '',
            price: '',
            teacher: [
              {
                teacherName: 'احمد انواری',
                teacherInfo: 'Back-end Developer at Snapp, Bsc. Student at Amirkabir University of Technology, ارائه دهنده در سه دوره پیشین جشنواره لینوکس امیرکبیر و مدرس سایت مکتب خونه',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae529c726a17d72f5a762/mainPic.png',
              },
            ],
            imageURL: 'https://cdn.hipwallpaper.com/i/72/14/7qMgZu.jpg',
          },
          {
            title: 'Cloud: A solution to infrastructure problem',
            info: '',
            time: '',
            price: '',
            teacher: [
              {
                teacherName: 'محمد کریمی',
                teacherInfo: 'Senior Cloud Engineer at Snapp, Former Site Reliability Engineer at Quiz of Kings and IT student at Amirkabir University of Technology',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae568c726a17d72f5a766/mainPic.png',
              },
            ],
            imageURL: 'https://enterprise-cio.com/wp-content/uploads/sites/4/2020/03/cloud-database-over-computer-chip-moterboard-background-data-center-vector-id839394694.jpg',
          },
          {
            title: 'Kernel',
            info: '',
            time: '',
            price: '',
            teacher: [
              {
                teacherName: 'بهادر بخشی',
                teacherInfo: 'استاد دانشکده مهندسی کامپیوتر دانشگاه صنعتی امیرکبیر',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae542c726a17d72f5a763/mainPic.png',
              },
            ],
            imageURL: 'https://tuxnews.it/wp-content/uploads/2017/05/kernel-4.12.jpg',
          },
          {
            title: 'Penetration Testing with Kali Linux',
            info: '',
            time: '',
            price: '',
            teacher: [
              {
                teacherName: 'احسان عدالت',
                teacherInfo: 'دانشجوی دکترای دانشکده مهندسی کامپیوتر دانشگاه امیرکبیر',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae55bc726a17d72f5a765/mainPic.png',
              },
            ],
            imageURL: 'https://raw.githubusercontent.com/dorianpro/kaliwallpapers/master/kali-linux-wallpaper-v4.png',
          },
          {
            title: 'Virtualization',
            info: '',
            time: '',
            price: '',
            teacher: [
              {
                teacherName: 'پرهام الوانی',
                teacherInfo: 'Back-end (Golang) Developer at Snapp, PhD Student at Amirkabir University of Technology',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae54dc726a17d72f5a764/mainPic.png',
              },
            ],
            imageURL: 'https://www.multapplied.net/wp-content/uploads/2019/11/header-virtualization-best-practice.jpg',
          },
          {
            title: 'Container Orchestration in Cloud',
            info: '',
            time: '',
            price: '',
            teacher: [
              {
                teacherName: 'امید رجب‌آقا',
                teacherInfo: 'Senior Cloud Engineer at Snapp. Former Site Reliability Engineer at Quiz of Kings',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae57cc726a17d72f5a768/mainPic.png',
              },
            ],
            imageURL: 'https://images5.alphacoders.com/874/874813.jpg',
          },
          {
            title: 'اسنپ‌کلود:‌ دلایل بنیادین و نحوه ساخت',
            info: '',
            time: '',
            price: '',
            teacher: [
              {
                teacherName: 'حسین مرادقلی',
                teacherInfo: 'Cloud Team Lead at Snapp, former CTO at Snapp',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae574c726a17d72f5a767/mainPic.png',
              },
            ],
            imageURL: 'https://images.unsplash.com/photo-1536514498073-50e69d39c6cf?ixlib=rb-1.2.1&auto=format&fit=crop&w=1951&q=80',
          },
          {
            title: 'Service Discovery',
            info: '',
            time: '',
            price: '',
            teacher: [
              {
                teacherName: 'محمد عبدلی‌راد',
                teacherInfo: 'Senior Software and DevOps Engineer at Snapp',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae587c726a17d72f5a769/mainPic.png',
              },
              {
                teacherName: 'نرگس احمدی',
                teacherInfo: 'DevOps Engineer at Snapp, former Linux System Engineer at Ztel',
                teacherImageURL: 'http://skillcenter.aut.ac.ir/linuxfestapi/uploads/2019/teachers/5e3ae596c726a17d72f5a76a/mainPic.png',
              },
            ],
            imageURL: 'http://thecookiezen.com/blog/images/ha-1.jpg',
          },
        ]
      }
    },
}
</script>

<style>
  body {
    font-family: 'iransans';
  }
  .always-on-top {
    z-index: 999999 !important;
  }
</style>
