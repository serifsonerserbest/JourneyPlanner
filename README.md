# Robust Journey Planner

This project is the term project of the Artificial Neural Networks course at Swiss Federal Institute of Technology Lausanne (EPFL). Details about the course can be found [here](https://edu.epfl.ch/coursebook/en/lab-in-data-science-EE-490-H).

<div align="center">
  <p>
  <img src="images/train.png" width="600" />
  </p>
  <p>
    <a href="">
      <img alt="First release" src="https://img.shields.io/badge/release-v1.0-brightgreen.svg" />
    </a>
  </p>

  <p>
    <strong>Roboust Route Planner</strong>
  </p>

</div>

## Team Members

* Serif Soner Serbest : serif.serbest@epfl.ch
* Jelena Banjac : jelena.banjac@epfl.ch
* Fatine Benhsain : fatine.benhsain@epfl.ch
* Asli Yorusun : asli.yorusun@epfl.ch

## Project Description

How many times have you ever followed religiously the itinerary given by your favourite journey planner until you missed a connection because of a delay or a connection time that was unrealistically short so your whole route was screwed and you had to figure out what to do next? Too many I would guess !

Our goal is to help you in these situations when you find yourself trapped because of a delay that could have been anticipated, and build a robust journey planner that takes into account the probabilities of delays happening depending on several criteria, using past data.

In our study, we started with importing and cleaning data, after that, we computed the probabilities of delays for different routes.Then, we built a connection graph to get access to the reachability of any station pairs, and created a timetable with information about the departure and arrival stations of the input and times for a given day. Finally, we calculate each possible route by using our timetable and connection graph, providing confidence levels with each route.

## Files

[SBB Data Analysis](SBB_Data_Analysis.ipynb) - contains the data analysis, cleaning and exploration 

[Distance Analysis](Distance_Analysis.ipynb) - contains the creation of the distance map of the stations

[Roboust Route Planner](Roboust_Route_Planner_FullDataset.ipynb) - the main notebook where we join the information found in two notebooks above and implement the route planner

[Roboust Route Planner for One Day](Roboust_Route_Planner_OneDay.ipynb) - the notebook similar to the above one, but it is only run on the one day

[Report](report.thml) - contains the profer results of the SBB dataset

## Presentation
[Final Presentation of the Project](handouts/final_presentation.pdf)

## Pro's and Con's of the Implementation

### Pro's
- Best routes are chosen based on the confidence and the shortest duration of the trip.
- User enters the inputs: "the start station" and "the end station" as well as "the departure time" one wishes to start a trip.
- We built the predictive model using the historical arrival/departure time data as well as other information from the given dataset.
- Validation is done on the small subset of the dataset (date 17.10.2017).
- Web visualization is implemented.

### Con's
- The planner does not mitigate the traveller's inconvenience if plan fails, we just don't propose that path if we think it will fail.
- Implementation is done based on the desired departure but it could also considered the arrival time to the final station, when user is asked to make a search.
- Web visualization could contain more information about the desired trip.

## References
[1] [The Open Data Platform Swiss Public Transport](https://opentransportdata.swiss) 

[2] [Stochastic Modelling of Train Delays and Delay Propagation in Stations](https://repository.tudelft.nl/islandora/object/uuid:caa72522-26b1-4088-afc0-59c6e5c346f6/datastream/OBJ/download)

[3] [Adi Botea, Stefano Braghin, "Contingent versus Deterministic Plans in Multi-Modal Journey Planning". ICAPS 2015: 268-272](https://dl.acm.org/citation.cfm?id=3038699)

[4] [Mathematical modeling and methods for rescheduling trains under disrupted operations](https://tel.archives-ouvertes.fr/tel-00453640/document)

[5] [Adi Botea, Stefano Braghin, "Contingent versus Deterministic Plans in Multi-Modal Journey Planning". ICAPS 2015: 268-272.](https://dl.acm.org/citation.cfm?id=3038699)

[6] [Adi Botea, Evdokia Nikolova, Michele Berlingerio, "Multi-Modal Journey Planning in the Presence of Uncertainty". ICAPS 2013.](https://www.aaai.org/ocs/index.php/ICAPS/ICAPS13/paper/view/6023)


