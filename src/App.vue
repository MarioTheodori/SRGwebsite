<template>
<div>
  <v-app>
    <v-app-bar color="white lighten-3" app clipped-right class="hover">
        <v-img
            class="mx-2"
            src="./assets/logo.png"
            height="10vw"
            max-height="50"
            max-width="50"
            contain
        ></v-img>
        <v-spacer></v-spacer>

        <a class="mx-2 d-none d-sm-block hover" @click="scroll('about')">{{about}}</a>
        <a class="mx-2 d-none d-sm-block hover" @click="scroll('service')">{{services}} </a>
        <a class="mx-2 d-none d-sm-block hover" @click="scroll('solution')">{{solutions}}</a>
        <a class="ml-2 mr-8 d-none d-sm-block hover" @click="scroll('contact')">{{contact}}</a>
        <v-spacer></v-spacer>
        <a class="mx-3 d-sm-block hover size" @click="isenglish=true">EN</a>
        <a class="mx-1 d-sm-block hover size" @click="isenglish=false">DE</a>
        <v-app-bar-nav-icon default class="d-sm-none" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-navigation-drawer
        clipped
        mobile-breakpoint
        absolute
        disable-resize-watcher
        class="d-sm-none header"
        v-model="drawer"
        right
        height="auto"
        ><div class="menu">
            <div class="line11"></div>
            <div class="line22"></div>
            <div class="line33"></div>
            
            <v-list
                nav
                dense
                class="list"
            >
                <v-list-item-group
                active-class=" text--accent-4"
                >
                <v-list-item class="fonts">
                    <v-list-item-title @click="scroll('about')">{{about}}</v-list-item-title>
                </v-list-item>
                <v-list-item class="fonts">
                    <v-list-item-title @click="scroll('service')">{{services}}</v-list-item-title>
                </v-list-item>
                <v-list-item class="fonts">
                    <v-list-item-title @click="scroll('solution')">{{solutions}}</v-list-item-title>
                </v-list-item>
                <v-list-item class="fonts">
                    <v-list-item-title @click="scroll('contact')">{{contact}}</v-list-item-title>
                </v-list-item>
                </v-list-item-group>
            </v-list>
          </div>
        </v-navigation-drawer>

    </v-app-bar>
    <v-content>    
    <div class="appContainer">
      <Aboutus class="top indexs" :english="isenglish" id="about"/>
      <Services :english="isenglish" id="service"/>
      <Solutions :english="isenglish" id="solution"/>
      <Contactus :english="isenglish" id="contact"/>
    </div>
    </v-content>
    <v-footer >
      <v-row>
        <v-dialog
          v-model="impressum"
          width="700"
          scrollable
          v-if="impressum"
        >
          <v-card>
            <v-btn
              icon
              dark
              @click="impressum = false"
            >
              <v-icon>mdi-close</v-icon>
            </v-btn>
            <v-card-title class="headline  lighten-2 redtext">
              Impressum
            </v-card-title>

            <v-card-text >
              SRG Handel und Dienstleistung Unternehmergesellschaft<br>
              Vertretungsberechtigter Geschäftsführer: Husam Shakeeb<br><br>

              Oststr. 20<br>
              47475 Kamp-Lintfort<br>
              info@srg-tech.com<br><br>

              Registergericht: Amtsgericht Kleve<br>
              Registernummer: HRB 17016<br>
            </v-card-text>
            <v-card-title class="headline lighten-2">
              Datenschutz
            </v-card-title>

            <v-card-text>
                Allgemeiner Hinweis und Pflichtinformationen<br>

                ‍Benennung der verantwortlichen Stelle<br>

                Die verantwortliche Stelle für die Datenverarbeitung auf dieser Website ist:<br>

                ‍SRG Handel un Dienstleistung Unternehmergesellschaft<br>
                Husam Shakeeb<br>
                Oststr. 20<br>
                47475 Kamp-Lintfort<br><br>

                ‍Die verantwortliche Stelle entscheidet allein oder gemeinsam mit anderen über die Zwecke und Mittel der Verarbeitung von personenbezogenen Daten (z.B. Namen, Kontaktdaten o. Ä.).<br>

                ‍‍Widerruf Ihrer Einwilligung zur Datenverarbeitung<br>
                ‍Nur mit Ihrer ausdrücklichen Einwilligung sind einige Vorgänge der Datenverarbeitung möglich. Ein Widerruf Ihrer bereits erteilten Einwilligung ist jederzeit möglich. Für den Widerruf genügt eine formlose Mitteilung per E-Mail. Die Rechtmäßigkeit der bis zum Widerruf erfolgten Datenverarbeitung bleibt vom Widerruf unberührt.<br><br>

                ‍‍Recht auf Beschwerde bei der zuständigen Aufsichtsbehörde<br>
                ‍Als Betroffener steht Ihnen im Falle eines datenschutzrechtlichen Verstoßes ein Beschwerderecht bei der zuständigen Aufsichtsbehörde zu. Zuständige Aufsichtsbehörde bezüglich datenschutzrechtlicher Fragen ist der Landesdatenschutzbeauftragte des Bundeslandes, in dem sich der Sitz unseres Unternehmens befindet. Der folgende Link stellt eine Liste der Datenschutzbeauftragten sowie deren Kontaktdaten bereit:<br>
                ‍https://www.bfdi.bund.de/DE/Infothek/Anschriften_Links/anschriften_links-node.html.<br><br>

                ‍Recht auf Datenübertragbarkeit<br><br>

                ‍‍Ihnen steht das Recht zu, Daten, die wir auf Grundlage Ihrer Einwilligung oder in Erfüllung eines Vertrags automatisiert verarbeiten, an sich oder an Dritte aushändigen zu lassen.<br>
                Die Bereitstellung erfolgt in einem maschinenlesbaren Format. Sofern Sie die direkte Übertragung der Daten an einen anderen Verantwortlichen verlangen, erfolgt dies nur, soweit es technisch machbar ist.<br><br>

                ‍‍Recht auf Auskunft, Berichtigung, Sperrung, Löschung<br><br>

                ‍‍Sie haben jederzeit im Rahmen der geltenden gesetzlichen Bestimmungen das Recht auf unentgeltliche Auskunft über Ihre gespeicherten personenbezogenen Daten, Herkunft der Daten, deren Empfänger und den Zweck der Datenverarbeitung und ggf. ein Recht auf Berichtigung, Sperrung oder Löschung dieser Daten. Diesbezüglich und auch zu weiteren Fragen zum Thema personenbezogene Daten können Sie sich jederzeit über die im Impressum aufgeführten Kontaktmöglichkeiten an uns wenden.<br><br>

                ‍SSL- bzw. TLS-Verschlüsselung<br><br>

                ‍‍Aus Sicherheitsgründen und zum Schutz der Übertragung vertraulicher Inhalte, die Sie an uns als Seitenbetreiber senden, nutzt unsere Website eine SSL-bzw. TLS-Verschlüsselung. Damit sind Daten, die Sie über diese Website übermitteln, für Dritte nicht mitlesbar. Sie erkennen eine verschlüsselte Verbindung an der „https://“ Adresszeile Ihres Browsers und am Schloss-Symbol in der Browserzeile.<br>
            </v-card-text>
            <v-card-title class="headline lighten-2">
              Kontaktformular
            </v-card-title>

            <v-card-text>
               ‍Per Kontaktformular übermittelte Daten werden einschließlich Ihrer Kontaktdaten gespeichert, um Ihre Anfrage bearbeiten zu können oder um für Anschlussfragen bereitzustehen. Eine Weitergabe dieser Daten findet ohne Ihre Einwilligung nicht statt.<br><br>

              Die Verarbeitung der in das Kontaktformular eingegebenen Daten erfolgt ausschließlich auf Grundlage Ihrer Einwilligung (Art. 6 Abs. 1 lit. a DSGVO). Ein Widerruf Ihrer bereits erteilten Einwilligung ist jederzeit möglich. Für den Widerruf genügt eine formlose Mitteilung per E-Mail. Die Rechtmäßigkeit der bis zum Widerruf erfolgten Datenverarbeitungsvorgänge bleibt vom Widerruf unberührt.<br><br>

              Über das Kontaktformular übermittelte Daten verbleiben bei uns, bis Sie uns zur Löschung auffordern, Ihre Einwilligung zur Speicherung widerrufen oder keine Notwendigkeit der Datenspeicherung mehr besteht. Zwingende gesetzliche Bestimmungen - insbesondere Aufbewahrungsfristen - bleiben unberührt.
            </v-card-text>
          </v-card>
        </v-dialog>
        <v-col
          class="text-right"
          cols="4"
        >
          {{ new Date().getFullYear() }} — <strong>SRG-Tech</strong>
        </v-col>
        <v-col class="text-right" cols="5">
          <a @click="impressum = true">Impressum & Datenschutz</a>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</div>
