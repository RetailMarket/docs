# docs

This doc is about how to build a structure to let the data consistent even when it depends on more than one service. (Simply microservice structure)

# Setup
clone scripts repo and run 'cloneAll.sh'

After that, run 'glideAll.sh', it will bundle all the required packages in all repos.

Start all services by running script 'startAll.sh'

Open localhost:5000 in browser

You can see all the products with latest price.

Go ahead and update the price of any product.

If any of the service is down, then price will not be updated, once service comes up the price will be automatically be updated.

# See the image url: <img src="https://github.com/RetailMarket/docs/blob/master/flow.png"></img>
