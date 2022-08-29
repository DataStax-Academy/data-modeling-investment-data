<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step2"}]' 
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 3 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step4"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Populate tables</div>

✅ Execute the CQL script to insert sample data:
```
SOURCE 'assets/sensor_data.cql'
```

✅ Retrieve all rows from table `networks`:
```
SELECT * FROM networks;        
```

✅ Retrieve all rows from table `temperatures_by_network`:
```
SELECT network, week, date_hour, 
       sensor, avg_temperature 
FROM temperatures_by_network;
```

✅ Retrieve all rows from table `sensors_by_network`:
```
SELECT * FROM sensors_by_network;                    
```

✅ Retrieve all rows from table `temperatures_by_sensor`:
```
SELECT * FROM temperatures_by_sensor; 
```

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step2"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step4"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>