</template>

<script>
import Aboutus from './components/Aboutus.vue';
import Services from './components/Services.vue';
import Solutions from './components/Solutions.vue';
import Contactus from './components/Contactus.vue';
import zenscroll from 'zenscroll';


export default {
  name: 'App',

  components: {
    Aboutus,
    Services,
    Solutions,
    Contactus
  },

  data: () => ({
    drawer: false,
    impressum: false,
    isenglish: true,
    lang: " English"
  }),

  computed: {
      contact: function () {
          if (this.isenglish) {
              return`Contact Us`
          }
          return`Kontakt`
      },
      about: function () {
          if (this.isenglish) {
              return`About us`
          }
          return`Über uns`
      },
      solutions: function () {
          if (this.isenglish) {
              return`Solutions`
          }
          return`Lösungen`
      },
      services: function () {
          if (this.isenglish) {
              return`Services`
          }
          return`Dienstleistungen`
      }
      
  },
  methods: {
    scroll: function (id){
      var about = document.getElementById(id);
      zenscroll.to(about);
      this.drawer = false;
    }
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300&display=swap');
*{
  font-family: 'Space Grotesk', sans-serif !important;
  color: black !important;
}
.appContainer{
  display: flex;
  flex-direction: column;
}
.line11{
        grid-column: 1/1;
        grid-row: 1/-1;
        width: 5px;
        z-index: 2;
        height: 100%;
        background-color: red;
        justify-self: end;
    }
    .line22{
        grid-column: 2/-1;
        grid-row: 3/3;
        width: 100%;
        z-index: 2;
        height: 5px;
        background-color: red;
    }
    .line33{
        grid-column: 1/1;
        grid-row: 1/1;
        width: 100%;
        z-index: 2;
        height: 5px;
        background-color: red;
    }
.fonts{
  text-align: center;
}
.list{
  grid-column: 2/2;
  grid-row: 2/2;
}
.full{
  height: 100%;
  width: 100%;
  position: relative;
}
.menu{
    position: relative;
    width: 100%;
    height: 100%;
    display: grid;
    grid-template-columns:20% 80%;
    grid-template-rows: 2px auto 5px;
    overflow: hidden;
}
.size{
  font-size: 12px;
}
.redtext{
  border-top:5px solid red;
}
.hover a:hover{ border-top:3px solid red; }
</style>
