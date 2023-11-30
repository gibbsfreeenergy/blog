<template>
    <v-card class="card">
        <v-card-title primary-title>
        <div>
            <h3 class="headline mb-0 title">火车票信息</h3>
            <div>车次: {{ trainNumber }}</div>
        </div>
        </v-card-title>

        <v-card-text>
        <div class="info">
            <div class="info-item">
            <strong>出发站:</strong> {{ departureStation }}
            </div>
            <div class="info-item">
            <strong>到达站:</strong> {{ arrivalStation }}
            </div>
        </div>

        <div class="info">
            <div class="info-item">
            <strong>出发时间:</strong> {{ departureTime }}
            </div>
            <div class="info-item">
            <strong>到达时间:</strong> {{ arrivalTime }}
            </div>
        </div>
        </v-card-text>
    </v-card>
</template>
  
  
<script>
  export default {
    props: {
      trainNumber: String,
      departureStation: String,
      arrivalStation: String,
      departureTime: String,
      arrivalTime: String,
    },
  };
  </script>
  
  <style scoped>
  .card {
    max-width: 400px;
    margin: auto;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  .title {
    font-size: 1.2em;
    margin-bottom: 8px;
  }

  .info {
    display: flex;
    justify-content: space-between;
    margin-bottom: 16px;
  }

  .info-item {
    flex: 1;
    margin-right: 8px;
  }

  .actions {
    display: flex;
    justify-content: flex-end;
  }
</style>
