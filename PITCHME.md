<!--
Slide delimiters are given by:
horizontal: ---
vertical: +++
-->

## LEVERAGING CYVERSE FOR LARGE-SCALE SPATIAL ANALYSIS

+++

#### October 27, 2017
#### Tyson Lee Swetnam
#### CyVerse Science Informatician

+++

### Contact Info

tswetnam@cyverse.org

github: tyson-swetnam

twitter: tswetnam

---

### What is CyVerse? 
![cyverse](assets/imagery/cyverse_logo_150px.png, http://cyverse.org)

+++

#### Vision: Transforming science through data driven discovery

+++

#### Mission: to design, deploy, and expand a national cyberinfrastructure for life sciences research, and to train scientists in its use.

+++

- Cyberinfrastructure
- Training
- Research

+++

---

### What does 'large-scale spatial data' really mean in the era of _big data_?

+++

*Mb? Gb? Tb? Pb? Eb?*

+++

Computing power and storage capacity are advancing at exponential rate

+++?image=assets/imagery/Moores_Law_over_120_Years.png&size=auto

Moore's law over last 120 years

+++

There are many levels of spatial data user...

- In this talk I'll cover a few of these depending upon need

+++

* New users
  * Graphic User Interfaces (GUI) & Integrated Development Environment (IDE) tools
  * learning spatial analyses

+++

* Experienced users
  * scaling workflows beyond the laptop / desktop on to HPC

+++

* Power users
  * integrating global and national datasets across HPC environments

---

### The Research Object

+++

A method for identification, aggregation, and exchange of scholarly information

+++

- Digital identity: DOI, ORCID
- Data aggregation: discoverable, reusable
- Annotation & Provenance: METADATA!

+++

CyVerse covers the entire life cycle of the Research Object:

- Creation
- Analysis
- Publishing
- Archival

---

### Data Science Workbenches

+++

Data scientists need a place to work...

+++

#### data + compute + algorithm

+++

- work in preferred environment, languages, and libraries
- computational notebooks written in Python, R, Spark, etc...

+++

- Jupyter Lab / Hub
- R / RStudio-Server

---

### DataStore 
![ds](assets/imagery/DataStore_blue.png)

+++

- Graphical User Interface (GUI) via the Discovery Environment
- Multi-threaded file transfer (iRODS)
- Mountable as a local file directory via FUSE
- Extendable API for developers via _*Agave*_

+++

- All new users receive 100GB 
- Increase to 10TB via portal request.
- +10TB available upon written request + executive review.

---

### <a href="Atmosphere" target="_blank">https://cyverse.org/atmosphere</a>

![atmo](assets/imagery/Atmosphere_Blue.png)
<img src="assets/imagery/Atmosphere_Blue.png" width="150">https://atmo.cyverse.org<a>


+++

- Linux environment (Centos, Ubuntu)
- On demand
- Collaborate together online
- Publically host custom images

+++

- Multiple 'flavors' of instance size
  - 1 CPU, 4GB RAM, 30GB Disk
  ...
  - 16 CPU, 128GB RAM, 1400GB Disk
- Attach (and detach) additional TB size volumes to an instance   
- emulated web shell and desktop via Apache _Guacamole_  

+++

Atmosphere proved to be very popular...

+++

### <a href="Jetstream" target="_blank">https://use.jetstream-cloud.org</a>


- Larger infrastructure
  - co-located at Texas Advanced Computing Center (TACC) and Indiana University (IU)
- instances up to 44 CPU, 120GB RAM  

+++?image=/assets/imagery/Jetstream_topology_diagram-crop.png&size=auto

---

### Data Commons 
<img src="assets/imagery/DataCommons_Blue.png" width="150">https://datacommons.cyverse.org<a>

+++

Recieve a DOI

---

### Discovery Environment 
![de](assets/imagery/Discovery_blue.png)


+++

Develop tools

+++

![docker|200x100,20%](assets/imagery/horizontal_large.png)

---

### Geographic Information Systems

+++

The majority of data (59%) include a spatial component or are themselves inherently spatial.

+++

But first, a bit of history...

+++

Environmental Systems Research Institute (ESRI), est. 1969

Geographic Resources Analysis Support System (GRASS), est. 1982

+++



+++

---

#### Where do I get started, if I don't know where to start?

The Carpentries


