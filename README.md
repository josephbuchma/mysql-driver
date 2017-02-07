# MySQL Driver

### See [issue #1](https://github.com/gemnasium/migrate/issues/1#issuecomment-58728186) before using this driver!

* Runs migrations in transactions.
  That means that if a migration fails, it will be safely rolled back.
* Tries to return helpful error messages.
* Stores migration version details in table ``schema_migrations``.
  This table will be auto-generated.


## Usage

```bash
migrate -url mysql://user@tcp(host:port)/database -path ./db/migrations create add_field_to_table
migrate -url mysql://user@tcp(host:port)/database -path ./db/migrations up
migrate help # for more info
```

See full [DSN (Data Source Name) documentation](https://github.com/go-sql-driver/mysql/#dsn-data-source-name).

### SSL

The MySQL driver will set a TLS config if the following env variables are set:

- `MYSQL_SERVER_CA`
- `MYSQL_CLIENT_KEY`
- `MYSQL_CLIENT_CERT`

## Authors

* Matthias Kadenbach, https://github.com/gemnasium
