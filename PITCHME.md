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

#### Roadmap

- Cyverse
- Data Science
  - Research Objects
 - Data Scientist Workbenches
  - RStudio
  - Project Jupyter
- Containers
  - Docker
  - Singularity
- GIS
- Live Demo

---

### What is [CyVerse](http://cyverse.org)? 
![cyverse](assets/imagery/cyverse_logo_150px.png)

+++

<span style="font-weight: bold; color:#3685E3">Vision:</span> Transforming science through data driven discovery.</span>

+++

<span style="font-weight: bold; color: #3685E3">Mission:</span> To design, deploy, and expand a national cyberinfrastructure for life sciences research, and to train scientists in its use.</span>

+++

- Cyberinfrastructure
- Research
- Training

+++

CyVerse is <span style="color: #118224">_you_</span> and <span style="color: #3685E3">_me_</span>.

CyVerse is enabled by <span style="font-weight: bold; color: #c7232e">_people_</span> 

It doesn't exist without users innovating new and important science within an ecosystem of interoperability.  

+++

When <span style="color: #118224">_you_</span> use CyVerse, develop new tools, workflows, and datasets they influence the science CyVerse embodies

---

### What does <span style="font-weight: bold; color: #118224">large-scale</span> really mean in the era of <span style="color: #3685E3">_big data_</span>?

+++

<span style="font-size: 200%; color:#000000">Data are always increasing in volume</span>

+++

