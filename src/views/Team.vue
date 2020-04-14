<template>
    <div class="team">
       
        <v-container my-2>
          <v-row>
            <v-col>
              <v-card  :class="`pa-4 job ${job.STS}`" v-for="job in jobs" :key="job.STD">
                <v-layout>
                  <v-flex >
                    <div class="caption grey--text text-left">STD</div>
                    <div class="">{{ job.STD }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Registration</div>
                    <div class="">{{ job.REG }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Airline</div>
                    <div class="">{{ job.AIR }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Stand</div>
                    <div class="">{{ job.STA }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Status</div>
                    <div :class="`caption jobtxt ${job.STS}`">{{ job.STS }}</div>
                  </v-flex>
                </v-layout>
                
              </v-card>
            </v-col>
            <v-spacer></v-spacer>
            <v-col>
              <div>
              <v-card  :class="`pa-4 job ${job.STS}`" v-for="job in jobs" :key="job.STD">
                <v-layout>
                  <v-flex >
                    <div class="caption grey--text text-left">STD</div>
                    <div class="">{{ job.STD }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Registration</div>
                    <div class="">{{ job.REG }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Airline</div>
                    <div class="">{{ job.AIR }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Stand</div>
                    <div class="">{{ job.STA }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Status</div>
                    <div :class="`caption jobtxt ${job.STS}`">{{ job.STS }}</div>
                  </v-flex>
                </v-layout>
              </v-card>
              </div>
              <div style="margin-top:10px;">
              <v-card :class="`pa-4 job ${job.STS}`" v-for="job in jobs" :key="job.STD">
                <v-layout>
                  <v-flex >
                    <div class="caption grey--text text-left">STD</div>
                    <div class="">{{ job.STD }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Registration</div>
                    <div class="">{{ job.REG }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Airline</div>
                    <div class="">{{ job.AIR }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Stand</div>
                    <div class="">{{ job.STA }}</div>
                  </v-flex>
                  <v-flex >
                    <div class="caption grey--text text-left">Status</div>
                    <div :class="`caption jobtxt ${job.STS}`">{{ job.STS }}</div>
                  </v-flex>
                </v-layout>
              </v-card>
              </div>
            </v-col>
          </v-row>  
        </v-container>
    </div>
</template>
<script>
export default {
    data() {
      return {
        jobs: [
          { ID: '453452', STD: '14:45', REG: 'OY4545', AIR: 'SAS', STA: 'W34', STS: 'Assigned'},
          { ID: '453451', STD: '13:35', REG: 'NO2323', AIR: 'NOW', STA: 'W09', STS: 'Done'},
          { ID: '453450', STD: '15:15', REG: 'LH1232', AIR: 'LH', STA: 'E23', STS: 'Done'},
          { ID: '453449', STD: '14:45', REG: 'OY4545', AIR: 'SAS', STA: 'N22', STS: 'OnGoing'},
          { ID: '453448', STD: '13:35', REG: 'NO2323', AIR: 'NOW', STA: 'E42', STS: 'Assigned'},
          { ID: '453447', STD: '15:15', REG: 'LH1232', AIR: 'LH', STA: 'W11', STS: 'OnGoing'},
          { ID: '453446', STD: '14:45', REG: 'OY4545', AIR: 'SAS', STA: 'E44', STS: 'OnGoing'},
          { ID: '453445', STD: '13:35', REG: 'NO2323', AIR: 'NOW', STA: 'N12', STS: 'Assigned'},
          { ID: '453444', STD: '15:15', REG: 'LH1232', AIR: 'LH', STA: 'E22', STS: 'New'}
        ]
      }
    }
}
</script>
<style>
.flex {
  max-width: 140px;
  
}
.jobtxt.Assigned {
  color: lightgreen;
  
}
.jobtxt.Done {
  color: green;
}
.jobtxt.New {
  color: lightcoral;
}
.jobtxt.OnGoing {
  color: lightblue;
}
.job.Assigned {
  border-left: 4px solid lightgreen;
  padding-left: 4px;
  margin-left: -5px;
}
.job.Done {
  border-left: 4px solid green;
  margin-left: -5px;
}
.job.New {
  border-left: 4px solid lightcoral;
  margin-left: -5px;
}
.job.OnGoing {
  border-left: 4px solid lightblue;
  margin-left: -5px;
}
</style>