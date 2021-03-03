<template lang="pug">
v-container(fluid='' style='margin: 0px; padding: 0px; width: 100%;')
  v-layout(row='' wrap='')
    v-container(fluid='' style='margin: 0px; padding: 0px; width: 100%;background-color: #1b65c4;')
      v-row
        v-flex(xs12='',sm12='', md4='',lg4='',xl4='')
          v-img(src='../assets/aboutus_team.png' aspect-ratio='1.7')
        v-flex(xs12='',sm12='', md7='',lg7='',xl7='')    
          v-container()  
            h1.pa-3.mt-3(style="text-align: center;color:#fff") About Us
            h3.font-weight-regular.mb-n.pl-12.pr-12.mt-n2(style="text-align: left;color:#fff") {{desc1}}
            h3.font-weight-regular.mb-n.pl-12.pr-12.mt-2(style="text-align: left;color:#fff") {{desc2}}
    v-container()      
      h1.pa-3.rounded-lg.text-center(style="text-align: center;color:#000") GUIDING PRINCIPLES
      v-flex(v-for='item in items', :key='item.name',xs12='',sm12='', md12='',lg12='',xl12='')
        div.d-none.d-lg-flex.d-xl-flex.mt-2
        div(v-if="item.direction === 'left'")
          v-row
            v-flex(xs12='',sm12='', md4='',lg4='',xl4='')
              v-img.mt-5.ml-3.mr-n3(:src="item.src" contain aspect-ratio='2.5')
            v-flex(xs12='',sm12='', md8='',lg8='',xl8='')    
                v-container()  
                  h1.font-weight-medium.pa-3(style="text-align: center;color:#000") {{item.heading}}
                  h3.font-weight-light.mb-n.pa-3(style="text-align: center;color:#000") {{item.subheading}}   
        div(v-if="item.direction === 'right'")
          v-layout(v-if='$vuetify.breakpoint.smAndDown')
            v-row
              v-flex(xs12='',sm12='', md4='',lg4='',xl4='')
                v-img.mt-5.ml-n3.mr-3(:src="item.src" contain aspect-ratio='2.5')
              v-flex(xs12='',sm12='', md8='',lg8='',xl8='')    
                v-container()  
                  h1.font-weight-medium.pa-3(style="text-align: center;color:#000") {{item.heading}}
                  h3.font-weight-light.mb-n.pa-3(style="text-align: center;color:#000") {{item.subheading}}          
          v-layout(v-if='$vuetify.breakpoint.mdAndUp')          
            v-row
              v-flex(xs12='',sm12='', md8='',lg8='',xl8='')    
                v-container()  
                  h1.font-weight-medium.pa-3(style="text-align: center;color:#000") {{item.heading}}
                  h3.font-weight-light.mb-n.pa-3(style="text-align: center;color:#000") {{item.subheading}}
              v-flex(xs12='',sm12='', md4='',lg4='',xl4='')
                v-img.mt-5.ml-n3.mr-3(:src="item.src" contain aspect-ratio='2.5')    

</template>
<script>
export default {
  name: "Project",
  data: () => ({
    desc1:
      "Entrepreneurship-Cell IIT Jodhpur is a student body that focuses on developing and promoting entrepreneurial eco-system and start-up skills in creative and potential minds. It focuses on various dimensions of the corporate world that revolves around an entrepreneur. Being a student-run body, we educate people about different aspects of a business, guide and promote entrepreneurial ideas and provide resources to help them establish, nurture and run their own startup.",

    item: 1,
    items: [
      {
        direction: "right",
        heading: "Corporate, Startups and Marketing",
        src: "../data/images/AboutusPoints/point1new.png",
        subheading:
          "Everything we do is to upskill ourselves! We aim to learn and grow as a team!"
      },
      {
        direction: "left",
        heading: "Events",
        src: "../data/images/AboutusPoints/point2new.png",
        subheading:
          "Inspire and guide the coming generation to build a functioning and interactive open-source community."
      },
      {
        direction: "right",
        heading: "Finance and Management",
        src: "../data/images/AboutusPoints/finance.jpeg",
        subheading:
          "We at devlup labs are committed to products and projects that matter, projects that serve a real purpose for the community."
      },
      {
        direction: "left",
        heading: "Media and Publicity",
        src: "../data/images/AboutusPoints/media.jpg",
        subheading:
          "We insist on the highest of standards, from functionality to code to coffee."
      }
    ]
  })
};
</script>
