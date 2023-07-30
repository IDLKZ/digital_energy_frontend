<template>
  <div class="container mx-auto py-[60px]">
    <!-- Container for demo purpose -->
    <div class="container my-24 mx-auto md:px-6">
      <!-- Section: Design Block -->
      <section class="mb-32 text-center">
        <h2 class="mb-12 text-3xl font-bold">
          Наша <u class="text-primary dark:text-primary-400">команда</u>
        </h2>

        <div class="grid gap-x-6 md:grid-cols-3 lg:gap-x-12">
          <div class="mb-6 lg:mb-0">
            <div
              class="block rounded-lg bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700">
              <div class="relative overflow-hidden bg-cover bg-no-repeat">
<!--                <img src="https://mdbcdn.b-cdn.net/img/new/avatars/6.jpg" class="w-full rounded-t-lg" />-->
                <div class="bg-img" :style="{ backgroundImage: `url(${require('@/assets/images/gosman.JPG')})` }"></div>
                <a v-on:click="showDetail(1)" href="#!">
                  <div class="absolute top-0 right-0 bottom-0 left-0 h-full w-full overflow-hidden bg-fixed"></div>
                </a>
                <svg class="absolute text-white dark:text-neutral-700 left-0 bottom-0" xmlns="http://www.w3.org/2000/svg"
                     viewBox="0 0 1440 320">
                  <path fill="currentColor"
                        d="M0,288L48,272C96,256,192,224,288,197.3C384,171,480,149,576,165.3C672,181,768,235,864,250.7C960,267,1056,245,1152,250.7C1248,256,1344,288,1392,304L1440,320L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
                  </path>
                </svg>
              </div>
              <div class="p-6">
                <h5 class="mb-4 text-lg font-bold">Амрин Госман Каримович</h5>
                <p v-on:click="showDetail(1)" class="cursor-pointer mb-4 text-neutral-500 dark:text-neutral-300">Председатель Попечительского совета, со-основатель Ассоциации</p>
                <p v-if="gosman" class="mb-4 text-neutral-500 dark:text-neutral-300">
                  Обладает огромным опытом управленческой работы в государственных и национальных компаниях. В различные годы работал Президентом АО «Центр инжиниринга и трансферта технологий», Первым вице-министром индустрии и торговли Республики Казахстан, Председателем правления АО «Национальный инновационный фонд». Также имеет ряд государственных медалей.
                </p>
<!--                <ul class="mx-auto flex list-inside justify-center">-->
<!--                  <a href="#!" class="px-2">-->
<!--                    &lt;!&ndash; GitHub &ndash;&gt;-->
<!--                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"-->
<!--                         class="h-4 w-4 text-primary dark:text-primary-400">-->
<!--                      <path fill="currentColor"-->
<!--                            d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />-->
<!--                    </svg>-->
<!--                  </a>-->
<!--                  <a href="#!" class="px-2">-->
<!--                    &lt;!&ndash; Twitter &ndash;&gt;-->
<!--                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"-->
<!--                         class="h-4 w-4 text-primary dark:text-primary-400">-->
<!--                      <path fill="currentColor"-->
<!--                            d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" />-->
<!--                    </svg>-->
<!--                  </a>-->
<!--                  <a href="#!" class="px-2">-->
<!--                    &lt;!&ndash; Linkedin &ndash;&gt;-->
<!--                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"-->
<!--                         class="h-3.5 w-3.5 text-primary dark:text-primary-400">-->
<!--                      <path fill="currentColor"-->
<!--                            d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z" />-->
<!--                    </svg>-->
<!--                  </a>-->
<!--                </ul>-->
              </div>
            </div>
          </div>

          <div class="mb-6 lg:mb-0">
            <div
              class="block rounded-lg bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700">
              <div class="relative overflow-hidden bg-cover bg-no-repeat">
