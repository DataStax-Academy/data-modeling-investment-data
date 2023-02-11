<!-- TOP -->
<div class="top">
  <img class="scenario-academy-logo" src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Investment Portfolio Data Modeling</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span>
  </div>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 2 of 10</span>
 <a href='command:katapod.loadPage?[{"step":"step3"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Create tables</div>

✅ Create table `accounts_by_user`:
```
CREATE TABLE IF NOT EXISTS accounts_by_user (
  username TEXT,
  account_number TEXT,
  cash_balance DECIMAL,
  name TEXT STATIC,
  PRIMARY KEY ((username),account_number)
);
```

✅ Create table `positions_by_account`:
```
CREATE TABLE IF NOT EXISTS positions_by_account (
  account TEXT,
  symbol TEXT,
  quantity DECIMAL,
  PRIMARY KEY ((account),symbol)
);
```

✅ Create table `trades_by_a_d`:
```
CREATE TABLE IF NOT EXISTS trades_by_a_d (
  account TEXT,
  trade_id TIMEUUID,
  type TEXT,
  symbol TEXT,
  shares DECIMAL,
  price DECIMAL,
  amount DECIMAL,
  PRIMARY KEY ((account),trade_id)
) WITH CLUSTERING ORDER BY (trade_id DESC);
```

✅ Create table `trades_by_a_td`:
```
CREATE TABLE IF NOT EXISTS trades_by_a_td (
  account TEXT,
  trade_id TIMEUUID,
  type TEXT,
  symbol TEXT,
  shares DECIMAL,
  price DECIMAL,
  amount DECIMAL,
  PRIMARY KEY ((account),type,trade_id)
) WITH CLUSTERING ORDER BY (type ASC, trade_id DESC);
```

✅ Create table `trades_by_a_std`:
```
CREATE TABLE IF NOT EXISTS trades_by_a_std (
  account TEXT,
  trade_id TIMEUUID,
  type TEXT,
  symbol TEXT,
  shares DECIMAL,
  price DECIMAL,
  amount DECIMAL,
  PRIMARY KEY ((account),symbol,type,trade_id)
) WITH CLUSTERING ORDER BY (symbol ASC, type ASC, trade_id DESC);
```

✅ Create table `trades_by_a_sd`:
```
CREATE TABLE IF NOT EXISTS trades_by_a_sd (
  account TEXT,
  trade_id TIMEUUID,
  type TEXT,
  symbol TEXT,
  shares DECIMAL,
  price DECIMAL,
  amount DECIMAL,
  PRIMARY KEY ((account),symbol,trade_id)
) WITH CLUSTERING ORDER BY (symbol ASC, trade_id DESC);
```

✅ Verify that the six tables have been created:
```
DESCRIBE TABLES;
```

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step3"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>
