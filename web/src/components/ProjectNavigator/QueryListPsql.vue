<template>
  <div>
    <v-btn
      @click="newQuery"
    >New PSQL Query</v-btn>
    <h2>a list of named raw sql queries that can be used ad-hoc during dev</h2>
    <!-- <v-btn>New GraphQL Test</v-btn>
     <v-list>
      <template v-for="(test, index) in tests">
        <v-list-tile
          :key="test.id"
          ripple
          @click="selected(test)"
          :class="test.id === focusPatch.id ? 'v-list__tile--active' : 'v-list__tile'"
        >
          <v-list-tile-content>
            <v-list-tile-sub-title class="text--primary">{{ `${test.name}` }}</v-list-tile-sub-title>
          </v-list-tile-content>

        </v-list-tile>
        <v-divider
          v-if="index + 1 < tests.length"
          :key="index"
        ></v-divider>
      </template>
    </v-list>         -->
  </div>
</template>

<script>

export default {
  name: "QueryListPsql",
  components: {
  },
  methods: {
    newQuery () {
      console.log('this.minorId', this.minorId)
      this.$store.commit('focusMinorId', this.minorId)
      this.$router.push({ name: 'new-psql-query' })
    },
    selected (test) {
      // this.$router.push({ name: 'new-psql-query' })
    }
  },
  computed: {
  },
  watch: {
  },
  props: {
    minorId: {
      type: String,
      required: false,
      default: ''
    }
    // tests: {
    //   type: Array,
    //   required: true
    // }
  },
  data () {
    return {
      focusPatch: {}
    }
  },
}
</script>
