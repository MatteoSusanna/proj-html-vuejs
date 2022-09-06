<template>
  <footer>
    <div class="footer-top">
      <div class="row">

        <!-- prima colonna footer -->
        <div class="col abount" v-for="(abount, indice) in abount" :key="indice">
          <h3>ABOUT US</h3>
          <div class="ptb">{{abount.descrizione}}</div>
          <img class="img" :src="abount.url" alt="logo">
        </div>

        <!-- seconda colonna footer -->
        <div class="col archivies">
          <h3 class="pb-20">Archives</h3>
          <ul>
            <li v-for="(archivio ,indice) in archives" :key="indice">
              {{archivio.data}} {{archivio.quantita}}
            </li>
          </ul>
        </div>

        <!-- terza colonna footer -->
        <div class="col featuras">
          <h3>OUR FEATURAS</h3>
          <div class="ptb">Nunc gravida rutrum mauris vehim hasellus ac pretium augue vivamul lacus ligul mattis ac vene</div>
          <ul>
            <li v-for="(feature,indice) in features" :key="indice">
              <img src="../assets/img/style_4_alt.png" alt="ceck">
              {{feature.voce}}
            </li>
          </ul>
        </div>

        <!-- quarta colonna footer -->
        <div class="col posts">
          <h3 class="pb-20">RECENT POSTS</h3>
          <div class="card" v-for="(post, indice) in recentPosts" :key="indice">
            <div class="wrapper-img">
              <img :src="post.url" alt="bambini">
            </div>
            <div class="text">
              <h3>{{post.attivita}}</h3>
              <div class="d-flex">
                <img class="mr-10" src="../assets/img/date_footer.png" alt="calendario">
                <div>{{post.data}}</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="footer-bot">
      <ul class="d-flex">
        <li class="d-flex" v-for="(social ,indice) in socialFooter" :key="indice">
          <img :src="social" alt="social">
        </li>
      </ul>
      <p class="text-center pt">&copy;Fable-Children Kindergarten WordPress Theme by QuanticaLabs</p>
    </div>
  </footer>
</template>

<script>
export default {
    nome: 'MyFooter',
    data(){
      return{
          abount: [
                    {
                      descrizione: 'Elipsis magna a nulla elite forte maecenas est elementum magna etos interdum movum morbi vehicula morbi',
                      url: require('../assets/img/logo_footer.png'),
                    },
                  ],
          archives: [
                      {
                        data: 'OCTOBER 2014',
                        quantita: '(2)',
                      },
                      {
                        data: 'SEPTEMBER 2014',
                        quantita: '(2)',
                      },
                      {
                        data: 'AUGUST 2014',
                        quantita: '(2)',
                      },
                      {
                        data: 'JULLY 2014',
                        quantita: '(2)',
                      },
                      {
                        data: 'JUNE 2014',
                        quantita: '(2)',
                      },
                      {
                        data: 'MAY 2014',
                        quantita: '(1)',
                      },
                    ],
          features: [
                      {
                        voce: 'Friendly and welcoming place'
                      },
                      {
                        voce: 'Science and art classes'
                      },
                      {
                        voce: 'Positive learning environment'
                      },
                      {
                        voce: 'Educational field trips'
                      },
                      {
                        voce: 'Writing and reading classes'
                      },
                      {
                        voce: 'Science and art classes'
                      },
                    ],
          recentPosts:  [
                          {
                            url: require('../assets/img/blog_09-150x150.jpg'),
                            attivita: 'Drawing',
                            data: 'October 2014',
                          },
                          {
                            url: require('../assets/img/blog_10-150x150.jpg'),
                            attivita: 'Meeting day',
                            data: 'October 2014',
                          },
                          {
                            url: require('../assets/img/blog_08-150x150.jpg'),
                            attivita: 'Birthday',
                            data: 'September 2014',
                          },
                        ],
        socialFooter: [
                        require('../assets/img/behance.png'),
                        require('../assets/img/dribbble.png'),
                        require('../assets/img/envato.png'),
                        require('../assets/img/facebook.png'),
                        require('../assets/img/twitter.png'),

                      ]
      }
    },
}
</script>

<style scoped lang="scss">
@import '../style/general.scss';
.col{
  width: calc(100% / 4 - 1rem);
    .img{
      width: 100%;
    }
}
ul{
      li{
        list-style: none;
      }
    }


footer{
  .footer-top{
    padding: 30px;
    color: white;
    background-image: url('../assets/img/pattern.png');
      .row{
        display: flex;
        justify-content: space-between;
        width: 1000px;
        margin: 0 auto;
        .archivies{
          ul{
            li{

              border: 1px solid white;
              padding: 15px;
              margin: 5px 0;
            }
          }
        }
        .featuras{
          ul{
            li{
              margin: 5px 0;
            }
          }
        }
        .posts{
          .card{
            display: flex;
            margin-bottom: 15px;
            .wrapper-img{
              height: 100px;
              width: 100px;
              img{
                width: 100%;
              }
            }
            .text{
              display: flex;
              flex-direction: column;
              justify-content: space-between;
              margin-left: 10px;
            }
          }
        }
      }
  }
  .footer-bot{
    height: 150px;
    padding: 10px;
    ul{
      display: flex;
      li{
        height: 60px;
        width: 60px;
        background-color: $blaze_orange;
        margin-left: 5px;
      };
    }
  }
}


</style>