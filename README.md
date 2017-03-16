# Docs

This doc is about how to build a structure to let the data consistent even when it depends on more than one service. (Simply microservice structure)

Install <a href="https://github.com/bumptech/glide">Glide</a> locally in you machine.

Clone <a href="https://github.com/RetailMarket/infra">Infra</a> repo.

# Getting Started

```
open cd scripts/
```

## clone all repos
```
sh ./cloneAll.sh
```

## Bundle all the required packages in all repos.
```
sh ./glideAll.sh
```

## Start all services by running script
```
sh ./startAll.sh
```

## Open UI
```
localhost:5000 (default)
```

You can see all the products with latest price.

Go ahead and update the price of any product.

If any of the service is down, then price will not be updated, once service comes up the price will automatically be updated.

![Flow](https://github.com/RetailMarket/docs/blob/master/flow.png)