<span style="font-weight: bold; font-size: 200%; color:#FF0000">90% </span><span style="font-size: 200%; color: #000000"> of all data in human history were created in [last 24 months](https://blog.microfocus.com/how-much-data-is-created-on-the-internet-each-day/)</span>

+++

So, what qualifies as big data?

@[0](<span style="font-size: 250%; font-weight: bold; color:#3685E3">Megabyte 10<sup><span style="font-size: 75%; font-weight: bold; color:#3685E3">6</span></sup>?</span>)
@[1](<span style="font-size: 250%; font-weight: bold; color:#0000FF">Gigabyte 10<sup><span style="font-size: 75%; font-weight: bold; color:#0000FF">9</span></sup>?</span>)
@[2](<span style="font-size: 250%; font-weight: bold; color:#0000A0">Terabyte 10<sup><span style="font-size: 75%; font-weight: bold; color:#0000A0">12</span></sup>?</span>)
@[3](<span style="font-size: 250%; font-weight: bold; color:#800080">Petabyte 10<sup><span style="font-size: 75%; font-weight: bold; color:#800080">15</span></sup>?</span>)
@[4](<span style="font-size: 250%; font-weight: bold; color:#00FF00">Exabyte 10<sup><span style="font-size: 75%; font-weight: bold; color:#00FF00">18</span></sup>?</span>)
@[5](<span style="font-size: 300%; font-weight: bold; color:#FF0000">data are just data</span>)

+++

Computing power and storage capacity are advancing at exponential rate

+++?image=assets/imagery/Moores_Law_over_120_Years.png&size=contain

<span style="color:#3685E3"> last 5 are all GPUs </span> 

+++

There are many types of spatial data user...

In this talk I'll cover a few skill levels

+++

<span style="font-weight: bold; font-size: 150%; color:#FF0000">New users</span>
- Interest in Graphic User Interfaces (GUI) & Integrated Development Environment (IDE) tools
  - Maybe just learning spatial analyses for the first time

+++

<span style="font-weight: bold; font-size: 150%; color:#0000A0">Experienced users</span>
- Interest in scaling workflows beyond the laptop / desktop on to HPC and Cloud
- Need to move significant amounts of data around networks

+++


<span style="font-weight: bold; font-size: 150%; color:#800080">Power users</span>
- Interest in integrating global and national datasets across HPC environments for massively parallel computing

---

### The Research Object

+++

<span style="font-weight: bold; font-size: 100%; color:#000000">_Okay, what is a Research Object?_</span>

@[1](<span style="font-size: 125%; font-weight: bold; color:#3685E3">broadly, it is a method for identification, aggregation, and exchange of scholarly information</span>)

+++

The Research Object needs:
- Digital identity: DOI, [ORCID](http://orcid.org/)
- Data aggregation: discoverable, reusable
- Annotation & Provenance: METADATA!

+++

CyVerse covers the entire life cycle of the Research Object:

- Create
- Analyze
- Annotate
- Publish
- Archive

---

### Data Science Workbenches

+++

Data scientists need a place to work...

+++

### data + compute + algorithm

+++

A workbench allows you to:
- work in preferred environment, languages, and libraries
- computational notebooks written in Python, R, Spark, etc...

+++

<img src="assets/imagery/Python_logo_and_wordmark.svg.png" width="300"> <img src="http://jupyter.org/assets/hublogo.svg" width="205">

+++

<img src="assets/imagery/Rlogonew.png" width="200"> 

---

### DataStore 
![ds](assets/imagery/DataStore_blue.png)

+++

- GUI via the [Discovery Environment](https://de.cyverse.org)
- Multi-threaded file transfer ([iRODS](https://irods.org/))
- Mountable as a local file directory via FUSE
- Extendable API for developers via _*Agave*_

+++

- All new users receive 100 GB 
- Increase to 10 TB via portal request.
- \>10 TB available upon written request + executive review.

+++

Despite hosting several petabytes of data storage, CyVerse *is not* a canonical geospatial data repository, e.g. [Earth on AWS S3](https://aws.amazon.com/earth/).

+++

CyVerse *is* a place you can bring large quantities of data and do analysis on, generate more result data, and hold for a short period (e.g. 6 months to 1 year), before moving those data to a canonical or privately hosted repository.

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
- emulated web shell and desktop via [Apache _Guacamole_](https://guacamole.incubator.apache.org/)  

+++

Atmosphere proved to be very popular...

+++

...so they built

<img src="assets/imagery/Jetstream_logo_hi_res_cropped.jpg" width="500">

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

[DOI](https://www.doi.org/) is a Digital Object Identifier 

[ARK](https://en.wikipedia.org/wiki/Archival_Resource_Key) is an Archival Resource Key.

Both identifiers are issued by CyVerse through the California Digital Library's [EZID service](http://ezid.cdlib.org/).

+++

- Publish your notebooks 
- datasets
 - Recieve a DOI
 - Searchable

---

### [Discovery Environment](https://de.cyverse.org)
![de](assets/imagery/Discovery_blue.png)

+++

Develop new tools using Docker
<img src="assets/imagery/horizontal_large.png" width="200">

---

### GIS

+++

The majority of data (59%) include a spatial component or are themselves inherently spatial.

+++

a bit of history...

+++

Environmental Systems Research Institute (ESRI), est. 1969

<img src="https://upload.wikimedia.org/wikipedia/en/thumb/6/6e/Esri_logo.svg/1280px-Esri_logo.svg.png" width="400"> 

+++

ESRI has come to dominate the GIS marketplace and is used widely by gov't and academia.
+++

Geographic Resources Analysis Support System (GRASS), est. 1982

<img src="http://grassmac.wdfiles.com/local--files/start/startup_banner.png" width="500">

+++

Which GIS platform is best for CyVerse?

@[1](<span style="font-size: 150%; font-weight: bold; color:#3685E3">They are both great</span>)

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

<img src="http://singularity.lbl.gov/images/logo/logo.svg" width="250">

Singularity Hub

---

### using Licensed software with CyVerse

+++

ArcGIS is the most widely used GIS software in the USA, ~40% of all users.

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

@title[Docker RStudio]

### <span style="color: #e49436">Docker + RStudio</span>
<br>

```shell
$ ezd
$ sudo usermod -aG docker $USER
$ exit
$ docker pull rocker/geospatial
$ docker run -d -p 8787:8787 rocker/geospatial

Done!

```

@[1](install Docker)
@[2](change `sudo` privileges)
@[3](exit and restart terminal window)
@[4](pull the Rocker/Geospatial Rstudio-Server from DockerHub)
@[5](Run the Container on port `:8787`)
@[7](Open the IP and port number in a new browser window)

---

#### Where do I get started, if I don't know where to start?

[The Carpentries](https://software-carpentry.org/)
