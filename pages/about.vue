<template>
  <v-row>
    <v-card
      class="mx-2"
      color="primary"
      dark
    >
      <v-card-title>
        <v-icon
          large
          left
        >
          mdi-account
        </v-icon>
        <span class="title font-weight-light">Quem sou eu ?</span>
      </v-card-title>

      <v-card-text class="headline font-weight-bold white--text">
        {{ aboutMe }}
      </v-card-text>

      <v-card-actions>
        <v-list-item class="grow">
          <v-list-item-avatar color="white">
            <v-img
              class="elevation-6"
              alt=""
              src="https://avataaars.io/?accessoriesType=Prescription02&avatarStyle=Transparent&clotheType=BlazerSweater&eyeType=Happy&eyebrowType=Default&facialHairColor=Black&facialHairType=BeardLight&hairColor=Black&topType=ShortHairShortCurly"
            />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>Daniel Silva</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-card-actions>
    </v-card>
    <v-card
      style="width: 100%"
      outlined
      class="mt-2 mx-2"
    >
      <v-card-text>
        <div class="font-weight-bold ml-8 mb-2 title text-center">
          Experiências
        </div>
        <v-timeline>
          <v-timeline-item
            v-for="(item, i) in experienceItems"
            :key="i"
            :color="item.color"
            :icon="item.icon"
            fill-dot
          >
            <template #opposite>
              <span
                :class="`headline font-weight-bold blue--text`"
                v-text="item.year"
              />
            </template>
            <v-card
              :color="item.color"
              dark
            >
              <v-card-title class="title">
                {{ item.title }}
              </v-card-title>
              <v-card-text v-if="item.description" class="pt-2">
                <p
                  v-for="(line,j) in item.description"
                  :key="j"
                  class="body-1 white--text"
                >
                  {{ line }}
                </p>
              </v-card-text>
            </v-card>
          </v-timeline-item>
        </v-timeline>
        <div class="font-weight-bold ml-8 mb-2 title text-center">
          Educação
        </div>
        <v-timeline>
          <v-timeline-item
            v-for="(item, index) in educationItems"
            :key="index"
            :color="item.color"
            :icon="item.icon"
            fill-dot
          >
            <template #opposite>
              <span
                :class="`headline font-weight-bold blue--text`"
                v-text="item.year"
              />
            </template>
            <v-card
              :color="item.color"
              dark
            >
              <v-card-title class="title">
                {{ item.title }}
              </v-card-title>
              <v-card-text v-if="item.description" class="pt-2">
                <p
                  v-for="(line,j) in item.description"
                  :key="j"
                  class="body-1 white--text"
                >
                  {{ line }}
                </p>
              </v-card-text>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-card>
  </v-row>
</template>
<style scoped>

