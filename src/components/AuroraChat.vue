<template>
    <div class="chat">
        <div class="chat-msg" >



<div class="msg-me-left">
    ghfdsgfdsgdfsgdf
</div>




    <!-- Aqui fica onde a msg é enviada quando é digitado e dá enter-->
        <v-list class="msg-me-rigth" >
            <v-list-item style="
flex-direction: column;

border-style: solid;

border-width: 1px;
border-radius: 20%;

"  v-for="(message, index) in chat" :key="index">
                {{ message.sender }}: {{ message.content }} 
            </v-list-item>
        </v-list>
    
    
    </div>
        <div class="input-container">
            <input class="input" type="text" v-model="newMessage" @keyup.enter="sendMessage" />
            <v-btn style="background-color: orangered;" icon="mdi-send" @click="sendMessage"></v-btn>
        </div>
    </div>
</template>

<script>
export default {
    components: {
    },
    data() {
        return {
            chat: [],
            newMessage: "",
        };
    },
    methods: {
        sendMessage() {
            if (this.newMessage.trim() !== "") {
                this.chat.push({
                    sender: "Você", // Defina o remetente como desejar
                    content: this.newMessage,
                });
                this.newMessage = "";
            }
        },
    },
};
</script>

<style scoped>
.chat {
    height: 100%;
    margin: auto;
    width: 70%;
    float: right;
}

.input-container {
    display: flex;
    align-items: center;
    margin-top: auto;

}

.input {
    flex: 1;
    width: 250px;
    border-style: solid;
    border-width: 1px;
    border-radius: 15px;
    padding: 10px;
    margin: 0 40px;
}

.msg-me-rigth{
    width: 50%;
    float: right;
}
.msg-me-left{
width: 50%;
    float: left;
}
.chat-msg{
    height: 81vh;
    margin-top: auto;
}

</style>
