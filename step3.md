<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <span class="scenario-title">Investment Portfolio Data Modeling</span>
  <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span> 
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step2"}]' 
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 3 of 10</span>
 <a href='command:katapod.loadPage?[{"step":"step4"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Populate tables</div>

✅ Execute the CQL script to insert sample data:
```
SOURCE 'assets/investment_data.cql'
```

✅ Retrieve all rows from table `accounts_by_user`:
```
SELECT * FROM accounts_by_user;        
```

✅ Retrieve all rows from table `positions_by_account`:
```
SELECT * FROM positions_by_account;
```

✅ Retrieve all rows from table `trades_by_a_d`:
```
SELECT * FROM trades_by_a_d;                    
```

✅ Retrieve all rows from table `trades_by_a_td`:
```
SELECT * FROM trades_by_a_td;
```

✅ Retrieve all rows from table `trades_by_a_std`:
```
SELECT * FROM trades_by_a_std;       
```

✅ Retrieve all rows from table `trades_by_a_sd`:
```
SELECT * FROM trades_by_a_sd;       
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
