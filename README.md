# JS graph library comparison

## Description

This is a comparison of JS graph libraries, loading real-life user data.  The data, [Wei2.cys](https://github.com/cytoscape/cytoscape-tests/blob/master/docs/Session-Files/Wei-Zhang/Wei_2.cys), is taken from the [`cytoscape/cytoscape-test`](https://github.com/cytoscape/cytoscape-tests) repository.  It is a protein-protein interaction graph, containing 104 nodes and 2000 edges.

This repository aims to fairly compare the libraries, with the same data, as similar settings as possible, and as similar rendering output as possible.

## Libraries & notes

- [Cytoscape.js](http://cytoscape.github.io/js-graph-lib-comparison/cytoscape)
 - Near instant results
 - Style kept minimalistic to match with Sigma.js and VivaGraph.js
- [Sigma.js](http://cytoscape.github.io/js-graph-lib-comparison/sigma)
 - Near instant first frame
 - The layout takes some seconds to stabilise
 - The layout must be stopped manually, because Sigma's physics layout does not support autostopping on a stabilised state
 - The layout is stopped after 3 seconds in this demo
 - Only simple styling is supported, like setting node colour
- [VivaGraph.js](http://cytoscape.github.io/js-graph-lib-comparison/vivagraph)
 - Near instant first frame
 - The VivaGraph WebGL renderer is set here to give VivaGraph a fairer comparison (SVG is default)
 - The layout can not be stopped (automatically or manually)
 - The layout options were optimised to give better results than the default and to have some stabilisation
 - The layout does not ever fully stabilise
 - No styling is documented other than setting a background image for the nodes using SVG
 - Labels do not appear to be supported
