<!--
Slide delimiters are given by:
horizontal: ---
vertical: +++
-->

@Title[LEVERAGING CYVERSE FOR LARGE-SCALE SPATIAL ANALYSIS]

+++

### October 27, 2017
### Tyson Lee Swetnam
### CyVerse Science Informatician

+++

### Contact Info

tswetnam@cyverse.org

github: tyson-swetnam

---

### What is CyVerse?

+++

- Cyberinfrastructure
- Training
- Research

---

### What does 'large-scale spatial data' really mean in the era of _big data_?

+++

*Mb? Gb? Pb? Tb? Pb? Eb?*

+++

Computing power and storage capacity are advancing at exponential rate

+++?image=assets/imagery/Moores_Law_over_120_Years.png&size=auto

Moore's law over 120 years 
note: last several years are dominated by GPU
Source: Wikipedia

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

### DataStore

+++

- Graphical User Interface (GUI) via the Discovery Environment
- Multi-threaded file transfer (iRODS)
- Mountable as a local file directory via FUSE
- Extendable API for developers via _*Agave*_

---

### Atmosphere

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

### Jetstream

- Larger infrastructure
  - co-located at Texas Advanced Computing Center (TACC) and Indiana University (IU)
- instances up to 44 CPU, 120GB RAM  

+++?image=/assets/imagery/Jetstream_topology_diagram-crop.png&size=auto
---

### Data Commons

+++

Recieve a DOI

---

### Discovery Environment

+++

Develop tools

+++

![docker|200x100,20%](assets/imagery/horizontal_large.png)