<!--                <img src="https://mdbcdn.b-cdn.net/img/new/avatars/8.jpg" class="w-full rounded-t-lg" />-->
                <div class="bg-img" :style="{ backgroundImage: `url(${require('@/assets/images/kanat.jpeg')})` }"></div>
                <a v-on:click="showDetail(2)" href="#!">
                  <div class="absolute top-0 right-0 bottom-0 left-0 h-full w-full overflow-hidden bg-fixed"></div>
                </a>
                <svg class="absolute text-white dark:text-neutral-700  left-0 bottom-0" xmlns="http://www.w3.org/2000/svg"
                     viewBox="0 0 1440 320">
                  <path fill="currentColor"
                        d="M0,96L48,128C96,160,192,224,288,240C384,256,480,224,576,213.3C672,203,768,213,864,202.7C960,192,1056,160,1152,128C1248,96,1344,64,1392,48L1440,32L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
                  </path>
                </svg>
              </div>
              <div class="p-6">
                <h5 class="mb-4 text-lg font-bold">Кудайберген Канат Жакыпулы</h5>
                <p v-on:click="showDetail(2)" class="cursor-pointer mb-4 text-neutral-500 dark:text-neutral-300">Член Попечительского совета, со-основатель Ассоциации</p>
                <p v-if="kanat" class="mb-4 text-neutral-500 dark:text-neutral-300">
                  Обладая выдающимся опытом в металлургии и горнодобывающей промышленности в Казахстане, г-н Кудайберген обладает экспертными знаниями и долгосрочным видением того, что мы называем возможностями на всю жизнь в отрасли. Его навыки стратегического и оперативного управления были усовершенствованы во время работы в НАК «Казатомпром» в качестве генерального директора ряда дочерних компаний. Занимал должность генерального директора ГК «Тау-Кен Самрук» до создания GWM.
                </p>
              </div>
            </div>
          </div>

          <div class="">
            <div
              class="block rounded-lg bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700">
              <div class="relative overflow-hidden bg-cover bg-no-repeat">
<!--                <img src="https://mdbcdn.b-cdn.net/img/new/avatars/15.jpg" class="w-full rounded-t-lg" />-->
                <div class="bg-img" :style="{ backgroundImage: `url(${require('@/assets/images/zhanna.png')})` }"></div>
                <a v-on:click="showDetail(3)" href="#!">
                  <div class="absolute top-0 right-0 bottom-0 left-0 h-full w-full overflow-hidden bg-fixed"></div>
                </a>
                <svg class="absolute text-white dark:text-neutral-700 left-0 bottom-0" xmlns="http://www.w3.org/2000/svg"
                     viewBox="0 0 1440 320">
                  <path fill="currentColor"
                        d="M0,288L48,256C96,224,192,160,288,160C384,160,480,224,576,213.3C672,203,768,117,864,85.3C960,53,1056,75,1152,69.3C1248,64,1344,32,1392,16L1440,0L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
                  </path>
                </svg>
              </div>
              <div class="p-6">
                <h5 class="mb-4 text-lg font-bold">Утарбаева Жанна</h5>
                <p v-on:click="showDetail(3)" class="cursor-pointer mb-4 text-neutral-500 dark:text-neutral-300">Член Попечительского совета, со-основатель Ассоциации</p>
                <p v-if="zhanna" class="mb-4 text-neutral-500 dark:text-neutral-300">
                  Является кандидатом философских наук, владелец IT компании «Digital Transformation Consulting». В нефтегазовом секторе Казахстана г-жа Утарбаева проработала более 20 лет. Она была первым PR руководителем в Казахстане, который готовил выход государственной энергетической компании «KEGOC» на Лондонский IPO. Несколько лет г-жа Утарбаева была координатором Электроэнергетического Совета Казахстана и Центральной Азии. В разные годы занимала руководящие позиции в АО НК «КазМунайГаз», ЗАО «KazMunaiTeniz», АО НГСК «КазСтроСервис». За 20 лет работы руковолителем GR и PR в нефтегазовой отрасли Казахстана г-жа Утарбаева реализовала более 100 международных проектов, получив уважение и признание от коллег по отрасли. За успешную реализацию международных проектов г-жа Утарбаева удостоилась награды американского журнала Hollywood Tribute. В марте 2023 году госпожа Утарбана получила звание «Коуч Года» по версии журнала Teens &People. В этом же году она получила звание «Бизнес вумен года» в Узбекистане по версии агентства «N1 Corporation». За вклад в развитие Казахстана госпожа Утарбаева вошла в национальную энциклопедию «Лучшие женщины Казахстана».
                </p>
              </div>
            </div>
          </div>
        </div>

        <div class="grid gap-x-6 md:grid-cols-3 lg:gap-x-12 mt-5">
          <div class="mb-6 lg:mb-0">
            <div
              class="block rounded-lg bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700">
              <div class="relative overflow-hidden bg-cover bg-no-repeat">
