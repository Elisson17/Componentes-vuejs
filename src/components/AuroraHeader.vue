<template >
    <div class="all">
<v-app-bar theme="dark" absolute class="border-b"  position="fixed">
    <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

    <v-app-bar-title><v-img width="230px" height="auto" src="../assets/logo_aurora.png"></v-img></v-app-bar-title>

    <template #append>
    <v-btn icon class="mr-2">
<v-badge dot color="info">
    <v-icon icon="mdi-bell-outline" ></v-icon>

</v-badge>
    </v-btn>        
    <v-avatar color="white">
        <v-img  src="../assets/perfil.png" >

        </v-img>
    </v-avatar>
        
    </template>
</v-app-bar>
<v-navigation-drawer width="110px" v-model="drawer" location="left" temporary >
    <v-list density="comfortable" nav>
        <v-list-item prepend-icon="mdi-align-vertical-bottom"  value="dashboard"  title="Dashboard">
    </v-list-item>
<v-list-item prepend-icon="mdi-monitor"  value="monitor"  title="Monitoramento">
</v-list-item>
    <v-list-item prepend-icon="mdi-card-account-phone"  value="Conversa"  title="Conversa">
    </v-list-item>
    
    </v-list>
    
</v-navigation-drawer>

</div>
</template>
<script>
export default {
   data() {
        return {
            drawer: false
        }
    }, methods: {
        
    }
    
}
</script>
<style scoped>

.all{
    overflow-y: hidden;
}

</style>