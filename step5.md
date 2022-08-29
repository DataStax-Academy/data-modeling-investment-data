<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Sensor Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step4"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 5 of 7</span>
 <a href='command:katapod.loadPage?[{"step":"step6"}]'
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Design query Q2</div>

✅ Find hourly average temperatures for every sensor in network `forest-net` and date range [`2020-07-05`,`2020-07-06`] within the week of `2020-07-05`; order by date (desc) and hour (desc):

<details>
  <summary>Solution</summary>

```
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week       = '2020-07-05'
  AND date_hour >= '2020-07-05'
  AND date_hour  < '2020-07-07';
```

</details>

<br/>

✅ Find hourly average temperatures for every sensor in network `forest-net` and date range [`2020-07-04`,`2020-07-06`] within the weeks of `2020-06-28` and `2020-07-05`; order by date (desc) and hour (desc):

<details>
  <summary>Solution 1</summary>

```
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week       = '2020-07-05'
  AND date_hour >= '2020-07-04'
  AND date_hour  < '2020-07-07';
  
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week       = '2020-06-28'
  AND date_hour >= '2020-07-04'
  AND date_hour  < '2020-07-07';  
```

</details>

<details>
  <summary>Solution 2</summary>

```
SELECT date_hour, avg_temperature, 
       latitude, longitude, sensor 
FROM temperatures_by_network
WHERE network    = 'forest-net'
  AND week      IN ('2020-07-05','2020-06-28')
  AND date_hour >= '2020-07-04'
  AND date_hour  < '2020-07-07';  
```

</details>

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step4"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step6"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>

