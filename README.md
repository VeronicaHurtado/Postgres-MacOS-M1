# Setup Postgres and pgAdmin on MacOS - M1

## Postgres

Install the version of postgres you would like using Homebrew:
`brew install postgresql@11`

Add the path to your .zshrc file:
`'export PATH="/opt/homebrew/opt/postgresql@11/bin:$PATH"' >> ~/.zshrc`

Apply the changes by running:
`source ~/.zshrc`

Start the server:
`postgres -D /opt/homebrew/var/postgresql@11`

You can access the postgres database with:
`psql postgres`

## pgAdmin

Download and install pgAdmin: https://www.pgadmin.org/download/pgadmin-4-macos/

Open pgAdmin

Right-click on the Servers group

Select Register > Server...

Set the connection according to the output from the `postgres -D /opt/homebrew/var/postgresql@11` command that you ran 
in the previous section.

e.g.:
```	
Host name/address: 127.0.0.1
Port: 5432
Maintenance database: postgres
Username: <type your username>
```
Click Save.

You should now see the new connection under Servers with access to the postgres database.