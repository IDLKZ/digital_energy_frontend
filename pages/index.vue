<template>
  <section>
    <!--    First bloc-->
    <section class="darken-bg">
      <div class="container mx-auto min-h-screen md:min-h-[80vh] flex items-center px-4">
        <div class="grid grid-cols-12 fle gap-4">
          <div class="col-span-12 md:col-span-6 text-center md:text-left">
            <p class="text-5xl text-white font-bold">
              Digital Energy
            </p>
            <p class="mt-8 text-xl text-white">
              Мы будем укреплять наши ценности <br>
              трудолюбия и ответственности, уважения к<br>
              Человеку Труда, создавая условия для<br>
              реализации созидательного потенциала <br>
              каждого гражданина страны.<br>
            </p>
            <div class="py-8">
              <button type="button" class="px-8 text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100  rounded-lg font-bold text-lg px-5 py-2.5 mr-2 mb-2 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600">
                Связь с нами
              </button>
            </div>

          </div>
        </div>
      </div>
    </section>
    <!-- First Bloc-->

    <!--    Second bloc-->
    <section class="custom-gray-bg">
      <div class="container mx-auto py-[20px] md:py-[100px] px-4">
        <div class="grid grid-cols-12 gap-4">
          <div class="col-span-12 px-4 md:col-span-7 text-center md:text-left">
            <p class="text-3xl md:text-4xl text-black font-bold">
              Об Ассоциации
            </p>
            <span class="mt-2 mb-4 w-[10%] h-[8px] bg-[#01bcfb] inline-block"></span>

            <p class="mt-4 pt-2 text-lg md:text-xl text-black" v-for="textAssociationItem of textAssociation">
              {{textAssociationItem}}
            </p>


            <div class="py-8">
              <button type="button" class="blue-gradient-button px-8 text-white bg-white border   rounded-lg font-bold text-lg px-5 py-2.5 mr-2 mb-2">
                Подробнее о нас
              </button>
            </div>
          </div>
          <div class="col-span-12 md:col-span-5">
            <ssr-carousel :responsive="slider_card_option" show-dots>
              <div class="slide">
                <div class="flex justify-center items-center">
                  <div
                    class="
                    py-4
                    px-8
                    flex items-end
                    card rounded-2xl
                    min-h-[500px] max-w-[350px] w-[350px] h-[500px]
                    bg-no-repeat bg-center bg-cover
                    bg-[url('~/assets/images/card_1.png')]
                    ">
                    <div>
                      <p class="text-2xl text-white font-bold my-2">
                        Объект 1
                      </p>
                      <p class="text-md text-white  my-2">
                        Все достижения и успехи страны – результат каждодневного, кропотливого труда всех казахстанцев.
                      </p>
                      <a href="" class="text-lg text-white font-bold my-2">
                        Подробнее >
                      </a>
                    </div>
                  </div>
                </div>
              </div>
              <div class="slide">
                <div class="flex justify-center items-center">
                  <div
                    class="
                    py-4
                    px-8
                    flex items-end
                    card rounded-2xl
                    min-h-[500px] max-w-[350px] w-[350px] h-[500px]
                    bg-no-repeat bg-center bg-cover
                    bg-[url('~/assets/images/card_2.png')]
                    ">
                    <div>
                      <p class="text-2xl text-black font-bold my-2">
                        Объект 2
                      </p>
                      <p class="text-md text-black  my-2">
                        Все достижения и успехи страны – результат каждодневного, кропотливого труда всех казахстанцев.
                      </p>
                      <a href="" class="text-lg text-black font-bold my-2">
                        Подробнее >
                      </a>
                    </div>
                  </div>
                </div>
              </div>

            </ssr-carousel>
          </div>
        </div>
      </div>
    </section>
    <!-- Second Bloc-->

    <!--    Third bloc-->
    <section>
      <div class="container mx-auto py-[20px] md:py-[100px] px-4">
        <div class="grid grid-cols-12 gap-4">
          <div class="col-span-12 px-4 md:col-span-12 text-center md:text-left">
            <p class="text-3xl md:text-4xl text-black font-bold">
              Ключевые задачи
            </p>
            <span class="mt-2 mb-4 w-[10%] h-[8px] bg-[#01bcfb] inline-block"></span>
          </div>
        </div>
        <div class="grid grid-cols-12 gap-4 my-[50px]">
          <div class="col-span-12 px-4 md:col-span-6 text-center md:text-left">
            <p class="text-2xl md:text-3xl text-black font-bold text-[#01bcfb]">
              1 задача
            </p>
            <p class="text-xl md:text-2xl text-black font-bold my-[10px]">
              Представление и защита интересов членов Ассоциации.
            </p>
            <p class="my-[20px]">
              Ассоциация защищает имущественные интересы  ее членов и выступает координатором деятельности субъектов энергетической отрасли по формированию консолидированной позиции по цифровому и технологическому развитию отрасли, моделированию направлений развития отрасли для совершенствования технологий и бизнес-процессов, путем создания на площадке Ассоциации условий для агрегирования профессиональной экспертизы, исследований технологий, решений и продуктов, имеющих успешный опыт промышленного использования в Казахстане и за её пределами.
            </p>
          </div>
          <div class="col-span-12 px-4 md:col-span-6 text-center md:text-left flex justify-center items-center">
            <img src="~/assets/images/icon_1.png">
          </div>
        </div>
        <div class="grid grid-cols-12 gap-4 my-[50px]">
          <div class="col-span-12 px-4 md:col-span-6 text-center md:text-left flex justify-center items-center">
            <img src="~/assets/images/icon_2.png">
          </div>
          <div class="col-span-12 px-4 md:col-span-6 text-center md:text-left">
            <p class="text-2xl md:text-3xl text-black font-bold text-[#01bcfb]">
              2 задача
            </p>
            <p class="text-xl md:text-2xl text-black font-bold my-[10px]">
              Улучшение регуляторной среды для технологического развития
            </p>
            <p class="my-[20px]">
              Ассоциация участвует в разработке и внесение в органы государственной власти, предложений по доктринальным документам (стратегии цифровой трансформации отрасли) и планам их реализации, по законопроектам и нормативным документам, по модели управления технологиями, данными и кибербезопасностью в отрасли, позволяющей осуществлять эффективное взаимодействие субъектов отрасли с регуляторами, по повышению прозрачности и эффективности управления и государственного контроля, с учетом интересов членов Ассоциации и общественности (конечных потребителей услуг и энергоресурсов).
            </p>
          </div>
        </div>
        <div class="grid grid-cols-12 gap-4 my-[50px]">
          <div class="col-span-12 px-4 md:col-span-6 text-center md:text-left">
            <p class="text-2xl md:text-3xl text-black font-bold text-[#01bcfb]">
              3 задача
            </p>
            <p class="text-xl md:text-2xl text-black font-bold my-[10px]">
              Развитие отраслевой компетенции в передовых технологиях.
            </p>
            <p class="my-[20px]">
              Ассоциация является площадкой для объединения усилий отраслевого бизнес-сообщества и товаропроизводителей, научно-исследовательских и образовательных организаций, сообществ информационных технологий и технологических акселераторов, органов государственной власти и международных организаций, объединений юридических лиц и общественных организаций, а также иных вовлеченных в цифровую трансформацию сообществ и организаций, для координации деятельности направленных на формирование агрегированной позиции по технологическому развитию отрасли и развитию отраслевой компетенции с сфере передовых технологий.
            </p>
          </div>
          <div class="col-span-12 px-4 md:col-span-6 text-center md:text-left flex justify-center items-center">
            <img src="~/assets/images/icon_3.png">
          </div>
        </div>
      </div>
    </section>
    <!-- Third Bloc-->
    <!--    Fourth bloc-->
    <section>
      <div class="container-full py-[50px]">
        <div class="min-h-[80vh] darken-slide-bg">
          <div class="container mx-auto">
            <div class="grid grid-cols-12 gap-4 py-20 px-4">
              <div class="col-span-12 md:col-span-6 text-center md:text-left">
                <ssr-carousel :slides-per-page='1' show-dots loop show-arrows>
                  <div class="slide">
                    <p class="text-3xl md:text-4xl text-white font-bold">
                      Новости
                    </p>
                    <span class="mt-2 mb-4 w-[10%] h-[8px] bg-[#01bcfb] inline-block"></span>
                    <p class="text-2xl md:text-3xl text-white font-bold">
                      Зависящая от импорта электричества Литва рассчитывает на солидарность соседей
                    </p>
                    <p class="text-md md:text-lg my-5 text-white">
                      Несмотря на тенденцию к замедлению, корейские инвестиции во Вьетнам в ближайшее время увеличатся, включая многие крупномасштабные проекты, до миллиардов долларов США.Проект на миллиард долларов ждетВ рамках Вьетнамско-корейского бизнес-форума, состоявшегося в выходные дни, по случаю визита президента Кореи Юн Сок Ель во Вьетнам был подписан ряд меморандумов о..
                    </p>
                    <div class="py-8">
                      <button type="button" class="bg-transparent px-8 text-white border rounded-lg font-bold text-lg px-5 py-2.5 mr-2 mb-2">
                        Подробнее
                      </button>
                    </div>
                  </div>
                  <div class="slide">
                    <p class="text-3xl md:text-4xl text-white font-bold">
                      Новости
                    </p>
                    <span class="mt-2 mb-4 w-[10%] h-[8px] bg-[#01bcfb] inline-block"></span>
                    <p class="text-2xl md:text-3xl text-white font-bold">
                      Зависящая от импорта электричества Литва рассчитывает на солидарность соседей
                    </p>
                    <p class="text-md md:text-lg my-5 text-white">
                      Несмотря на тенденцию к замедлению, корейские инвестиции во Вьетнам в ближайшее время увеличатся, включая многие крупномасштабные проекты, до миллиардов долларов США.Проект на миллиард долларов ждетВ рамках Вьетнамско-корейского бизнес-форума, состоявшегося в выходные дни, по случаю визита президента Кореи Юн Сок Ель во Вьетнам был подписан ряд меморандумов о..
                    </p>
                    <div class="py-8">
                      <button type="button" class="bg-transparent px-8 text-white border rounded-lg font-bold text-lg px-5 py-2.5 mr-2 mb-2">
                        Подробнее
                      </button>
                    </div>
                  </div>
                </ssr-carousel>
              </div>
              <div class="col-span-12 md:col-span-6 flex items-center md:items-end">
                <div>
                  <div class="card my-2 w-full md:w-3/4 md:ml-auto">
                    <div
                      class="flex flex-col rounded-bl rounded-tl bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700 md:max-w-xl md:flex-row">
                      <div class="w-full h-auto bg-no-repeat bg-center bg-cover bg-[url('~/assets/images/card_1.png')]">
                      </div>
                      <div class="flex flex-col justify-start p-6">
                        <h5
                          class="mb-2 text-xl font-medium text-neutral-800 dark:text-neutral-50">
                          От нефти к «зеленой» энергии. Роль Баку в глобальном энергопереходе
                        </h5>
                        <a class="mb-4 text-base text-neutral-600 dark:text-neutral-200">
                          Подробнее >
                        </a>
                      </div>
                    </div>
                  </div>
                  <div class="card my-2 w-full md:w-3/4 md:ml-auto">
                    <div
                      class="flex flex-col rounded-lg bg-white shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)] dark:bg-neutral-700 md:max-w-xl md:flex-row">
                      <div class="w-full rounded-bl rounded-tl object-cover h-auto bg-no-repeat bg-center bg-cover bg-[url('~/assets/images/card_1.png')]">
                      </div>
                      <div class="flex flex-col justify-start p-6">
                        <h5
                          class="mb-2 text-xl font-medium text-neutral-800 dark:text-neutral-50">
                          От нефти к «зеленой» энергии. Роль Баку в глобальном энергопереходе
                        </h5>
                        <a class="mb-4 text-base text-neutral-600 dark:text-neutral-200">
                          Подробнее >
                        </a>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>


      </div>
    </section>
    <!-- Fourth Bloc-->

    <!-- Fifth Bloc    -->
    <section>
    <div class="container mx-auto bg-[#0C3759] my-[50px] py-[50px] rounded-2xl">
      <div class="grid grid-cols-12 gap-4 md:px-[100px]">
        <div class="col-span-12 px-4 md:col-span-6 text-center md:text-left">
          <p class="text-3xl md:text-4xl text-white font-bold">
            Ключевые Цифры
          </p>
          <span class="mt-2 mb-4 w-[10%] h-[8px] bg-[#01bcfb] inline-block"></span>
          <p class="text-md md:text-lg text-white my-5">
            Мы будем укреплять наши ценности трудолюбия и ответственности, уважения к Человеку Труда, создавая условия для реализации созидательного потенциала каждого гражданина страны.
          </p>
        </div>
        <div class="col-span-12 px-4 md:col-span-6 text-center md:text-left">
          <div class="flex justify-center my-4">
            <div class="w-1/2 text-center">
              <p class="text-4xl font-bold text-[#01bcfb]">
                +100
              </p>
              <p class="text-xl text-white">
                Разработанных<br>
                проектов
              </p>
            </div>
            <div class="w-1/2 text-center">
              <p class="text-4xl font-bold text-[#01bcfb]">
                #1
              </p>
              <p class="text-xl text-white">
                В Центральной<br>
                Азии
              </p>
            </div>
          </div>
          <div class="flex justify-center my-4">
            <div class="w-1/2 text-center">
              <p class="text-4xl font-bold text-[#01bcfb]">
                9
              </p>
              <p class="text-xl text-white">
                Лет<br>
                Опыта работы
              </p>
            </div>
            <div class="w-1/2 text-center">
              <p class="text-4xl font-bold text-[#01bcfb]">
                +50
              </p>
              <p class="text-xl text-white">
                Сотрудников<br>
                в штате
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    </section>
    <!-- Fifth Bloc    -->
    <section>
      <div class="container mx-auto my-[50px] py-[50px] rounded-2xl">
        <div class="grid grid-cols-12 gap-4">
          <div class="col-span-12 px-4 md:col-span-12 text-center md:text-left">
          <ssr-carousel :slides-per-page='1' show-dots loop show-arrows>
              <div class="slide">
                <div class="flex justify-center">
                <div class="py-5 blue-gradient-button min-h-[250px] w-full md:w-6/12 rounded-2xl flex justify-center items-center px-3">
                    <div class="w-1/3 text-center">
                      <div class="mx-auto rounded-full w-[100px] h-[100px] bg-no-repeat bg-center bg-cover bg-[url('~/assets/images/card_1.png')]"></div>
                      <p class=" text-white text-md text-center font-bold my-2">
                        Жанар Айманова
                      </p>
                      <p class=" text-white text-md text-xs text-center">
                        Директор
                      </p>
                    </div>
                    <div class="w-2/3 text-white items-center flex items-center">
                      <div>
                        <p class="text-2xl mb-0">"</p>
                        <p class="text-md text-white">
                          Все достижения и успехи
                          страны – результат каждодневного, кропотливого труда всех казахстанцев.
                          Мы будем укреплять наши ценности трудолюбия и ответственности
                        </p>
                        <p class="text-2xl text-center">"</p><br>
                      </div>


                    </div>

                </div>
              </div>
              </div>
              <div class="slide">
                <div class="flex justify-center">
                <div class="py-5 blue-gradient-button min-h-[250px] w-full md:w-6/12 rounded-2xl flex justify-center items-center px-3">
                    <div class="w-1/3 text-center">
                      <div class="mx-auto rounded-full w-[100px] h-[100px] bg-no-repeat bg-center bg-cover bg-[url('~/assets/images/card_1.png')]"></div>
                      <p class=" text-white text-md text-center font-bold my-2">
                        Жанар Айманова
                      </p>
                      <p class=" text-white text-md text-xs text-center">
                        Директор
                      </p>
                    </div>
                    <div class="w-2/3 text-white items-center flex items-center">
                      <div>
                        <p class="text-2xl mb-0">"</p>
                        <p class="text-md text-white">
                          Все достижения и успехи
                          страны – результат каждодневного, кропотливого труда всех казахстанцев.
                          Мы будем укреплять наши ценности трудолюбия и ответственности
                        </p>
                        <p class="text-2xl text-center">"</p><br>
                      </div>


                    </div>

                </div>
              </div>
              </div>
          </ssr-carousel>
          </div>
        </div>
      </div>
    </section>
  </section>
