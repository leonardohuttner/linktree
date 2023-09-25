<template>
  <div class="base q-gutter-y-md">
    <div class="perfil q-pt-md">
      <img src="territorio-logo.png" class="imagem shadow-4"/>
      <h4>{{ empresa.nome ? empresa.nome : '' }}</h4>
      <p>{{ empresa.slogan }}</p>
    </div>
    <div class="q-gutter-y-md q-ma-md container">
      <q-card
        class="card"
        clickable
        v-for="dado in dados"
        :key="dado.nome"
        @click="abrirLink(dado.link)"
      >
        <q-list>
          <q-item>
            <q-item class="icone no-padding q-ma-xs">
                <img :src="dado.icon" :alt="dado.nome" class="avatar q-pr-sm" :style="dado.style ? dado.style : ''" />
            </q-item>
            <q-item-section>
              <q-item-label header class="no-padding no-margin">
                <p class="title">{{ dado.nome }}</p>
              </q-item-label>
              <q-item-label caption line="1" class="no-margin">
                {{ dado.descricao }}
              </q-item-label>
            </q-item-section>
          </q-item>
        </q-list>
      </q-card>
      <q-card class="card">
          <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3425.2987427273006!2d-51.81483372525907!3d-30.85030996911322!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x951a77492d48ab1f%3A0x3e67687a3167b41f!2zVGVycml0w7NyaW8gQ2FtYXF1w6M!5e0!3m2!1spt-BR!2sbr!4v1695611138117!5m2!1spt-BR!2sbr" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </q-card>
      <!-- <q-card class="card q-mb-md">
        <fotos />
      </q-card> -->
    </div>

    <section class="desenvolvido">
      Desenvolvido por
      <a href="https://br.linkedin.com/in/leonardo-huttner">Leonardo Huttner</a>
    </section>
  </div>
</template>

<script>
// import fotos from "./views/fotos.vue";
export default {
  // components: { fotos },
  data() {
    return {
      color_amarelo: "#fcbd18",
      color_verde: "#00a85a",
      empresa: {
        slogan:
          "Praticidade e conforto até você.",
      },
      dados: [
        {
          nome:"Site",
          descricao:"Compre através do nosso site, e garanta as melhores ofertas.",
          icon: "/territorio-logo-bg.png",
          link:"https://loja.territoriocamaqua.com.br"
        },
        {
          nome: "WhatsApp",
          descricao: "Entre em contato conosco com link direto com um de nossos atendentes",
          icon: "/whatsapp.png",
          link: "https://wa.me/message/6Z5UKTEG34ROI1",
          style: "width: 2rem;"
        },
        {
          nome: "Instagram",
          icon: "/instagram.png",
          descricao: "Nos siga para acompanhar as ultimas novidades",
          link: "https://www.instagram.com/aterritorio.store/",
          style: "width: 2rem;"
        },
        {
          nome: "Shopee",
          icon: "/shopee.png",
          descricao:
            "Encontre-nos pela nossa loja na shopee e aproveite preços baixos e cupons!",
          link: "https://shopee.com.br/shop/397063255/search",
          style: "width: 2rem;"
        },
        {
          nome: "Mercado Livre",
          icon: "ml.svg",
          descricao:
          "Compre também através do Mercado Livre",
          link: "https://www.mercadolivre.com.br/perfil/TERRITORIODOCALCADO",
          style: "width: 2rem;"
        },
        {
          nome: "Mercado Shops - Atacado",
          icon: "ml.svg",
          descricao:
          "Compre também através do Mercado Livre",
          link: "https://territoriodocalcado.mercadoshops.com.br/",
          style: "width: 2rem;"
        },
        {
          nome: "Email",
          icon: "mail.png",
          descricao:
            "Não encontrou o que procurava? Entre em contato por email",
          link: "mailto:territoriodocalcado.camaqua@gmail.com?subject=Duvidas%20Contato&body=Olá%20estou%20com%20duvidas%20e%20gostaria%20de%20atendimento.",
          style: "width: 2rem;"
        },
      ],
    };
  },
  methods: {
    abrirLink(link) {
      window.open(link, "_blank");
    },
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400&display=swap');
body {
  margin: 0;
  width: 100vw;
  height: 100vh;
}
p,
h4,
h6 {
  font-family: 'Roboto', sans-serif;
  font-size: 1rem;
  margin: 0px;
}
.base {
  /* background-color: #00a85abb; */
  margin: 0;
  background: rgb(252,189,24);
  background: linear-gradient(0deg, #EFDDDD 0%, rgba(255,255,255,1) 100%);
  background-repeat: no-repeat;
  background-size: cover;
}
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.card {
  width: 100%;
  max-width: 500px;
  border-radius: 20px;
  cursor: pointer;
}
.perfil {
  margin-top: 5px;
  text-align: center;
}

.imagem {
  width: 12rem;
  height: 12rem;
  border-radius: 50%;
}
.desenvolvido {
  text-align: center;
}

.avatar {
  max-height: 10rem;
  margin: 0;
}
a{
  text-decoration: none;
  color: black;
}
.icone {
  display: flex;
  align-items: center;
  justify-content: center;
}

.title {
  font-size: 1.2rem;
  font-weight: bold;
  margin: 0;
}
</style>
