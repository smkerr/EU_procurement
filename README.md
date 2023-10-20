# EU Procurement
This project analyzes EU procurement contract network data for the Applied Network Analysis course (GRAD-E1426) taught by [Phillip Lorenz-Spreen](https://www.mpib-berlin.mpg.de/staff/philipp-lorenz-spreen) at the [Hertie School](https://www.hertie-school.org/en/) in Berlin.

## Data
[`eu_procurements`](https://networks.skewed.de/net/eu_procurements): A bipartite network of public EU procurement contracts, from 2008 to 2016, between issuing buyers (public institutions such as a ministry or city hall) and supplying winners (a private firm). Contracts are aggregated into annual snapshots, edges are annotated with contract value information. Nodes are annotated with location information, including country of origin. The network contains 839,824 nodes and 4,098,711 links.

### Node properties
* `address`: the raw address of the entity          
* `canonical_name`: the most common name of the entity after deduplication   
* `country`: the country of the entity          
* `id_final`: the algorithmically deduplicated identifier of the entity         
* `name`: the raw name of the entity             
* `postcode`: the raw postcode of the entity       
* `sector`: the sector of the *issuer*         
* `town`: the raw town of the entity           
* `type`: the type of the *issuer* 

### Link properties
* `contract_cpv`: the raw CPV code of the contract  
* `contract_eu_funded`: 1 if the contract was supported by EU funding  
* `contract_nuts`: the raw NUTS geographic code of the contract's performance  
* `contract_type`: the type of the contract  
* `contract_value`: the raw value of the contract (currency/VAT unclear)  
* `cpv2`: the 2-digit CPV code of the contract  
* `date_dispatched`: the date of the contract  
* `est_value`: the raw estimated value of the contract (currency/VAT unclear)  
* `n_bids`: the number of bids received  
* `nocft`: 1 if there was no call for tenders found  
* `procedure`: what kind of procedure the contract was awarded under  
* `processed_nuts`: an imperfectly cleaned NUTS code  
* `single_bidder`: 1 if there was no competition for the contract (note: mean imputed at the country-level) 
* `tender_id`: an identifier for each contracts               
* `year`: the year of the contract                                     

## Method
* Throughout the project workflow, [Google Colab](https://colab.research.google.com/) is used to write and execute Python code. To enable use of the `graph-tool` package in the Colab environment, code provided [Tiago Peixoto (@count0)](https://github.com/count0/colab-gt/blob/master/colab-gt.ipynb) is used.
* The `eu_procurements` dataset was imported directly from the `graph-tools` package.

## Sources
* J. Wachs, M. Fazekas, and J. Kertész; Corruption Risk in Contracting Markets: A Network Science Perspective.&quot; International Journal of Data Science and Analytics, pp 1–16 (2020), https://link.springer.com/article/10.1007%2Fs41060-019-00204-1.
* Contracts data dictionary associated for the `eu_procurements` data set can be found [here](https://zenodo.org/records/3537986).

## Additional Resources
* [@briatte | A curated list of awesome network analysis resources. ](https://github.com/briatte/awesome-network-analysis)
* [networkD3 | D3 JavaScript Network Graphs from R](http://christophergandrud.github.io/networkD3/)
* [The R Graph Gallery | Network graph](https://r-graph-gallery.com/network.html)
* [Towards Data Science | Tutorial: Network Visualization Basics with Networkx and Plotly in Python](https://towardsdatascience.com/tutorial-network-visualization-basics-with-networkx-and-plotly-and-a-little-nlp-57c9bbb55bb9)
* [Yunran Chen | Introduction to Network Analysis Using R](https://yunranchen.github.io/intro-net-r/)
* [graph-tool](https://graph-tool.skewed.de/)
* [How to Use Graph-Tool in Google Colab](https://colab.research.google.com/github/count0/colab-gt/blob/master/colab-gt.ipynb#scrollTo=GQ18Kd5F3uKe)
