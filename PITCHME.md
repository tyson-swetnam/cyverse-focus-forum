<!--
Slide delimiters are given by:
horizontal: ---
vertical: +++
-->

## Leveraging CyVerse for large scale spatial analysis
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

### What is [CyVerse](http://cyverse.org)? 
![cyverse](assets/imagery/cyverse_logo_150px.png)

+++

<span style="font-family: Helvetica Neue; font-weight: bold; color:#3685E3">Vision:</span> Transforming science through data driven discovery.</span>

+++

<span style="font-family: Helvetica Neue; font-weight: bold; color: #3685E3">Mission:</span> To design, deploy, and expand a national cyberinfrastructure for life sciences research, and to train scientists in its use.</span>

+++

- Cyberinfrastructure
- Research
- Training

+++

CyVerse is <span style="font-family: Helvetica Neue; color: #118224">_you_</span> and <span style="font-family: Helvetica Neue; color: #3685E3">_me_</span>.

CyVerse is what <span style="font-family: Helvetica Neue; font-weight: bold; color: #c7232e">_people_</span> make it.

It doesn't exist without users driving new and important science. 

+++

When <span style="font-family: Helvetica Neue; color: #118224">_you_</span> use CyVerse, develop new tools, workflows, and datasets they influence the science CyVerse embodies

---

### What does <span style="font-family: Helvetica Neue; font-weight: bold; color: #118224">large-scale</span> really mean in the era of <span style="font-family: Helvetica Neue; color: #3685E3">_big data_</span>?

+++

