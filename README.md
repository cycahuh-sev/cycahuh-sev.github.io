<!-- public_sensor.html -->
<script>
fetch('https://your-ha:8123/api/states/sensor.temperature', {
  headers: { 'Authorization': 'Bearer YOUR_TOKEN' }
})
.then(r => r.json())
.then(data => {
  document.getElementById('temp').innerText = data.state + '°C';
});
</script>
<div>Температура: <span id="temp"></span></div>
