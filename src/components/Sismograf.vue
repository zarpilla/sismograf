/* eslint-disable */
<template>
  <div>
<full-page :options="options">
      <div class="section">
        <button @click="$refs.fullpage.api.moveSectionDown()">
            Next
        </button>
        Section 1
      </div>
      <div class="section">
        <button @click="$refs.fullpage.api.moveSectionUp()">
            Prev
        </button>
        Section 2
      </div>
    </full-page>
<!-- <ul id="menu">
        <li data-menuanchor="page1" class="active"><a href="#page1">Section 1</a></li>
        <li data-menuanchor="page2"><a href="#page2">Section 2</a></li>
        <li data-menuanchor="page3"><a href="#page3">Section 3</a></li>
    </ul>
    <full-page ref="fullpage" :options="options" id="fullpage">
    <div class="section">
      First section ...
    </div>
    <div class="section">
      Second section ...
    </div>
  </full-page> -->
<!-- 
    <div id="example-1">
      <div v-for="(ambit, i) in ambits" v-bind:key="i + ambit.nom">
        <div class="ambit">
          {{ ambit.nom }}
        </div>
        <div v-for="(sector, i) in ambit.sectors" v-bind:key="i + sector.nom">
          <div class="sector">
          {{ sector.nom }}
          </div>          
          <ul v-for="(item, i) in sector.items" v-bind:key="i + item.nom">
            <li class="item" style="float:left" v-on:click="punctuation(ambit, sector, item)">
            {{ item.nom }}
            </li>          
          </ul>
          <br>
          <br>
        </div>
        <br>
        <br>
      </div>
    </div> -->

  </div>
</template>

<script>

