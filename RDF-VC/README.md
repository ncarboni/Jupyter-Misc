# Workflow for VC RDF data

Use [OpenRefine_to_XML](OR_to_XML.ipynb) to download the project corpus and save it in XML. Afterwards transform the XML data to RDF using [X3ML](https://github.com/isl/x3ml)

The transformation in RDF requires three files:
+ A mapping file
+ A URL policy (generator policy)
+ An input file

In the folder Metadata_corpus there are the ncessary files to transform the corpus in RDF
In the folder Cluster_image_explore there are the ncessary files to transform the Cluster< ->image relationships (extracted from Explore) into RDF

## Transformation

The command to use X3ML to transform XML in RDF is 

```bash
java -jar /path/to/x3ml-engine-2.1.0-exejar.jar -x mapping_schema.x3ml -p generator_policy.xml -i input.xml -o output.ttl -f text/turtle
```


## Model

The mapping file follow the Data Model 
![Data Model](data_model.png)