<!--                <img src="https://mdbcdn.b-cdn.net/img/new/avatars/6.jpg" class="w-full rounded-t-lg" />-->
                <div class="bg-img" :style="{ backgroundImage: `url(${require('@/assets/images/olzhas.png')})` }"></div>
                <a v-on:click="showDetail(4)" href="#!">
                  <div class="absolute top-0 right-0 bottom-0 left-0 h-full w-full overflow-hidden bg-fixed"></div>
                </a>
                <svg class="absolute text-white dark:text-neutral-700 left-0 bottom-0" xmlns="http://www.w3.org/2000/svg"
                     viewBox="0 0 1440 320">
                  <path fill="currentColor"
                        d="M0,288L48,272C96,256,192,224,288,197.3C384,171,480,149,576,165.3C672,181,768,235,864,250.7C960,267,1056,245,1152,250.7C1248,256,1344,288,1392,304L1440,320L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
                  </path>
                </svg>
              </div>
              <div class="p-6">
                <h5 class="mb-4 text-lg font-bold">Худайбергенов Олжас Абдумаликович</h5>
                <p v-on:click="showDetail(4)" class="cursor-pointer mb-4 text-neutral-500 dark:text-neutral-300">Член Попечительского совета, со-основатель Ассоциации</p>
                <p v-if="olzhas" class="cursor-pointer mb-4 text-neutral-500 dark:text-neutral-300">
                  Является высококвалифицированным экономистом Казахстана, обладает большим опытом управленческой работы в различных секторах экономики. В разные годы работал в государственном секторе, был членом Центра анализа мониторинга социально-экономических реформ при Президенте Республики Казахстан и внештатным советником Президента Республики Казахстан по экономическим вопросам. Является старшим партнером консалтинговой компании «Center for strategic initiatives» и Председателем Управляющего совета при Министерстве нацэкономики РК. Работа совета нацелена на достижение результатов по основным направлениям новой экономической политики Казахстана.
                </p>
              </div>
            </div>
          </div>

          <div class="mb-6 lg:mb-0">
            <div
              class="block rounded-lg bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700">
              <div class="relative overflow-hidden bg-cover bg-no-repeat">
<!--                <img src="https://mdbcdn.b-cdn.net/img/new/avatars/8.jpg" class="w-full rounded-t-lg" />-->
                <div class="bg-img" :style="{ backgroundImage: `url(${require('@/assets/images/bakitzhan.jpeg')})` }"></div>
                <a v-on:click="showDetail(5)" href="#!">
                  <div class="absolute top-0 right-0 bottom-0 left-0 h-full w-full overflow-hidden bg-fixed"></div>
                </a>
                <svg class="absolute text-white dark:text-neutral-700  left-0 bottom-0" xmlns="http://www.w3.org/2000/svg"
                     viewBox="0 0 1440 320">
                  <path fill="currentColor"
                        d="M0,96L48,128C96,160,192,224,288,240C384,256,480,224,576,213.3C672,203,768,213,864,202.7C960,192,1056,160,1152,128C1248,96,1344,64,1392,48L1440,32L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z">
                  </path>
                </svg>
              </div>
              <div class="p-6">
                <h5 class="mb-4 text-lg font-bold">Ильяс Бакытжан Нассенулы</h5>
                <p v-on:click="showDetail(5)" class="cursor-pointer mb-4 text-neutral-500 dark:text-neutral-300">Председатель Ассоциации</p>
                <p v-if="bakitzhan" class="mb-4 text-neutral-500 dark:text-neutral-300">
                  Обладает большим опытом работы в энергетической отрасли Казахстане. Работал руководителем в ряде энергетических компаниях частного и государственного секторов. Занимал должность Председателя Правления АО «Казахстанский оператор рынка электрической энергии и мощности», организовывал работу первого Отраслевого центра технологической компетенций в сфере электроэнергетики Министерства энергетики РК.
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!-- Section: Design Block -->
    </div>

  </div>
</template>

<script>

export default {
  name: "teams",
  data() {
    return {
      zhanna: false,
      gosman: false,
      kanat: false,
      olzhas: false,
      bakitzhan: false,
      zhannaImg: '~/assets/images/zhanna.png'
    }
  },
  methods: {
    showDetail(id) {
      switch (id) {
        case 1:
          this.gosman = !this.gosman
          break;
        case 2:
          this.kanat = !this.kanat
          break
        case 3:
          this.zhanna = !this.zhanna
          break
        case 4:
          this.olzhas = !this.olzhas
          break
        case 5:
          this.bakitzhan = !this.bakitzhan
          break
        default:
          console.log('')
      }
    }
  }
}
</script>

<style scoped>
  .bg-img {
    background-size: cover!important;
    width: 100%;
    height: 400px;
    background-repeat: no-repeat!important;
    background-position: center!important;
  }
</style>
