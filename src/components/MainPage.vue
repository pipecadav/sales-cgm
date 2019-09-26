<template>
  <v-container>
    <h1>
      Competitor Growth Mapping
    </h1>
    <v-form v-model="valid">
      <v-container>
        <v-row>
          <v-col cols="12" md="2">
            <v-text-field
              v-model="searchTerm"
              :rules="valueRules"
              label="Search Term"
              required
            />
          </v-col>
  
          <v-col cols="12" md="2">
            <v-text-field
              v-model="startDate"
              :rules="valueRules"
              label="Start Date"
              required
            />
          </v-col>
  
          <v-col cols="12" md="2">
            <v-text-field
              v-model="endDate"
              :rules="valueRules"
              label="End Date"
              required
            />
          </v-col>

          <v-col cols="12" md="2">
            <v-text-field
              v-model="frequency"
              :rules="valueRules"
              label="Frequency"
              required
            />
          </v-col>

          <v-col cols="12" md="4">
            <v-btn @click="loadCards()">
              Submit
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-form>
    <div
      class="graphs"
      v-for="(card, index) in cards"
      :key = index
    >
    </div>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      valid: false,
      searchTerm: '',
      startDateSelected: '',
      endDateSelected: '',
      intervalSelected: '',
      periods: [],
      cards: [],
      valueRules: [
        v => !!v || 'Required',
      ],
    }
  },
  methods: {
    loadCards() {
    },
    divideByWeeks(){
      const startDate = new Date(this.startDateSelected)
      const endDate = new Date(this.endDateSelected)
      const interval = new interval(this.intervalSelected)
      
      
    },
    divideByMonths(){

    },
    divideByDays(){}

  }
};
</script>
