# Docs

This doc is about how to build a structure to let the data consistent even when it depends on more than one service. (Simply microservice structure)

### Machine Setup

* Install `golang` 1.7 
* Install [glide](https://github.com/Masterminds/glide).

## Project setup

1. clone <a href="https://github.com/RetailMarket/infra">Infra</a> repo.
2. open scripts `cd scripts/`
3. close all repos `./cloneAll.sh`
4. glide install `./glideAll.sh`

## Bring up services
```
Do `./start_server.sh` in PriceManager, Workflow, priceSync, workflowsync, priceWeb.
```

The web service should be available at `http://localhost:5000`

## Steps to check flow

Open the above url.

You can see some products with there price.

Go ahead and update the price of any product.

Refresh the page after 5 sec(jobs are scheduled after every 5 sec).

You will see that the price was updated.

Now stop any service except **priceWeb**.

Then update the price of any product again and refresh the page after 5 sec.

You will see that the price didn't change.

Now start the service again which you have stopped.

Come back to UI, wait for 5 sec and refresh the page again.

Now you will see that the price has been updated.

If any of the service is down, then updation will not take place, once service comes up the updation will happen automatically.

![Flow](https://github.com/RetailMarket/docs/blob/master/flow.png)
