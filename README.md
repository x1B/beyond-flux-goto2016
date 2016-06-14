# Beyond Flux

> Scalable front-end architecture using publish/subscribe, talk given at [goto;amsterdam](http://gotocon.com/amsterdam-2016/) 2016

- The [PDF slides](beyond_flux.pdf) for download.

- To view the original HTML slides (source under `./slides`):

```sh
git clone https://github.com/x1B/beyond-flux-goto2016/
cd beyond-flux-goto2016
npm install
npm start
# Ctrl+C to stop
```

URL: http://localhost:9200/


- To access the demos (unter `demos`):

```sh
# prepare as for the slides (above)
npm run install-demos
npm start
```

URLs:
 - Flux ([Yahoo Fluxible](http://fluxible.io/)): http://localhost:9200/demos/flux-comparison-simplified/yahoo-fluxible/
 - Redux: http://localhost:9200/demos/flux-comparison-simplified/redux/
 - Pub/Sub ([LaxarJS](http://laxarjs.org/)): http://localhost:9200/demos/flux-comparison-simplified/pubsub-laxar/
