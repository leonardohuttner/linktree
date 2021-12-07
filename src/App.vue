<template>
  <div class="base q-gutter-y-md">
    <div class="perfil q-pt-md">
      <img src="territorio-logo.jpg" class="imagem shadow-9"/>
      <h4>{{ empresa.nome }}</h4>
      <p>{{ empresa.slogan }}</p>
    </div>
    <div class="q-gutter-y-md q-ma-md">
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
              <img :src="dado.icon" :alt="dado.nome" class="avatar" />
            </q-item>
            <q-item-section>
              <q-item-label header class="no-padding no-margin">
                {{ dado.nome }}
              </q-item-label>
              <q-item-label caption line="1" class="no-margin">
                {{ dado.descricao }}
              </q-item-label>
            </q-item-section>
          </q-item>
        </q-list>
      </q-card>
      <q-card class="card q-mb-md">
        <fotos />
      </q-card>
    </div>

    <section class="desenvolvido">
      Desenvolvido por
      <a href="https://br.linkedin.com/in/leonardo-huttner">Leonardo Huttner</a>
    </section>
  </div>
</template>

<script>
import fotos from "./views/fotos.vue";
export default {
  components: { fotos },
  data() {
    return {
      color_amarelo: "#fcbd18",
      color_verde: "#00a85a",
      empresa: {
        nome: "Territorio do Calçado",
        slogan:
          "Somos uma loja virtual que traz praticidade e leva conforto até você.",
      },
      dados: [
        {
          nome:"Site",
          descricao:"Compre sem sair de casa através do nosso site próprio",
          icon: "/site.png",
          link:"https://lojaterritoriodocalcado.com.br"
        },
        {
          nome: "WhatsApp",
          descricao: "Entre em contato conosco com link direto com um de nossos atendentes",
          icon: "/whatsapp.png",
          link: "https://wa.me/message/6Z5UKTEG34ROI1",
        },
        {
          nome: "Catalogo",
          descricao:
            "Clique e confira nosso catalogo e compre direto pelo WhatsApp",
          icon: "/whatsapp.png",
          link: "https://wa.me/c/555185261791",
        },
        {
          nome: "Shopee",
          icon: "/shopee.png",
          descricao:
            "Encontre-nos pela nossa loja na shopee e aproveite preços baixos e cupons!",
          link: "https://shopee.com.br/shop/397063255/search",
        },
        {
          nome: "Email",
          icon: "mail.png",
          descricao:
            "Procurando por produtos no atacado? Faça uma cotação por email",
          link: "mailto:territoriodocalcado.camaqua@gmail.com?subject=Produtos%20por%20atacado&body=Tenho%20interesse%20em%20comprar%20por%20atacado.",
        },
        {
          nome: "Mercado Shops (ML) Vendas no atacado",
          icon: "ml.svg",
          descricao:
            "Compre tambem através do Mercado Livre",
          link: "https://territoriodocalcado.mercadoshops.com.br/",
        },
        {
          nome: "Mercado Livre",
          icon: "ml.svg",
          descricao:
            "Compre tambem através do Mercado Livre",
          link: "https://www.mercadolivre.com.br/perfil/TERRITORIODOCALCADO",
        },
        {
          nome: "Instagram",
          icon: "/instagram.png",
          descricao: "Nos siga para acompanhar as ultimas novidades",
          link: "https://www.instagram.com/territoriodocalc/",
        }
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
background: linear-gradient(0deg, rgba(252,189,24,1) 0%, rgba(255,255,255,1) 100%);
  background-repeat: no-repeat;
  background-size: cover;
}
.card {
  width: 100%;
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
  max-height: 2rem;
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
</style>
