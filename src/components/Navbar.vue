<template>
    <nav>
        <v-app-bar flat app color="#041c2c">
            <v-app-bar-nav-icon class="white--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title class="text-uppercase white--text grey--light">
             <span class="font-weight-light">Todo</span> 
             <span>Stuff</span>  
            </v-toolbar-title>   
            <v-spacer></v-spacer>
            <v-btn small flat color="#041c2c">
                
                <v-icon small color="white">mdi-location-exit</v-icon>
            </v-btn> 
        </v-app-bar> 

        <v-navigation-drawer v-model="drawer" app class="primary">
            <v-list>
                <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                    <v-list-item-action>
                        <v-icon class="white--text">{{link.icon}} </v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title class="white--text">
                            {{link.text}}
                        </v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            drawer: false,
            links: [
                {icon: 'mdi-view-dashboard', text: 'Dashboard', route: '/'},
                {icon: 'mdi-folder', text: 'My Projects', route: '/Projects'},
                {icon: 'mdi-account', text: 'Team', route: '/Team'},
                  {icon: 'mdi-exit-to-app', text: 'Login', route: '/Login'}
            ]
        }
    }    
}
</script>