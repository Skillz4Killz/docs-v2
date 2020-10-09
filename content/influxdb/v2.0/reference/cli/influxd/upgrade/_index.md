---
title: influxd upgrade
description: The `influxd upgrade` command DOES TKD
menu:
  influxdb_2_0_ref:
    parent: influxd
weight: 201
products: [oss]
---

Use the `influxd upgrade` command to upgrade a 1.x version of InfluxDB to InfluxDB 2.0.
This will copy all data in [databases and retention policies]() (used in 1.x) over to [buckets]() (used in 2.0).

## Usage

```
influxd upgrade [flags]
influxd upgrade [command]
```

## Subcommands
| Subcommand                                                           | Description                    |
|:---------------------------------------------------------------------|:-------------------------------|
| [v1-dump-meta](/influxdb/v2.0/reference/cli/influxd/upgrade/v1-dump-meta/) | Dump InfluxDB 1.x meta.db      |
| [v2-dump-meta](/influxdb/v2.0/reference/cli/influxd/upgrade/v2-dump-meta/) | Dump InfluxDB 2.x influxd.bolt |
    
## Flags

| Flag |                | Description                                                   | Input type |
|:-----|:---------------|:--------------------------------------------------------------|:----------:|
| `-h` | `--help`       | Help for the `upgrade` command                                |            |
|      | --v1-meta-dir  | Path to 1.x meta.db directory (default "`~/.influxdb/meta`")  | string     |
|      | --v2-bolt-path | Path to 2.0 metadata (default "`~/.influxdbv2/influxd.bolt`") | string     |
