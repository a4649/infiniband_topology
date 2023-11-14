infiniband_topology
===================

A small web application to visualize an Infiniband fabric

It consists of two parts: a parser written in Python and a visualization application written in Javascript.

The parser:
- takes the output of the "ibnetdiscover" utility as it's input
- parses all the nodes and connections
- outputs this info into a .json file

The visualizer:
- loads the .json file
- displays the fabric topology using d3.js force layout
- allow you to interact with the visualization

How to use:

Install python2

```sudo dnf install python2 python2-virtualenv```

Create python2 virtualenv

```virtualenv --python=/usr/bin/python2 ib-topo-venv```

Activate virtualenv

```source ib-topo-venv/bin/activate```

Clone this repository

```git clone https://github.com/a4649/infiniband_topology.git```

Install requirements

```python -m pip install -r infiniband_topology/requirements.txt```

Parse your infiniband topology

```python topoparse.py my_cluster_ib_topology```

Rename output file

```mv my_cluster_ib_topology.json topo.json```

Open topo.html with your web browser

