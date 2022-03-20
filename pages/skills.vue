<template>
  <v-card outlined>
    <v-card-title> Quadro de Habilidades</v-card-title>
    <v-row class="mx-1 align-start py-3">
      <v-col
        v-for="(system, index) in systems"
        :key="index"
        cols="12"
        sm="4"
        md="3"
      >
        <SystemKnowledge
          :title="system.title"
          :level="system.level"
          :bar-value="system.bar"
          :progress-bar-color="system.barColor"
          :description="system.description"
          :avatar-letter="system.avatarLetter"
          :avatar-color="system.avatarColor"
          :card-color="system.cardColor"
          :text-color="system.textColor"
          :description-title-color="system.descriptionTitleColor"
        />
      </v-col>
    </v-row>
  </v-card>
</template>
<style scoped>

</style>
<script>
export default {
  name: 'Skills',
  data () {
    return {
      systems: [
        {
          title: 'C#',
          level: 'Diário',
          avatarColor: 'purple darken-1',
          cardColor: 'purple darken-3',
          bar: 100,
          avatarLetter: 'C#',
          description: 'Winforms e APIS, certificação 70-483'
        },
        {
          title: 'VueJs',
          level: 'Diario',
          cardColor: 'teal lighten-1',
          avatarColor: 'teal darken-4',
          barColor: 'white',
          bar: 100,
          description: 'Desenvolvimento Frontend com Vuetify e NUXTJS'
        },
        {
          title: 'MS SQL',
          level: 'Diario',
          cardColor: 'red lighten-2',
          avatarColor: 'teal darken-4',
          barColor: 'white',
          bar: 100,
          description: 'Desenvolvimento de tabelas e procedures'
        },
        {
          title: 'Laravel',
          avatarColor: 'red darken-2',
          cardColor: 'grey lighten-5',
          textColor: 'red',
          level: 'Estudo',
          bar: 30,
          description: 'APIS e Pacotes Composer'
        },
        {
          title: 'Flutter',
          level: 'Estudo',
          cardColor: 'blue lighten-2',
          avatarColor: 'blue darken-4',
          bar: 10,
          description: 'Em Fase aprendizado'
        },
        {
          title: 'Workday',
          level: 'Raro',
          cardColor: 'blue darken-3',
          avatarColor: 'orange darken-1',
          bar: 10,
          description: 'Desenvolvimento de Relatórios, Integrações e BIRT Reports'
        },
        {
          title: 'Fatorhweb',
          level: 'Raro',
          cardColor: 'blue darken-4',
          avatarColor: 'lime darken-4',
          bar: 10,
          description: 'Desenvolvimento de Relatórios, Integrações via SQL, ' +
            'Desenvolvimento de Melhorias e customizações em Java, Suporte e Criação de Rúbricas/Eventos e Acordos Coletivos'
        },
        {
          title: 'xMII - SAP',
          level: 'Frequente',
          cardColor: 'blue darken-4',
          avatarColor: 'black',
          bar: 70,
          description: 'Desenvolvimento e manutenção de Integrações entre SAP e Sistemas de Chão de Fábrica'
        }
      ]
    }
  }
}
</script>