</template>

<script lang="ts">
export default {
  data: () => ({
    textAssociation: [
      "Казахстанская Ассоциация Цифровой Энергетики является объединением юридических лиц и некоммерческой организацией, созданной с целью достижения целей технологического развития в сфере Internet of Energy и Industry 4.0, путем цифровой трансформации энергетической отрасли Республики Казахстан.",
      "Мы ожидаем в своих рядах и других игроков сектора, и мы открыты к профессиональной дискуссии. Мы готовы выступить со своими идеями и разработками на разных площадках, готовы обсудить перспективные направления с отраслевыми ассоциациями.",
      "Мы готовы работать по темам импортозамещения, кибер- и промышленной безопасности, кадрового обеспечения отрасли, развития цифровых компетенций и др.",
      "Мы открыто обсуждаем эти проблемы не только внутри сообщества, но и на уровне Правительства РК, на площадках комитетов Парламента РК, приглашая ведущих экспертов, представителей бизнес-, межотраслевых, научных сообществ для публичных дискуссий."
    ],
    slider_card_option:[
      {
        minWidth: 768,
        slidesPerPage: 1,
      },
      {
        minWidth: 1024,
        slidesPerPage: 1,
      }
    ],
  }),


}


</script>
<style>
[aria-disabled] > .ssr-carousel-dot-icon {
  opacity: 1;
  background: #01bcfb!important;
  cursor: default;
}
</style>
