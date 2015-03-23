---
layout: default
title: "Elastic Harvester.js"
---

# Elastic-Harvest

Elastic-Harvest is a Nodejs implementation of the [JSON API Search Profile](https://github.com/agco/agco-json-api-profiles).

This library ties together [harvester.js](https://github.com/agco/harvesterjs) and elasticsearch to offer the required [linked resource filtering and aggregation](https://github.com/agco/agco-json-api-profiles/blob/master/public/search-profile.md) features.

Apart from that it also provides a number of helper functions to synchronize harvester.js/mongoDB resources with an elasticsearch backend.

### Elasticsearch Tools

Find useful elastic-search tools as well as their documentation in /non-functionals.


## Features

- Aggregations : stats, extended_stats, top_hits, terms
- Primary and Linked resource filtering interop
- Top_hits aggregation interop with JSON API features, inclusion and sparse fieldsets [#6](https://github.com/agco-adm/elastic-harvest/issues/6)

## Roadmap

- More aggregations : min, max, sum, avg, percentiles, percentile_ranks, cardinality, geo_bounds, significant_terms, range, date_range, filter, filters, missing, histogram, date_histogram, geo_distance
- Reliable harvester.js/mongoDB - Elasticsearch data synchronisation ( oplog based )
- Support adaptive queries, use the ES mapping file to figure out whether to use parent/child or nested queries / aggregations
- Use Harvest associations + ES mapping file to discover which Mongodb collections have to be synced rather than having to register them explicitly
- Bootstrap elasticsearch with existing data from Harvest resources through REST endpoint
- Bootstrap elasticsearch mapping file through REST endpoint

## Dependencies
elasticSearch v1.4.0+

