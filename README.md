# Riak Protocol Buffers Client Pool

[![Build Status][travis_ci_image]][travis_ci]

About
=========

Riak client connection pool using poolboy

Usage
=========

```erlang
SizeArgs = [{size, 10},
            {max_overflow, 20}],
WorkerArgs = [{hostname, "127.0.0.1"},
              {port, 8087},
              {options, [{auto_reconnect, true}]}],
PoolName = badger_pool,
riakc_poolboy:start_pool(PoolName, SizeArgs, WorkerArgs),


riakc_poolboy:stop_pool(PoolName).
```

TODO
=========

* Support streaming functions
* Tests

[travis_ci]: https://travis-ci.org/puzza007/riakc_poolboy
[travis_ci_image]: https://travis-ci.org/puzza007/riakc_poolboy.png
