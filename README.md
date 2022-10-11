# founderblockgraphs
Constructs segment repeat-free founder block graphs from multiple sequence alignments

# getting started
Clone this repository, install sdsl-lite and compile:
```
git clone --recurse-submodules https://github.com/nrizzo/founderblockgraphs
cd founderblockgraphs/sdsl-lite
./install.sh
cd ..
make
```

# usage
For computing a semi-repeat-free segmentation minimizing the maximum segment length:
```
./founderblockgraph --elastic --input=test.fasta --output=tempindex --graphviz=tempgraphviz.dot
```
Visualization can be done with [Graphviz](https://graphviz.org/):
```
dot -Tsvg tempgraphviz -o tempgraph.svg
```
If the graph is very big, I did have success visualizing:
 - the svg/pdf output of graphviz, with Chrome/Chromium's pdf viewer
 - the dot file, using [Gephi](https://gephi.org/) with the Graphviz layout (it's a plugin that can be installed, also remember to choose a big "Max size" value in Tools>Options>Visualization>OpenGL)