</style>
<script>
export default {
  name: 'About',
  data () {
    return {
      aboutMe: '" Desenvolvedor Fullstack Sênior que adora inovar, discutir e desenvolver ideias e projetos novos. ' +
        'Devido a experiência como Analista de Negócios, tenho um olhar bem afiado para identificar a raíz do problema ' +
        'ou encontrar quem saiba, fazer a ponte entre as diversas partes envolvidas e então elaborar e desenvolver a melhor solução. ' +
        'Atualmente, meus pontos mais fortes estão em .Net com C# e Vue.Js. "',
      experienceItems: [
        {
          title: 'Desenvolvedor .NET Sênior - Amcor',
          icon: 'mdi-star',
          year: '2020 - Presente',
          color: 'primary',
          description: [
            '- Acompanhamento da mudança de escopo para que o time atue e desenvolva soluções globalmente',
            '- Estudo e implementação de Azure Devops como padrão para a companhia e para os times de desenvolvimento',
            '- Elaboração de guidelines e boas práticas para serem seguidas pelos desenvolvedores do time',
            '- Desenvolvimento, manutenção e integração em C# e Vb.net para sistemas de Chão de Fábrica.',
            '- Participação de projetos e desenvolvimento que impactam Europa, América do Norte e Brasil',
            '- Refatoração de sistemas legados, trazendo-os para o ambiente .NET Core e utilizando conceitos modernos ' +
            'como arquitetura de micro serviços, mensageria, testes automatizados e deploys automatizados com Azure Devops',
            '- Densevolvimento de Sistemas usando Vue.Js no Frontend integrando com .Net Core'
          ]
        },
        {
          title: 'Desenvolvedor Pleno - Amcor',
          icon: 'mdi-account',
          year: '2018 - 2020',
          color: 'indigo',
          description: [
            '- Mudança para atuar com o time de desenvolvimento nos Estados Unidos dentro da Amcor',
            '- Densevolvimento de relatórios e Integrações na ferramenta Workday',
            '- Desenvolvimento, manutenção e integração em C# e Vb.net para sistemas de Chão de Fábrica',
            '- Desenvolvimento e manutenção de integração entre ERP\'s e SAP usando XMII'
          ]
        },
        {
          title: 'Founder/Developer - Tamarindo Soluções',
          year: '2016 - 2019',
          icon: 'mdi-rocket',
          color: 'orange',
          description: [
            '- Projeto de Startup que ocorreu em paralelo ao meu trabalho na Amcor',
            '- Planejamento e Desenvolvimento da Plataforma Tamarindo (descontinuada) com Laravel e Vue.Js'
          ]
        },
        {
          title: 'Analista de Negócios - Bemis/Amcor',
          year: '2016 - 2018',
          icon: 'mdi-account',
          color: 'indigo',
          description: [
            '- Propor padrões, procedimentos e fornecer suporte técnico na identificação das alternativas e oportunidades de aplicações de Tecnologias de Informação para as áreas de RH.',
            '- Avaliação das evoluções de versões dos sistemas de RH identificando os impactos no modelo já implantado e o custo benefício dessas atualizações.',
            '- Participar das elaborações de "Business Case" de Projetos relacionados aos processos, gerando subsídios para decisões relativas à implementação.',
            '- Avaliar continuamente os Projetos relacionados à área de RH, aferindo os benefícios esperados e calculando os referidos retornos do capital empregado (ROI).',
            '- Participar de reuniões com fornecedores de soluções e áreas administrativas da empresa para prestar suporte e esclarecer o atendimento aos requerimentos definidos e o completo entendimento das necessidades de TI e negócio.',
            '- Promover o relacionamento externo com fornecedores para o perfeito atendimento das necessidade e estratégias da companhia.',
            '- Desenvolvimento de Correções e Melhorias para o Fatorhweb',
            '- Desenvolvimento de Relatórios Customizados com IReports e manutenção em código legado de código intra-company',
            '- Manutenção e desenvolvimento de Procedures e Views no MSSQL'
          ]
        },
        {
          title: 'Estagiário Analista de Negócios - Bemis',
          year: '2014 - 2016',
          icon: 'mdi-account',
          color: 'indigo'
        }
      ],
      educationItems: [
        {
          title: 'USP/ESALQ - MBA - Gestão de Negócios',
          icon: 'mdi-briefcase',
          year: '2019 - 2021',
          color: 'primary'
        },
        {
          title: 'Certicação C# - Exam 483 - Programming in C#',
          icon: 'mdi-language-csharp',
          year: '2019',
          color: 'purple'
        },
        {
          title: 'Capacitação em Green Belt Lean Seis Sigma - Fundação Vanzolini - 72 Horas (sem certificação)',
          icon: 'mdi-google-analytics',
          year: '2017',
          color: 'green darken-4'
        },
        {
          title: 'IFSP - Análise e Desenvolvimento de Sistemas',
          year: '2013 - 2016',
          icon: 'mdi-glasses',
          color: 'green',
          description: [
            '- Projeto Final: Um sistema web em C# que a partir de HTML estático, gerava temas funcionais para ' +
            'as plataformas Wordpress e Drupal'
          ]
        },
        {
          title: 'SENAI - Técnico em eletrônica',
          year: '2011 - 2012',
          icon: 'mdi-memory',
          color: 'red',
          description: [
            '- Ênfase em automação',
            '- Projeto final foi um mini sistema em c++ que controlava o movimento de um robô em uma plano 2D ' +
            'usando processamento de imagem de uma câmera externa',
            '- Robô utilizava um micro-controlador PIC'
          ]
        }
      ]
    }
  }
}
</script>
