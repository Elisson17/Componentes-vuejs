<template>
  <div class="conversation-list">
    <h2 style="background-color:rgb(39, 39, 39); width: 209PX
    ; color: white;" >Chat</h2>
    <v-list class="listagem">
      <v-list-item
        v-for="contact in contacts"
        :key="contact.id"
       
        class="contact-item"
      >
        <v-list-item-avatar>
          <v-img class="contact-image" :src="contact.image"></v-img>
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title v-text="contact.name"></v-list-item-title>
          <v-list-item-subtitle v-text="contact.lastMessage"></v-list-item-subtitle>
        </v-list-item-content>
        <v-spacer></v-spacer>
      </v-list-item>
    </v-list>
  </div>


</template>


<script>



export default {
  
  data() {
    return {
      contacts: [
        {
          id: 1,
          name: "Eu",
          lastMessage: "Me responda",
          image: require("../assets/auau.jpeg"),
        }, {
          id: 2,
          name: "Diretor",
          lastMessage: "Me responda",
          image: require("../assets/auau.jpeg"),
        },{
        id: 3,
        name: "Orientador",
        lastMessage: "Me responda",
          image: require("../assets/auau.jpeg"),
        },{
        id: 4,
        name: "chefão",
        lastMessage: "Me responda",
          image: require("../assets/auau.jpeg"),
        }
        , {
          id: 5,
          name: "Homem de ferro",
          lastMessage: "Me responda",
          image: require("../assets/auau.jpeg"),
        }, {
          id: 6,
          name: "Cachorro do vizinho",
          lastMessage: "Me responda",
          image: require("../assets/auau.jpeg"),
        }, {
          id: 7,
          name: "Irmão",
          lastMessage: "Me responda",
          image: require("../assets/auau.jpeg"),
        }, {
          id: 8,
          name: "Deus"
          , lastMessage: "Olá cria blz?"
          ,image: require("../assets/auau.jpeg")
        }
        // Adicione mais contatos conforme necessário
      ],
    };
  },
  methods: {
  
  },
};
</script>

<style scoped>
.conversation-list {
  width: 225px;
  position: fixed;
  overflow:auto;
  height:560px;
  margin: auto;
}

.contact-item {
  display: flex;
  cursor: pointer;
  padding: 10px;
  transition: background-color 0.3s ease;
width: 100%;

}

.contact-item:hover {
  background-color: #f0f0f0;
}

.contact-image {
  width: 24px;
  height: 24px;
  border-radius: 50%;
  margin-right: 10px;
}
.listagem{
overflow-y: hidden; /* Adicione uma barra de rolagem apenas ao conteúdo da lista */

width: 209px;
left: 0px;

}
</style>
