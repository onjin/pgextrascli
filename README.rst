===============================
pgextras CLI
===============================

.. image:: https://badge.fury.io/py/pgextrascli.png
    :target: http://badge.fury.io/py/pgextrascli
    
.. image:: https://travis-ci.org/onjin/pgextrascli.png?branch=master
        :target: https://travis-ci.org/onjin/pgextrascli

.. image:: https://pypip.in/d/pgextrascli/badge.png
        :target: https://pypi.python.org/pypi/pgextrascli


Simple command line wrapper for https://github.com/scottwoodall/python-pgextras

* Free software: BSD license

Install
-------

.. code-block::

  $ pip install pgextrascli


Usage
-----
Usage: pgextrascli [OPTIONS] CMD

Options:

.. code-block::

  $ pgextrascli --help

  -l, --list-commands  shows available commands
  --host=HOST          database host, default: localhost
  --port=PORT          database port, default: 5432
  --dbname=DBNAME      database name, default: template1
  --user=USER          database user, default: postgres
  --password=PASSWORD  database password, default: empty
  --help               Show this message and exit.

Available commands:

.. code-block::

  $ pgextrascli -l

  bloat                          Table and index bloat in your database ordered by most wasteful.
  blocking                       Queries holding locks other queryes are qaiting to be releases
  cache_hit                      Calculates your cache hit rate (effective databases are at 99% and up).
  calls                          Show 10 most frequently called queries. Requires the pg_stat_statements.
  index_usage                    Calculates your index hit rate (effective databases are at 99% and up).
  locks                          Display queries with active locks.
  long_running_queries           Show all queries longer than five minutes by descending duration.
  outliers                       Show 10 queries that have longest execution time in aggregate. Requires the pg_stat_statments.
  ps                             View active queries with execution time.
  seq_scans                      Show the count of sequential scans by table descending by order.
  total_table_size               Show the size of the tables (including indexes), descending by size.
  unused_indexes                 Show unused and almost unused indexes, ordered by their size relative to the number of index scans.
  vacuum_stats                   Show dead rows and whether an automatic vacuum is expected to be triggered.
  version                        Get the Postgres server version.
