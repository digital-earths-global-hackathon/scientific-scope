---
header_menu: false
---

# Cross cutting activities

A number of ambitious cross cutting activities are also planned.  These usually introduce or explore technical capabilities that might be useful for addressing a range of scientific questions.  For this reason we are setting up cross-cutting activities whose participants may also want to join a science team. Some of the activities require early registration to ensure timely access to the tools.

Activities are given a unique identifier (uid) following the convention ‘hk25-uid’. Each activity will also have a lead and an associated repo on github with the same uid. The repo will serve as the primary basis for communication among participants in an activity.  Mattermost channels, markdown pads, and video-conference links may also serve as supplemental forms of communications, as indicated on by the README for each activity.

{{< toc >}}

---
### Joint EarthCARE analysis with ESA ([hk25-EarthCARE](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-EarthCARE))

[EarthCARE](https://earth.esa.int/eogateway/missions/earthcare) — **Earth** **C**loud, **A**erosol and **R**adiation **E**xplorer — is a joint satellite mission by the European Space Agency (ESA) and the Japan Aerospace Exploration Agency (JAXA). It is the sixth mission selected under ESA’s Earth Explorer Programme and was launched on 28 May 2024. By the time of the Hackathon, it will be approaching its first full year in orbit. EarthCARE offers a unique combination of four active and passive instruments for observing clouds, aerosols, and radiation.

In this team we will analyze both EarthCARE data and the participating models along virtual EarthCARE swaths, with an initial focus on tropical deep convection as analyzed by EarthCARE, aircraft, ships and ground stations during the [ORCESTRA campaign](http://orcestra-campaign.org/), i.e., over the Tropical Atlantic in the time-period between 10 August and 30 September, 2024. In addition, we are interested in extending this analysis framework to other phenomena such as tropical cyclones and subtropical stratocumulus, to evaluate how these systems are represented in both models and EarthCARE data.

**Note**:   We actively invite collaboration with science teams whose research aligns with EarthCARE’s mission and our initial objectives, and look forward to jointly integrating observational and modeling approaches.

**Coordination**: Saskia Brose (saskia.brose@esa.int)

#### Sketch of initial activities:
* extract model output along selected orbit frames
* post-process output using model simulators
* extract analagous EarthCARE frames and data from reanalyses
* perform composit analysis of various quantities
* applied research interests: tropical convection/ORCESTRA campaign, tropical cyclones, and stratocumulus clouds

---
### DestinE with the ClimateDT Consortium ([hk25-DestinE](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-DestinE))

[DestinE](https://destination-earth.eu) is an initiative of the European Commission which includes the operationalization of multi-decadal climate simulations using km-scale global models. Several multi-decadal scenario simulations have been performed with the [Climate Change Adaptation Digital Twin](https://destine.ecmwf.int/climate-change-adaptation-digital-twin-climate-dt/#What-is-the-Climate-DT) and are being integrated into the DestinE platform. Models underlying the Climate DT are ICON, IFS-NEMO, and [IFS-FESOM](https://github.com/digital-earths-global-hackathon/hk25/blob/main/content/models/ifs.md).

In this cross-cutting activity, we will exploit DestinE runs for new scientific insights via the [DestinE data platform (DESP)](https://platform.destine.eu). One of the goals is to expand the scope of the scientific analyses being performed by the HK25 science teams using the multi-decadal km-scale simulations of the Climate DT. The longer-term simulations may allow answering how a particular process identified by the other science teams might change under global warming. We can also address how much of a recent observed extreme event can be attributed to the already realised climate change, or how the exact event might have unfolded in an even warmer climate (using DestinE's so-called storyline simulations).

**Note**: Upgraded access to the DestinE data platform is required for eligible participants in the Hackathon. Those wishing to gain access need to register by 2 May (via https://platform.destine.eu/access-policy-upgrade/), and abide by the DestinE data policies.

**Coordination**: Tracy Kiszler (theresa.kiszler@csc.fi), **Co-coordination**: Thomas Rackow (thomas.rackow@ecmwf.int)

#### Sketch of initial activities:
* Gain access to the DestinE platform
* Identify analyses from science teams that could be executed on that platform and/or extended in scope using longer-term scenario simulations
* Perform analyses and compare to other Hackathon models

---
### AI Representations with NVIDIA ([hk25-NVIDIA](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-NVIDIA))

NVIDIA has been exploring the use of AI to improve the workflows associated with km-scale models.  For the Hackathon they have developed a prototype emulator allows massive compression of km-scale data, which then can provide a platofrm for accelerated analysis.

In this cross-cutting activity we will evaluate the capabilities and limitations of the emulator, and its ability to learn differences amond km-scale models. 

**Note** Participants are asked to register for the team as early as possible so the varied skill levels can be evalauted and approrpiate activities defined. 

**Coordination**: Karthik Kashinath (kkashinath@nvidia.com), Noah Brenowitz (nbrenowitz@nvidia.com)

#### Sketch of initial activities:
* extend AI training to additional models hosted on NERSC mode
* scale out the AI traning to other hackathon nodes and models
* test inference of model trained on an earlier version of ICON and ERA5

---
### Feature tracking with the grassroots ([hk25-Tracking](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-Tracking))

Global models simulating the atmosphere at km-scale with high resolution spatio-temporal output facilitate tracking of a variety of simulated features, similar to what is done using satellite data.  For example tracking can be used to identify and follow tropical storms, mesoscale convective systems, atmospheric rivers, and so on.  For the hackathon a number of tracking tools are being adapted to work on the HEALPix output of the models.  Trackers will be introduced to related science teams by members of this cross-cutting activity.

**Coordination**: Zhe Feng (zhe.feng@pnnl.gov)

#### Sketch of initial activities
- Gain familiarity with one or more trackers
- Develop and extend their capabilities
- Apply to output to answer questions posed by science teams.

---

### Data interoperability ([hk25-EOPF_DGGS](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-EOPF_DGGS))

For software-engineeering oriented peeps interested in ESA's Earth Observation Processor Framework (EOPF).  This activity will explore how to help scientists and engineers to seamlessly link HEALPix based workflows to with diverse geospatial datasets (in-situ, Satelite, model output). Our efforts focus on simplifying manipulation and analysis workflows for Discrete Global Grid Systems (DGGS), particularly HEALPix-based data, with a strong emphasis on interoperability and scalability.

**Coordination**: Tina Odaka (tina.odaka@ifremer.fr)

#### Sketch of initial activities
- Zarr v3 on HEALPix
- Multiresolution data access
- Interoperability and community standardization

---

### 21st Century Weather ([hk25-AusNode](https://github.com/digital-earths-global-hackathon/hk25-teams/tree/main/hk25-AusNode))

As part of the [ARC Centre of Excellence for the Weather of the 21st Century](https://21centuryweather.org.au) the Australian node is supporting ca 10 cross-cutting research projects. These structured projects explore how km-scale models can advance understanding of weather and climate across scales.  The goal is to analyze global simulations through a local lens, using existing tools, methodologies, and datasets. 

**Note:** We wil look at some topics addressed by specific science tehams, and others that are orthogonal, through a more holistic lense.  Hence, this is structured as a cross-cutting activity to encourage collaboration with science teams working on related topics.

**Coordination:** Melissa Hart (melissa.hart@utas.edu.au)

#### Sketch of initial activities:

* Work on healpix examples to read a plot data.
* Identify data and variables to analyze according to the topic of interest. 
* Collaborate and discuss research plan