export default {
  name: 'Sismograf',
  
  props: {
    msg: String
  },
  methods: {
    punctuation: function (ambit, sector, item) {
      // `this` inside methods points to the Vue instance
      // alert('Hello ' + ambit.nom + '!')
      // alert('Hello ' + sector.nom + '!')
      // alert('Hello ' + item.nom + '!')
      console.log(ambit.nom);
      console.log(sector.nom);
      console.log(item.nom);
      //console.log(this);
      // `event` is the native DOM event
      // if (event) {
      //   alert(event.target.tagName)
      // }
    }
  },
  data () {  
    return {
      options: {        
        menu: '#menu',
        anchors: ['page1', 'page2', 'page3'],
        sectionsColor: ['#41b883', '#ff5f45', '#0798ec']
      },
      ambits: [
          {
              nom: "ÀMBIT PERSONAL", sectors: [
                  { nom: "Desenvolupament personal", coopsula: "Coòpsula Desenvolupament Personal i Rols i Lideratges", items: [{ nom: "Explotació", valor: 1 }, { nom: "Objectivització del treball laboral", valor: 2 }, { nom: "Conductisme productiu", valor: 3 }, { nom: "Desenvolupament personal extern i forçat", valor: 4 }, { nom: "Activisme – autoexplotació", valor: 5 }, { nom: "Consiliació social", valor: 6 }, { nom: "Proactivitat", valor: 7 }, { nom: "TREBALL*", valor: 8 },] },
                  { nom: "Treball reproductiu", coopsula: "-", items: [{ nom: "Patriarcal", valor: 1 }, { nom: "Productivisme", valor: 2 }, { nom: "Síntoma Tatcher", valor: 3 }, { nom: "Paritat", valor: 4 }, { nom: "Feminisme revindicatiu", valor: 5 }, { nom: "Posar les cures al centre", valor: 6 }, { nom: "Cures estructurals", valor: 7 }, { nom: "Equitat comunitàri del treball reproductiu", valor: 8 },] },
                  { nom: "Arrelament i identitat", coopsula: "Còpsula Identitat i Propòsit", items: [{ nom: "Treball per sobre el propòsit", valor: 1 }, { nom: "Innovació utilitària", valor: 2 }, { nom: "Venda per sobre el valor", valor: 3 }, { nom: "RSE", valor: 4 }, { nom: "Propòsit per sobre el treball", valor: 5 }, { nom: "Sentiment de pertinença", valor: 6 }, { nom: "Iniciativa arrelada", valor: 7 }, { nom: "Propòsit i treball en equilibri", valor: 8 },] },
              ]
          },
          {
              nom: "ÀMBIT ESTRUCTURAL", sectors: [
                  { nom: "Organització interna", coopsula: "Coòpsula Organització interna, Rols i lideratges i Models de Gobernança i Participació", items: [{ nom: "Autoritorisme", valor: 1 }, { nom: "Demagogia", valor: 2 }, { nom: "Votació com a única eina", valor: 3 }, { nom: "Delegatiu", valor: 4 }, { nom: "Consens", valor: 5 }, { nom: "Rols col·legiats", valor: 6 }, { nom: "Consentiment", valor: 7 }, { nom: "Co-creació autogestionària (ontonomia)", valor: 8 },] },
                  { nom: "Economia", coopsula: "Coòpsula Sostenibilitat Econòmica", items: [{ nom: "Deuta", valor: 1 }, { nom: "Precarietat", valor: 2 }, { nom: "Subsistència", valor: 3 }, { nom: "Capacitat d’inversió", valor: 4 }, { nom: "Sostenibilitat econòmica", valor: 5 }, { nom: "Finances co-gestionades", valor: 6 }, { nom: "Economia cooperativa", valor: 7 }, { nom: "Mutualisme comunitàri", valor: 8 },] },
                  { nom: "Jurídic i legal", coopsula: "Assessories", items: [{ nom: "Deixadesa", valor: 1 }, { nom: "Gestió de mínims", valor: 2 }, { nom: "Externalització de responsabilitats", valor: 3 }, { nom: "Control de la gestió", valor: 4 }, { nom: "Internalització", valor: 5 }, { nom: "Externalització de tasques", valor: 6 }, { nom: "Co-gestió amb responsabilitats", valor: 7 }, { nom: "Auto-gestió comunitària", valor: 8 },] },
              ]
          },
          {
              nom: "ÀMBIT D’INFLUÈNCIA", sectors: [
                  { nom: "Avaluació i estratègia ", coopsula: "Coòpsula Avaluació i Planificació estratègica", items: [{ nom: "Invasora", valor: 1 }, { nom: "Mercantilista", valor: 2 }, { nom: "Oportunista", valor: 3 }, { nom: "Parisitària avengelitzadora", valor: 4 }, { nom: "Confrontativa", valor: 5 }, { nom: "Responsiva", valor: 6 }, { nom: "Reconsiliadora", valor: 7 }, { nom: "Sistèmica", valor: 8 },] },
                  { nom: "Comunicació externa", coopsula: "Coòpsula Comunicació externa", items: [{ nom: "Comunicació de la por i l’engany", valor: 1 }, { nom: "Creació de necessitats externes", valor: 2 }, { nom: "Màrqueting condecendent", valor: 3 }, { nom: "Màrqueting de valors", valor: 4 }, { nom: "Revindicativa", valor: 5 }, { nom: "Comunicació per a la transformació", valor: 6 }, { nom: "Propositiva", valor: 7 }, { nom: "Diàleg dialògic", valor: 8 },] },
                  { nom: "Intercooperació", coopsula: "Festival ESS i Jornades d’intercooperació", items: [{ nom: "Monopoli", valor: 1 }, { nom: "Oligopoli", valor: 2 }, { nom: "Competència", valor: 3 }, { nom: "Oligopoli cooperatiu", valor: 4 }, { nom: "Autonomisme", valor: 5 }, { nom: "Interdependència", valor: 6 }, { nom: "Interindependència", valor: 7 }, { nom: "Ecosistema cooperatiu", valor: 8 },] },
              ]
          },
          {
              nom: "ÀMBIT COMUNITÀRI", sectors: [
                  { nom: "Impacte econòmic", coopsula: "Coòpsula Ecosistemes ESS i Desenvolupament local", items: [{ nom: "Degradació", valor: 1 }, { nom: "Deslocalització", valor: 2 }, { nom: "Centralisme", valor: 3 }, { nom: "Pesebrisme", valor: 4 }, { nom: "Decreixement", valor: 5 }, { nom: "Restauratiu", valor: 6 }, { nom: "Reconsiliadora", valor: 7 }, { nom: "Regeneratiu", valor: 8 },] },
                  { nom: "Impacte social", coopsula: "Coòpsula Ecosistemes ESS i Desenvolupament local", items: [{ nom: "Esclavitud", valor: 1 }, { nom: "Utilitari", valor: 2 }, { nom: "Paternalisme", valor: 3 }, { nom: "Assistencialisme", valor: 4 }, { nom: "Justícia Social", valor: 5 }, { nom: "Restauratiu", valor: 6 }, { nom: "Reconsiliadora", valor: 7 }, { nom: "Regeneratiu", valor: 8 },] },
                  { nom: "Impacte ecològic", coopsula: "Coòpsula Ecosistemes ESS i Desenvolupament local", items: [{ nom: "Expoliació", valor: 1 }, { nom: "Extracció", valor: 2 }, { nom: "Green washing", valor: 3 }, { nom: "Proteccionisme", valor: 4 }, { nom: "Ecologisme", valor: 5 }, { nom: "Restauratiu", valor: 6 }, { nom: "Reconsiliadora", valor: 7 }, { nom: "Regeneratiu", valor: 8 },] }
              ]
          }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
