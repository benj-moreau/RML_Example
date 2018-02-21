# RML_Example
An example of RML mapping to transform a JSON dataset to RDF.

# RML
[RML](http://rml.io/) is a generic scalable mapping language to express transformation of data of heterogeneous formats into RDF data.
The RML spec is available [here](http://rml.io/spec.html).
[RML-Mapper](https://github.com/RMLio/RML-Mapper) is a mapper that read an RML file to transform a non-RDF datasource into RDF.

# Transform a JSON dataset into RDF

In this example, we show how to use RML & RML-Mapper to transform a json dataset about [roman emperors](https://data.opendatasoft.com/explore/dataset/roman-emperors%40public/) into an RDF structure.

## Installation

Get RML-mapper by cloning [this repository](https://github.com/RMLio/RML-Mapper) and update dependencies by executing:

```bash
git clone --recursive https://github.com/RMLio/RML-Mapper.git

git submodule update --init --recursive
```

go into the RML-mapper directory and build it with:

```bash
bin/RML-Mapper
```

RML-Mapper is now ready to work.

## Run the example

Copy the mapping file (roman-emperors.rml file) and the json dataset (roman-emperors.json) into the RML-Mapper folder.

You can generate the RDF file (turtle by default) with this command:
```bash
bin/RML-Mapper -m <rml_file> -o <output_file>
```

For our example:
```bash
bin/RML-Mapper -m roman-emperors.rml -o roman-emperors.ttl
```

