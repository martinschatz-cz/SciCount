Data origin
===========

`The Long-Term Evolution Experiment <the-ltee.org>`_

Goal
====

Given an image of a Petri dish with agar substrate and two types of E. Coli
bacterial colonies differing by color, enumerate and clasify colonies into 
two categories. Perform statistical analysis of colonies' properties, such as 
surface area, circularity, excentricity, etc.


Proposed workflow
=================

#. Mask out everything but agar with colonies.
#. Adjust colors to cast agar into background.
#. Make a suitable projection to eliminate color difference between colonies.
#. Use a neural network to detect colonies.
#. Make a different projection to emphasize color difference between colonies.
#. Categorize colonies by color.
#. Apply detection and categorization masks to original picture for statistical analysis.


Hitches
=======

* Petri dish not exactly circular and has marks on the side which cast shadow, they also rotate.
* Agar background changes color.
* Color difference between categories changes - threshold must be dynamic.
* Size of colonies changes dramatically, there can be many overlaps.
