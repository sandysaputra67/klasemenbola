<template>
  <div>
    <h2>Tampilan Klasemen</h2>
    <table class="table">
      <thead>
        <tr>
          <th>No</th>
          <th>Klub</th>
          <th>Ma</th>
          <th>Me</th>
          <th>S</th>
          <th>K</th>
          <th>GM</th>
          <th>GK</th>
          <th>Point</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(team, index) in teams" :key="index">
          <td>{{ index + 1 }}</td>
          <td>{{ team.club }}</td>
          <td>{{ team.ma }}</td>
          <td>{{ team.me }}</td>
          <td>{{ team.s }}</td>
          <td>{{ team.k }}</td>
          <td>{{ team.gm }}</td>
          <td>{{ team.gk }}</td>
          <td>{{ team.point }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      teams: [
        {
          club: "Persib",
          ma: 2,
          me: 2,
          s: 0,
          k: 0,
          gm: 4,
          gk: 0,
          point: 6,
        },
        {
          club: "Arema",
          ma: 2,
          me: 1,
          s: 0,
          k: 1,
          gm: 2,
          gk: 2,
          point: 3,
        },
        {
          club: "Persija",
          ma: 2,
          me: 0,
          s: 0,
          k: 2,
          gm: 0,
          gk: 4,
          point: 0,
        },
        {
          club: "psis",
          ma: 2,
          me: 0,
          s: 0,
          k: 2,
          gm: 0,
          gk: 4,
          point: 0,
        },
      ],
    };
  },
};
</script>
<style>
.table {
  margin: auto;
  width: 50% !important;
}
</style>
