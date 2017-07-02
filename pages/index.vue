<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="text-xs-center">
        <img src="/v.png" alt="Vuetify.js" class="mb-5" />
      </div>
      <v-card>
        <v-card-text>
          <v-dialog
            persistent
            v-model="modal2"
            lazy
          >
            <v-text-field
              slot="activator"
              label="Picker in dialog"
              v-model="e6"
              prepend-icon="access_time"
              readonly
            ></v-text-field>
            <v-time-picker v-model="e6" actions>
              <template scope="{ save, cancel }">
                <v-card-row actions>
                  <v-btn flat primary @click.native="cancel()">Cancel</v-btn>
                  <v-btn flat primary @click.native="save()">Save</v-btn>
                </v-card-row>
              </template>
            </v-time-picker>
          </v-dialog>
          <p>Welcome to the Webpack SSR template.</p>
          <p>Vuetify is a progressive Material Design component framework for Vue.js. It was designed to empower developers to create amazing applications. For more information on Vuetify, check out the <a href="https://vuetifyjs.com" target="_blank">documentation</a>. If you have questions, please join the official <a href="https://gitter.im/vuetifyjs/Lobby" target="_blank" title="chat">gitter</a>. Find a bug? Report it on the github <a href="https://github.com/vuetifyjs/vuetify/issues" target="_blank" title="contribute">issue board</a>.</p>
          <p>Thank you for developing with Vuetify and I look forward to bringing more exciting features in the future.</p>
          <div class="text-xs-right">
            <em><small>&mdash; John Leider</small></em>
          </div>
        </v-card-text>
        <v-card-row actions>
          <v-btn primary flat router to="/inspire">Continue</v-btn>
        </v-card-row>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data () {
    return {
      modal2: false,
      e6: ''
    }
  }
}
</script>
