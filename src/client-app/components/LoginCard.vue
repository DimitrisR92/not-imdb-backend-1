<template>
   <v-card
        class="mx-auto grey darken-3"
        max-width="500"
      >
        <v-card-title>Login</v-card-title>
        <v-card-text>
            <v-form>
                <v-row
                align="center"
                class="mx-0"
                >
                    <v-text-field
                        class="pa-16 white--text"
                        label="username"
                    ></v-text-field> 
                </v-row>
                <v-row
                align="center"
                class="mx-0"
                >
                    <v-text-field
                        class="pa-16 input-group--focused white--text"
                        label="Password"
                        hint="At least 8 characters"
                        :append-icon="show ? 'mdi-eye' : 'mdi-eye-off'"
                        :type="show ? 'text' : 'password'"
                        error
                        @click:append="show = !show"
                    ></v-text-field>
                </v-row>
                <v-row
                align="center"
                class="mt-8"
                >
                <v-col>
                    <v-btn
                    class="ma-8"
                    color="black white--text"
                    >
                    Log In
                    </v-btn>
                </v-col>
                <v-col>
                    <v-btn
                    class="ma-8"
                    color="black white--text"
                    >
                    Use SSO
                    </v-btn>
                </v-col>
                </v-row>
                <v-row
                align="center"
                class="mt-8"
                >
                    <nuxt-link to="/Register">Not Registered? Sign Up here</nuxt-link>
                </v-row>
            </v-form>
        </v-card-text>
      </v-card>
</template>

<script>
export default {
    name:'LoginCard',
    data(){
        return{
            show : false
        }
    },
}
</script>

<style>

</style>