# PostgreSQL Client

psql is PostgreSQL's command line tool. Use this container when you need to connect to a Postgres database via the command line but don't want to install the entire Postgres distribution, e.g. on macOS.

To run, enter:

`docker run --rm lenn4rd/psql`

You can create a `psql` shell alias:

`alias psql='docker run --rm -it -v $(pwd):/psql -v $HOME/.pgpass:/runner/.pgpass:ro lenn4rd/psql'`

Mounting the current working directory into the container enables you to pipe queries in and redirect query results to a local file. An example:

`psql -f query.sql > output.txt`

Mounting a `.pgpass` file into the user's home directory (in read-only mode) enables `psql` running in the container to look up configured connections.
