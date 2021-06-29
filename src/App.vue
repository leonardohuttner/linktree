<template>
  <div class="base q-gutter-md q-ma-md justify-center">
      <div class="perfil">
        <img src="territorio-logo.jpg" class="imagem">
        <h4>{{empresa.nome}}</h4>
        <p>{{empresa.slogan}}</p>
      </div>
    <q-card
      class="card"
      clickable
      v-for="dado in dados"
      :key="dado.nome"
      @click="abrirLink(dado.link)"
    >
    <q-list>
      <q-item>
        <q-item-section avatar>
          <q-avatar class="q-ma-sm" size="sm">
            <img :src="dado.icon" :alt="dado.nome">
          </q-avatar>
        </q-item-section>
        <q-item-section>
          <q-item-label header class="q-pa-xs">
            <h6>{{dado.nome}}</h6>
          </q-item-label>
          <q-item-label caption line=1>
            {{dado.descricao}}
          </q-item-label>
        </q-item-section>
      </q-item>
    </q-list>
    </q-card>
    <q-card class="card q-mb-md">
      <fotos/>
    </q-card>
<section class="desenvolvido">
  Desenvolvido por Leonardo Huttner
</section>
  </div>
</template>

<script>
import fotos from './views/fotos.vue'
export default {
components:{ fotos },
  data(){
   return {
     color_amarelo:'#fcbd18',
     color_verde:'#00a85a',
     empresa:{
      nome:'Territorio do Calçado',
      slogan:'Somos uma loja virtual que traz praticidade e leva conforto até você.'
     },
     dados:[
       {
         nome:'WhatsApp',
         descricao:'Entre em contato conosco com link direto',
         icon: '/whatsapp.png',
         link: 'https://wa.me/message/6Z5UKTEG34ROI1'
       },
       {
        nome:'Catalogo',
        descricao:'Clique e confira nosso catalogo e compre direto pelo WhatsApp',
        icon:'/whatsapp.png',
        link:'https://wa.me/c/555185261791'
       },
       {
         nome:'Shopee',
         icon:'/shopee.png',
         descricao:'Encontre-nos pela nossa loja na shopee e aproveite preços baixos e cupons!',
         link:'https://shopee.com.br/shop/397063255/search'
       },
       {
         nome:'Email',
         icon:'mail.png',
         descricao:'Procurando por produtos no atacado? Faça uma cotação por email',
         link:'mailto:territoriodocalcado.camaqua@gmail.com?subject=Produtos%20por%20atacado&body=Tenho%20interesse%20em%20comprar%20por%20atacado.'
       },
       {
         nome:'Instagram',
         icon:'/instagram.png',
         descricao:'Nos siga para acompanhar as ultimas novidades',
         link:'https://www.instagram.com/territoriodocalc/'
       }
     ]
   }
 },
 methods:{
   abrirLink(link){
     window.open(link,'_blank')
   }
 }
}
</script>

<style>

body{
  margin: 0;
  width: 100vw;
  height: 100vh;
}
p,h4,h6{
  margin: 0px;
}
.base{
  /* background-color: #00a85abb; */
  background-repeat: no-repeat;
  background-size: cover;
}
.card{
  width: 90%;
  height: auto;
  margin-left: auto;
  cursor: pointer;
}
.card{
  width: 90%;
  height: auto;
  margin-left: auto;
  cursor: pointer;
}
.perfil{
  margin-top: 5px;
  text-align: center;
}

.imagem{
  width: 8rem;
  height: 8rem;
  border-radius: 50%;
}
.desenvolvido{
  text-align: center;
}
</style>