@[1](<span style="font-family: Helvetica Neue; font-size: 250%; color:#3685E3">Data are always increasing in volume</span>)
@[2](<span style="font-family: Helvetica Neue; font-weight: bold; font-size: 250%; color:#FF0000"</span>90%<span style="font-family: Helvetica Neue; font-size: 250%"> of all data in human history were created in [last 24 months](https://blog.microfocus.com/how-much-data-is-created-on-the-internet-each-day/)</span>)

+++

So, what qualifies as big data?

@[0](<span style="font-family: Helvetica Neue; font-size: 250%; font-weight: bold; color:#3685E3">Mb?</span>)
@[1](<span style="font-family: Helvetica Neue; font-size: 250%; font-weight: bold; color:#0000FF">Gb?</span>)
@[2](<span style="font-family: Helvetica Neue; font-size: 250%; font-weight: bold; color:#0000A0">Tb?</span>)
@[3](<span style="font-family: Helvetica Neue; font-size: 250%; font-weight: bold; color:#800080">Pb?</span>)
@[4](<span style="font-family: Helvetica Neue; font-size: 250%; font-weight: bold; color:#00FF00">Eb?</span>)
@[5](<span style="font-family: Helvetica Neue; font-size: 300%; font-weight: bold; color:#FF0000">data are just data</span>)

+++

Computing power and storage capacity are advancing at exponential rate

+++?image=assets/imagery/Moores_Law_over_120_Years.png&size=contain

<span style="font-family: Helvetica Neue; color:#3685E3"> last 5 are all GPUs </span> 

+++

There are many types of spatial data user...

- In this talk I'll cover a few skill levels

+++

New users
- Interest in Graphic User Interfaces (GUI) & Integrated Development Environment (IDE) tools
  - Maybe just learning spatial analyses for the first time

+++

Experienced users
- Interest in scaling workflows beyond the laptop / desktop on to HPC and Cloud
- Need to move significant amounts of data around networks

+++

Power users
- Interest in integrating global and national datasets across HPC environments for massively parallel computing


---

### The Research Object

+++

_What is a Research Object?_

broadly, it is a method for identification, aggregation, and exchange of scholarly information

+++

- Digital identity: DOI, ORCID
- Data aggregation: discoverable, reusable
- Annotation & Provenance: METADATA!

+++

CyVerse covers the entire life cycle of the Research Object:

- Create
- Analyze
- Publish
- Archive

---

### Data Science Workbenches

+++

Data scientists need a place to work...

+++

#### data + compute + algorithm

+++

A workbench allows you to:
- work in preferred environment, languages, and libraries
- computational notebooks written in Python, R, Spark, etc...

+++

<img src="assets/imagery/Python_logo_and_wordmark.svg.png" width="300"> <img src="http://jupyter.org/assets/hublogo.svg" width="200">

+++

<img src="assets/imagery/Rlogonew.png" width="200"> 

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

### [Atmosphere](https://cyverse.org/atmosphere)
![atmo](assets/imagery/Atmosphere_Blue.png)

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

...so they built

### [Jetstream](https://use.jetstream-cloud.org)

<img src="assets/imagery/Jetstream_logo_hi_res_cropped.jpg" width="200">

+++?image=/assets/imagery/Jetstream_topology_diagram-crop.png&size=auto

+++

- co-located at Texas Advanced Computing Center (TACC) and Indiana University (IU)
- launch dozens of instances 
- sizes from 1 core 2GB RAM, up to 44 CPU, 120GB RAM
- Request necessary storage size

---

### [Data Commons](https://dc.cyverse.org)
<img src="assets/imagery/DataCommons_Blue.png" width="150">

+++

- Publish your notebooks 
- datasets
 - Recieve a DOI
 - Searchable

---

### [Discovery Environment](https://de.cyverse.org)
![de](assets/imagery/Discovery_blue.png)

+++

Develop tools

+++

Use Docker <img src="assets/imagery/horizontal_large.png" width 100>


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

---

#### Setting up Atmosphere instances as Data Science Workbenches

---

@title[EZ Install]

### <span style="color: #e49436">EZ Install</span>
<br>

```shell
$ ezs
$ ezd
$ ezj -R -3

Done!
```

@[1](Install latest version of Singularity.)
@[2](Install latest version of Docker)
@[3](Install Anaconda and Jupyter Notebooks w/ Python3 and R Kernel)
@[5](Start doing work!)

---

## [Bisque](https://bisque.cyverse.org)
![bisque](assets/imagery/bisQue_Blue.png)

+++

BisQue is an image analysis platform 

+++

- segmentation
- annotation
- metadata tagging

+++

#### Coming soon

- Machine Learning
- Structure from Motion

---

### Containers

Docker

Docker Hub

+++

Singularity

<img src="http://singularity.lbl.gov/images/logo/logo.svg" width="150">

Singularity Hub

---

### using Licensed software with CyVerse

+++

ArcGIS is the most widely used GIS software in the USA

+++

[ArcGIS Portal 10.5](http://server.arcgis.com/en/portal/latest/install/linux/welcome-to-the-portal-for-arcgis-installation-guide.htm) runs in Linux

- install on Atmosphere / Jetstream instances using Chef
 - must use license keys issued via your institution
- Integrated with Docker and [Project Jupyter](https://hub.docker.com/r/esridocker/arcgis-api-python-notebook/) 
 - run notebooks with ArcPy and the ArcGIS API to do big data applications 

--- 

@title[ArcGIS Jupyter Notebook with Docker]

### <span style="color: #e49436">Docker + Jupyter + ArcPy</span>
<br>

```shell
$ ezd
$ usermod -aG docker $USER
$ docker pull esridocker/arcgis-api-python-notebook

Done!

```

@[1](Install latest version of Docker using `EZ` installation)
@[2](Add yourself to the Docker group on your VM so you can run without `sudo`)
@[3](Pull the ArcGIS Jupyter Docker Container)
@[4](The Jupyter notebook should now be running on the localhost - change `localhost` out for the VM's IP address)
@[5](Start doing work!)

---

<img src="assets/imagery/RStudio-Logo-Blue-Gradient.png" width="500">

+++

@title[RStudio-Server]

### <span style="color: #e49436">R + RStudio-Server</span>
<br>

```shell
$ git clone https://github.com/cyverse-gis/focus-forum.git
$ cd focus-forum/atmo
$ . install_rstudio.sh
$ rstudio-server status
Done!

```

@[1](Clone this Github Repository to the Virtual Machine)
@[2](change directories to access the shell installation scripts)
@[3](Run the script - this will take a while)
@[4](The RStudio-Server should now be running, check to be sure)
@[5](Start doing work!)

