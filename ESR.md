# Abstract 
BOSS is a complementary mission for NASA's OSIRIS-REx.

OSIRIS-REx has collected significant amounts of data on Bennu, thus making the goal of finding further relevant information, while keeping a focus on creativity and innovation, a serious challenge. 

As a consequence of rigorous planning and methodical identification and arrangement of stakeholders, a general mission framework has been layed out, with its high-level requirements.

After filling out the STM and the TTM, more detailed mission requirements have been set out and an adequate payload has been carefully selected.

A feasibility study has been carried on, marking off a definitive mission architecture.
The mission has been globally divided into two distinct stages: 

+ *In orbit analysis* 
+ *In situ analysis*

During the first stage, a meticulous selection of sensors will collect specific datasets, via hyperspectral analysis, infrared imagery, LIDAR cloudpoints, etc, while AI algorithms handle a fully autonomous GNC system. 

During the second stage, the satellite will land on Bennu's surface, collecting further datasets, with particular focus on its local geological and chemical composition. 

All communications with Earth are ricocheted off OSIRIS-REx. 

# Scope and purpose
This document is a summary of all the steps taken by the project team, in order to design and manage the preliminary levels of a space mission, aimed to the observation of Bennu.

It is the final deliverable of this case study and will be used to assess the activities carried out by the team.

The document includes the following content:

+ Identification of stakeholders and mission needs
+ Delineation of high-level requirements and constraints
+ Delineation of the ConOps and mission architecture
+ Delineation of trajectories and kinematic relations, calculated by *Systems Tool Kit*
+ Delineation of individual subsystems and their budget
+ Jobs management and tasks distribution
+ Risk and cost analysis

# Context and objectives of the mission
Asteroids are small irregularly shaped celestial bodies, similar in composition to rocky planets. 

They're the vast majority of celestial bodies in the Solar System and they're classified by their spectral bands, which identify average surface chemical composition. 

Asteroids are among the most studied and yet fascinatingly mysterious celestial bodies. 

Further discoveries in this field of astronomy are crucial for unveiling unknown pieces in the history of the Solar System. 

Asteroids are in fact thought to have originated in protoplanetary disks, thus retaining information (like chemical composition) about the genesis of a star and its orbiting planets. 

In addition to this, celestial bodies such as meteors and asteroids might have played a role in the origin of life on Earth (and possibly other planets), as a carrier of genetic material from different parts of the universe, according to the *panspermia* hypothesis.

*Near Earth Asteroids* are remarkably interesting, as they can potentially collide with Earth and improving techniques for studying their trajectory might be key in predicting a catastrophic impact. 

Apollo asteroids are a subset of Earth-crossing NEAs, characterized by an orbital semi-major axis greater than that of the Earth, but perihelion distances less than the Earth's aphelion distance. 

Discovered in 1999 by the *LINEAR* project, a predominantly carbonaceous asteroid, named Bennu, was identified and classified with the following features: 

+ Aphelion = 1.36 AU
+ Perielion = 0.897 AU
+ Semi-major axis = 1.12 AU
+ Orbital inclination = 6.0349°
+ Orbital period = 1.1955 yr
+ Mean diameter = 490 m

There are eight potential collisions with Earth, between 2169 and 2199, with an average 0.07% likelyhood of impact.

This value is highly fluctuating, as it depends on unforeseeable perturbations the asteroids' motion is subjected to.

Further progress in space research should (in theory) advance at a fast enough pace that will prevent a fatal collision with planet Earth. 

Last but not least, the potential use of asteroids as mining commodities is heavily discussed and portrayed as a way to reduce the disruptive extraction of limited materials on Earth (Elon Musk figlio di puttana devi morire), although there are still too many challenges and hassles to see *space mining* as a near future possibility.

## Stakeholders' needs analysis
Several potential stakeholders have been identified, then mindfully selected and classified by their plausible interest and the power they might exert to manipulate the mission. 

The stakeholders have been subdivided into four tiers:
+ *Latents*: very low or negligible interest, but potentially highly influential 
+ *Apathetics*: very low or negligible interest, as well as very low or negligible power over the mission
+ *Defenders*: very high interest, but not particularly influential
+ *Promoters*: highest tier of both interest and power

Based on this tiering system, the most important stakeholders are:

+ *ESA*
+ *Public investors*
+ *Scientific community*
+ *Private investors*

ESA is the most influential entity, being the main sponsor and financer of the mission. 

The agency, being funded by the European Union, benefits from data collection, but needs to prioritize its image and public perception as well, thus exerting power in order to make the mission's success a top priority.

Public investors hold a similar interest in their public perception, but overall have far less influence over the mission. 

On the other hand, private investors might need to value their image to a certain degree, but generally receive far less mediatic pressure and their influence highly depends on overall financial power. (elon musk merda assoluta). 

The primary scientific community, being intrinsecally more decentralized, is in a less economically biased position and holds a more genuine interest towards collected data and scientific progress. However, its overall influence is not as strong as that of large corporations or extremely influential public institutions like ESA. 

### QFD

The *Quality Function Development* is comprised of two parts. 

The upper table is a color-coded binary comparison of Values vs Values (green -> matching, red-> conflict) and helps identify common concerns or conflicts of interest.

The lower table correlates values with stakeholders, through a cumulative scoring system, ranging from 1 to 10. 

Total scores: 
+ Primary values (scores from 300 to 350) 
    + Knowledge & Technological return (350) 
    + Safety & Robustness (336) 
    + Test & Validation (335) 
    + Data Quality & Elaboration (313) 
+ Secondary values (scores from 200 to 300) 
    + Reduction of weight & dimensions (274) 
    + System reliability (254) 
    + Research & Development (246) 
    + Operative costs (sustainment of mission) (228) 
    + Mission background costs (research & development) (222) 

## Mission objectives

Following the meticulous stakeholders analysis, the team came up with a mission statement: 

“*To develop an independent mission, complementary to Osiris-Rex, to collect, elaborate and distribute data on Bennu’s surroundings and its morphology, to let the scientific community study its trajectory and prevent potential collisions, and to further expand our knowledge on the origin of the Solar System. 
To land on Bennu in order to collect further data in situ, using technologies for small satellites, in order to showcase their reliability in deep space exploration mission.*” 

The following objectives can be derived from this mission statement: 

+ Primary objectives 
    + To map the global properties of Bennu. 
    + To characterize the proximity of the asteroid. 
    + To showcase the usage of smallsats technologies in deepspace. 
+ Goal of opportunity 
    + To conduct an *in situ* analysis of chemical and physical properties.

The primary objectives, unlike the goal of opportunity, are essential tasks that guarantee a succesful mission.

## High level requirements

High level requirements have been layed out, as a synthesis of all the steps taken to this point, including the mission goals and the top priority objectives derived from the *STM* (Science Traceability Matrix) and the *TTM* (Technology Traceability Matrix).

All the requirements can be found in the statement of work.

# Mission and system design

## AHP analysis

An AHP analysis has been conducted (reference all'annex dell'AHP), in order to make adequate decisions by objective comparison of ad-hoc figures of merit. 

Using this method, three different mission architectures have been analyzed. 

Architecture complexity, lifecycle costs, data reliability and number of subsystems are the figure of merits taken into account. 

A scoring system, carried out through a figure of merit prioritization matrix, allowed for the identification of the most suitable option.

Further details are discussed in the (Mission architecture) section.

## Concept of operations

The mission will begin after detachment from OSIRIS-REx. 
Shortly before the separation, BOSS will start a commissioning phase in its stowed configuration: the power supply turns on the onboard computer and other electronics, while executing system integrity checks of ComSys, GNC, TCS, etc, and collecting housekeeping data.

Once the AOCS and the propulsion system are active and verified to be properly functioning, this phase will be finalized with a calibration of the GNC system and with data validation. 

Communications will be relayed by OSIRIS-REx to Earth.

Once the satellite is on a stable orbit, its payload will begin scanning Bennu's surface and carry on with an interdisciplinary analysis for three months. 

Assuming that OSIRIS-REx will be able to locate an optimal landing site, the satellite will start de-orbiting and will land on the asteroid, taking advantage of its low gravitational pull for a gentle landing. 

Provided that the landing operation is succesful, the satellite will activate a CASSE and an X-ray diffractometer, while translating on Bennu's surface via an autonomous mobility mechanism. 

The total duration of the mission is expected to last for six months, based on estimates of its average battery life. 

## Functional analysis 

The mission has been divided into two main stages:

+ *In orbit analysis*
  + System integrity check
  + Detachment
  + Orbital stabilization
  + Analysis 
+ *In situ analysis*

All the phases have been further subdivided into lower level subtasks, each of them associated with an appropriate system.

The subdivision is illustrated by a functional tree. 

Furthermore, the N2 diagram highlights the interaction of systems (structural, mechanical, electrical, functional, thermal, etc) and simplifies the budgets calculation. 

## Mission architecture

Based on the previous examinations and results, three main mission architectures have been thoroughly discussed.

### Satellite constellation

This configuration allows for a great level of redundancy and can simultaneously scan larger surface areas, however the overall system complexity and storage requirements are exponentially increased, thus making it unfeasible for this scenario.

### Lander and orbiter

The idea behind this architecture is that of using two specialized elements for the main stages of the mission. 
The main disadvantage of this approach is excessive cost, in addition to the unsatisfactory payload redundancy.

### Single orbiting-landing unit

The single unit performs all the tasks, in different phases, while providing significant advantages, like a lower level of complexity, higher onboard capacity and lower mass. 

The main drawback, compared to an architecture with multiple specialized units, is the longer time span required to collect a similar amount of data.

What emerged from the AHP analysis (reference) is that, despite having some criticalities and engineering challenges, the single unit solution is the best suited for the mission.

One of its key pros is the ability to move on the asteroid's surface (similarly to JAXA's Hayabusa) and closely analyze different areas of Bennu, increasing chances of relevant discoveries.

## Mission analysis
### In orbit

**Introduction to Mission Analysis** 

The following section presents a description of the orbits selected for the BOSS Mission, the evaluation of the ΔV budget needed and the main maneuvers executed during the orbital phase. The proposed mission has been set up in order to accomplish the mission requirements MIS-xx1 and MIS-xx2 (defined to manage the global orbital period). 

The in-orbit operative phase is made of three different types of orbits. All the orbits described are retrograde, sub-polar and with a high value of Beta Angle and they will be classified according to their height in A-orbit, B-orbit and C-orbit. 

Using the STK software, (with a focus on the STK Astragator tool), a study of orbital propagation has been carried out, taking into account: 

+ Bennu’s gravitational parameters (zonal harmonic terms up to grade four: J2, J3, J4); 

+ The effect of Solar radiation pressure, based on a spherical model; 

+ The perturbation of gravitational forces exerted by a third body, like the Sun, Jupiter, or other planet in the proximity of Bennu, like the Earth, Venus and Mars. 

All the previous contributions have been added to the propagator ‘Bennu Perturbated’ in order to execute the analysis. 

Moreover, according to the type of propulsion, the maneuvers have been assumed to be impulsive. 

**Deployment and Orbit insertion**  

According to the timetable defined in the SoW, the mission will start on 11 Dec 2023 04:00:00 UTC, after the separation of BOSS from the mothercraft or more specifically when OSIRIS-Rex is going to be, for the first time, 16 km away from Bennu. 

The release maneuver will be performed by a dispenser (exerting a force of 1 N, in accordance with the deployer standards ADx). 

The separation is implemented through a ‘follow maneuver’ of the mothercraft, convoyed by an ‘in-track maneuver’. 

The last maneuver will last for two days, in order to complete the commissioning phase (detumbling, solar arrays deployment, check and calibration of payloads). 

Once BOSS reaches a sufficient distance from OSIRIS-Rex, the first propulsive maneuver will take place, immediately followed by the insertion maneuver. 

This is the beginning of the operative phase. 

**Operative Orbits, orbital maneuvers & station-keeping**

The operative orbits have been classified based on the distance from Bennu’s mean surface: 

+ *A orbit*: number of orbits 3.5 at a height of 2.5 km

+ *B orbit*: number of orbit 25.5 at a height of 1 km

+ *C orbit*: number of orbit 39 at a height of 0.5 km

From Dec 13 2023 (16:30:00 UTC) through  Jan 3 2024 (09:00:00 UTC), the spacecraft will follow the A orbit trajectory. Once the operative height is reached (after a circularization maneuver), the first type of maneuvers will begin. 

These orbits are highly influenced by the perturbative effects of the other bodies. 

Their duration has been chosen in order to minimize the time needed to globally map the surface of the asteroid (with particular focus to the time needed by the Chameleon imager and the LIDAR). 

In spite of these major issues, this kind of orbit offers way too many benefits in terms of scientific measurements and accomplishment of science goals (e.g. mapping the residual magnetic field). 

From Jan 5 2024 (10:00:00 UTC) through Feb 13 2024 00:00:00 UTC, the spacecraft will follow the B orbit trajectory. 

After a perigee reduction maneuver, the B orbit insertion maneuver will take place. 

Thanks to B orbit’s stability (negligible perturbative effects) all the measurements are performed more accurately, making it easier to handle optics and in general pointing requirements.   

From Feb 13 2024 (13:00:00 UTC) through Mar 13 2024 (14:41:00 UTC), the spacecraft will follow the C orbit trajectory. 

Much like the previous maneuvers, this kind of orbit will be reached through a maneuver of perigee reduction. 

Based on the scientific measurements performed and landing site selection, this phase will last longer than the previous ones. 

As just mentioned, data collected by onboard instruments and those transmitted by OSIRIS-Rex will be analyzed in order to define the landing site. 

This phase will be followed by the landing maneuver.  

All the operative phases are characterized by station-keeping maneuvers, in order to manage, in a pre-defined range, the evolution of the orbital parameters. 

The range needed is defined in accordance to the payloads requirements and the optimization of the ΔV. 

The main maneuvers focus on perigee and apogee adjustment. 

In order to supply sufficient powers during the in orbit stage, an additional station-keeping maneuver will be performed, with the goal of increasing the Beta Angle (angle between the satellite's orbital plane and the sun vector).

**Orbital Scientific Measurements**

Orbital features, including -but not limited to- duration, have been carefully selected by taking payload requirements into account.

Once the orbits have been chosen, further studies have been conducted, focusing on orbital stability, maneuver complexity, data coverage and redundancy.

A Beta angle range has been defined, in order to guarantee appropriate sizing of solar panels and, consequently, of the entire power supply chain. 

Proper sizing of solar panels is key, as the entire in orbit stage has been designed with particular attention to avoiding the usage of batteries (which will be essential during the in situ stage), in order to maximize overall mission longevity. 

The meticolous choice of this essential parameter, among the various considerations, has also been influenced by the necessity to carry out infrared analysis, both in daylight and in eclipse. 

In addition to this, a subpolar inclination angle will satisfy the global coverage requirement and optimize pointing accuracy, allowing for the mapping of residual magnetic field over polar regions, as an added benefit. 

Moreover, this inclination will completely avoid eclipse periods, thus avoiding battery utilization (as previously mentioned) and simplifying overall thermal control of the satellite. 

Additional benefits include simplified landing operations (lower total number of maneuvers, due to less strict limits on landing site latitude and longitude), which is a key advantage, given that the site is not known a priori.

Additionally, the descending semimajor axes progression is compliant with MIS-xx requirement of measure magnetic field, guaranteeing data redundancy and higher picture clarity (less noise and more details captured for a given camera resolution). 

As a precaution, since mission failure is likely to increase over time, higher stability orbits will be the last to be followed. 

Last but not least, the orbital eccentricity is kept as close to 0 as possible, in order to easily meet payload pointing requirements and, as an added benefit, simplifying a preliminary link budget analysis (reference al capitolo del link budget).

**Landing and Ground science operations** 

The In-Orbit operational phase will end with the landing site selection, then unnecessary payloads will be shut down and  landing maneuvers will begin.

This part will be managed by the GNC, aided by LIDAR and ADCS data. 

Since the landing site is not known in advance, the exact date and time of this phase can only be restricted to the duration of the last C Orbit, even though it would be preferrable to choose equatorial latitudes, in accordance to EPS and TCS requirements.

The landing phase will be broken down into two stages: the Hohmann maneuver and the Ground Approach phase. 

A periapsis altitude-reducing maneuver is carried on(from 500 m to 50 m), during which the spacecraft will orient itself, in order to achieve engine ignition, which in turns nullifies the In-Track and Cross-Track velocity components. 

At this point the only component will be the radial one and the satellite will be in free fall, under the action of the Bennu's gravitational acceleration (~ 8e-05 m / s2), up to the altitude of 10 m. 

Consequently, a new engine ignition has been planned, in order to further control the descent speed, resulting in a soft touchdown 20 minutes afterwards. 

During the ground approaching phase the solar panels will not be deployed. 

In order to estimate the ΔV Budget, the first landing meuver has been implemented in STK, while the remaining ones are a result of Simulink simulations. 

Provided that the landing operation is successful, the satellite will switch to its ground configuration, which is expected to last for three extra months.

The entire landing phase, including drop tests and ground approach, has been simulated in Simulink, with great attention to structural integrity, power system health and overall attitude control of the satellite. 

Assuming the tests have been correctly set up, no critical issues have emerged from the simulations.


### In situ

Provided that the landing operation is successful, all primary mission goals will have been achieved. 

The second mission stage will be entirely focused on the goal of opportunity.

Once correctly positioned on Bennu's surface, the satellite's battery pack is expected to be fully charged and ready to power all systems for its first ground analysis.

The X-ray diffractometer and CASSE will be operational for a whole day (with reference to the asteroid's daylight definition). 

Right after this first phase, the satellite is expected to have sufficient power to activate its mobility mechanism and beginning the exploration of Bennu's surface.

This mechanism will allow BOSS to move along parabolic trajectories, within a 
controlled range (further details in [reference al paragrafo sul mobility mechanism]).

Additionally, the guidance and control algorithm, aided by the IMU, will allow for a soft landing onto the target face, in order to perform additional surface inspections, while preventing damage to the most critical systems (e.g. solar panels). 

As mentioned in (reference al paragrafo sui sensori), proximity sensors will further ensure that the satellite has landed onto the correct face.

Once a new location is reached, solar panels will be deployed and the batteries charged, right after activating dust shields, which will minimize efficiency degradation, thus guaranteeing an optimal charging phase and greater longevity of the power supply chain.

Assuming dust accumulation is minimized, the entire charge should take no longer than a couple of Earth days.

Despite the negligible gravitational acceleration (~ 0.000098 m/s²), some of the operations described in this chapter, including landing and moving on the surface of the asteroid, might present several critical issues. 

Being aware of all these potential problems, each phase of the operation has been diligently studied and solutions have been implemented accordingly. 



## Operational modes & duty cycle

The duty cycle has been crucial in defining the power consumption of each component, in every possible configuration.

Fifteen different operational modes have been identified:

+ *Dormant mode* - All subsystems and payloads are powered off (Pre-launch, Launch, Transfer, In-orbit insertion).
+ *Checking mode* - The onboard computer is turned on and system integrity checks are performed. The CubeADCS, all GNC sensors and Comsys are active and in medium power consumption mode. Once detachment begins, power is entirely supplied by batteries. 
+ *Safe recharge mode* - Batteries are charged at a rapid pace, while the OBC and GNC sensors are idled.
+ *Detumbling* - All GNC related components, with the exception of the OBC (whose highest power threshold comprises the highest load from payloads), are under full load.
+ *Initial maneuver* - After reaching a stable orbit, solar arrays deployment begins and solar panels supply power from this moment on.
+ *Calibration* - All stage one payloads are pointed at Bennu and calibrated accordingly.
+ *High and low orbit service* - Further details in sections (mission analysis and payload).
+ *Orbiting maneuver* - Different power levels are required depending on the specific orbit change or adjustment maneuver (including station-keeping maneuvers).
+ *Landing maneuver* - Solar arrays are stowed, while all navigation sensors are active. 
+ *On ground analysis* - On ground payloads are active and operating under the power supply of the battery pack. 
+ *On surface movement* - An electric engine produces momentum for the mobility mechanism and is powered by the battery pack for relatively short, but high power consumption time spans.
+ *Cleaning mode* - The battery pack supplies power to the active dust shield. 
+ *Standby and recharge* - Most systems are in standby mode, while solar panels recharge the batteries during daylight. During night time, comsys are actively sending data to OSIRIS-REx, while also producing heat. 
+ *Passive mode* - Once EOL is reached, all systems power off, while the battery pack slowly dies. 
+ *Safe mode* - An emergency mode, during which only vital components are kept powered on. ComSys are not turned off, since they need to send all collected data to OSIRIS-REx, in case the mission is compromised. 





## Payload

### Magnetometer

Despite the lack of a magnetically active core, asteroids can keep hold of a residual but very faint field, that suggests the presence of ferrite or chondrite minerals, whose domains might have been aligned by past magnetic activities, perhaps in very remote areas of the Solar System or during its formation.

The triaxial flux-gate *NewSpace Magnetometer* has been selected, being particularly lightweight and abundantly used in LEO cubesats, thus giving this technology a chance to be tested in a deep space application.

Furthermore, OSIRIS-REx doesn't utilize any magnetometers, meaning that potentially interesting outcomes might surface from this new dataset.

### Mini-TES

A *Thermal Emission Spectrometer* is an infrared spectrometer, operating in the 6-35 µm range and can be used to unveil part of the chemical composition of a celestial body. 

The Mini-TES is a compact and lightweight model, which has already been used on the Phoenix Mars rover and has a 1 km resolution, assuming a 100 m altitude from the target's surface. 

### Lidar DLEM 20

This extremely compact LIDAR will densely sample Bennu's surface, producing a collection of point clouds, stored in a LAS dataset. 

This open and standardized file format, contains high-fidelity sampled and post-processed data, including x, y, z information. 

The information can later be used to produce 3D models of a certain voxel resolution and, combined with other scanning techniques, can utilize albedo, normal, ambient occlusion and roughness maps in order to render photorealistic raster images of the asteroid. 

### Chameleon imager

The Chameleon imager is a small and lightweight hyperspectral camera, operating in a 148 bands spectrum, ranging from visible to near infrared light.

This device can perform multiple independent tasks, including - but not limited to - studying the effects of solar pressure on the asteroid's motion, as well as mapping low albedo areas (< 1 %), seeking variations in spectral composition. 

Moreover, the instrument offers an opportunity to further study the Yarkovsky effect, by detecting Bennu's inertia and measuring how much the anisotropic emission of thermal photons affects its angular momentum.

### Thermopile detector

The thermopile detector is an infrared spectrometer, ranging from 1 up to 100 µm and is a redundancy for the Mini-TES, although covering a wider spectrum.

This instrument is not space-rated and non-essential for the mission, being just a test subject for general purpose technologies in space. 

### X-ray diffractometer X-123

This is another lightweight spectrometer, operating in the x-ray spectrum. 

Much like the Thermopile detector, this device is not space-rated and has been included for testing purposes.

### CASSE

Last but not least, the *Cometary Acoustic Surface Sounding Experiment* utilizes soundwaves to map objects' chemical composition, making it a great option to further enhance the spectral analysis with new datasets.

## Guidance, Navigation & Control

### Guidance

Payload sensitivity issues introduced a pointing accuracy requirement of x degrees.

A *closed-loop control system* with triaxial stabilization has been implemented, as described in ECSS. 

The guidance algorithm is a relatively simple implementation, as it's based on well defined angular range constraints (dependent on payload requirements), rather than instantaneous changes in angular displacement and velocity. 

Despite being a straightforward model, the algorithm should effortlessly guarantee an adequate pointing accuracy.

The ranges, as previously mentioned, are defined by payload contraints, but might be dinamically changed, assuming that an active maneuver is necessary.

### Navigation sensors

Appropriate high performance sensors have been diligently selected, in order to grant an optimal dataset to the navigation system, which calculates the instantaneous position in space (relative to a reference frame) and sends it to the guidance system, capable of error correction between *current* and *target* position, both in terms of rotation and translation.

Various sensors have been chosen, with the awareness that they all have their pros and cons, thus making it necessary to combine and extrapolate information from multiple datasets.

#### In orbit

+ *Gecko camera* -  A compact optical camera, operating in the visible light range, outputting images in the RGB color space. 
+ *Sagitta Star Tacker* - A special sensor that creates tracking points of the stars captured in its field of view and compares the tracking data with a preloaded fixed map of the stars. 
  The alignment of realtime tracked data and the map guarantees a great pointing accuracy, with the added benefit of a low computational cost. 

  The sensor can identify and discard bright spots that might be outliars, however, extremely close and bright objects can temporarily blind the sensor, which won't work properly if too many trackers are out of frame. 

+ *Inertial Measurement Unit* - A highly responsive and precise motion sensor, which measures accelerations via accelerometers and change in angular velocity via gyroscopes. 
  
  This particular model utilizes bleeding edge technologies, such as closed loop *FOG*s (Fiber Optic Gyro) and *QPA*s (Quartz Pendulous Accelerometer), which ensure higher performance. 

+ *Digital Laser Gyro* - A peculiar type of gyroscope, whose working principle is based on the phase interference between two incoherent laser rays. 
  
  The interference pattern depends on the angular velocity, which is derived accordingly.
    
#### In situ

+ *Proximity sensors* - Five of these sensors should be applied on each of the satellite's faces (one in the center and one for each vertex), for higher accuracy. 
  They can identify a distance and return a boolean (a binary value), depending on a certain proximity threshold and they will be used to determine the satellite's position, relative to the asteroid's surface.

  A deterministic integration algorithm (like a Karman filter), is preferrable, as it's a reasonable workaround when the satellite is in eclipse.
### Propulsion system and ADCS

The propulsion system is subject to payload constraints as well. 

Two different configurations have been evaluated:

+ *VACCO® Micro Propulsion Systems-CPOD Cold gas propellers* - This system maneuvers the satellite by propelling a pressurized cold gas through eight nozzles (two for each spatial DOF, plus two extra nozzles for redundancy). 
    
    This technique allows the system to be steered, but a stabilization mechanism (like reaction wheels) is required in order to lock and stabilize the desired orientation. 

    Three reaction wheels are installed as part of the integrated CubeADCS system, which includes its own CPU, specifically designed for attitude control and a set of related sensors (3 MEMS gyroscopes, 10 course sun sensors, a triaxial deployable magnetometer, a fine Sun and Earth sensor). 

    This configuration has two main advantages: the reaction wheels are not just a stabilization mechanism, they can be actively used for a fine tuned attitude control; secondly, thrusters can be used to desaturate the reaction wheels themselves. 

+ *CUA / VACCO®-CubeSat High Impulse Propulsion System-CHIPS* - The only relevant variable of this configuration is the propulsion block position, located onto the lower face of the spacecraft (with reference to the axis intercepting both BOSS's and Bennu's centers of mass). 

  Both orbital and attitude maneuvers are performed by the engine itself, however, reaction wheels are still necessary for attitude stabilization and control. 

The latter has been chosen, as it still grants a highly accurate attitude control, while simplifying the in-depth analysis required by thrusters allocation.
A momentum budget has been calculated by taking the effect of environmental perturbations into account and attitude control actuators have been sized accordingly.

As a precaution, the maximum deviation from the local vertical axis has been set to 5 degrees. 

The total disturbance torque, calculated as the root sum square of all torque contributions, amounts to 9.1E-5 Nm.

All the parameters needed to compute this budget have been obtained from the satellite's configuration (e.g inertia) and orbital characteristics.

Furthermore, the worst case scenario emerged from the analysis is a 180 degrees maneuver, performed in a 5 minutes time span (de-orbiting maneuver).

The required slewing torque is 0.07 Nm.

All the selected sensors and actuators are COTS (datasheets in the applicable documents). 

The ADCS is tightly linked to the GNC, as they're part of the same closed-loop system.





## ComSys

All the communications to Earth are relayed by OSIRIS-REx, in S-band. 

A transmitter and a receiver communicate with the mothercraft by using two redundant unidirectional flat antennas. 

Originally, a trans-receiver had been taken into consideration, but given the limited access to online resources, a better suited configuration has been opted for, with two separate devices. 

This architecture allows for a more balanced uplink/downlink data distribution, while keeping power consumption lower.
### Link margin

The link margin is calculated with the following formula: 

Eb/N0 - Eb/N0 req

The signal to noise ratio should be evaluated, in terms of energy ratios: 

formula dell'Eb/N0, non mi ricordo come si chiami blablabla

Some values are known, like Boltzmann's constant (converted to dB) or other relevant info found in datasheets. 

Other values, like signal losses, system noise temperature and data rate have either been calculated with specific formulas or assumed to be a typical value, provided that data tables weren't available. 

Some assumptions have been made in regards with losses.

Firstly, atmospheric losses have been completely neglected, as the asteroid lacks a proper atmosphere.

Secondly, path losses have been roughly estimated, by assuming concentric circular orbits of BOSS and OSIRIS-REx, for the maximum slant range, and by using some trigonometry, as shown in the picture below.




The path losses are calculated by the formula: quella di Ls

System Noise Temperature is found in a table with typical values. (fatela per favore, non si possono vedere gli screenshot)

Finally, the required Eb/N0 can be estimated by a plot of the Probability of Bit Error Rate, assuming the modulation type is known (QPSK for the transmitter and receiver, according to manufacturers). 

A ~ 25 dB link margin has been estimated for both uplink and downlink connections, which exceeds the 10 dB recommended margin for optimal data transfer.

magari mettete una tabella con tutti i dati numerici raccolti, dovbrebbe già averla pronta Mariano







## Thermal control system

As shown in the thermal budget, payloads and subsystems require a certain optimal temperature range (0-30 °C). 

The *TCS* is implemented following the results of the *heat equation*, which provides a mathematical model that takes into account all the relevant heat fluxes.

The satellite is assumed to be a fixed volume sphere, with a 0.357 m² surface area. The thermal influence of solar arrays is negligible in this approximate model, due to the fact that they cast a shadow on the satellite itself. 

Given that the mission is split into two main stages, a different thermal analysis is required for both of them. 

The average heat fluxes given by direct sunlight, Bennu's own infrared emission and its solar albedo are used in this calculation, as they provide a reasonable value for both daylight and eclipse.  

These three contributions are relevant when operating on the asteroid's surface but, when in orbit, direct sunlight is substantially more significant.

In both scenarios, however, the overall direct sunlight and internal heat dissipation contribution is greater than that of albedo or infrared emission. 

While generally speaking the heat flux generated by conduction is not marginal, it is negligible on Bennu's surface, as its covered by a layer of regolith, a mineral with extremely low thermal conductivity. 

Given the insignificant contribution of conduction and due to empirical observation, it is safe to assume that the interally dissipated heat is equal to that generated by the satellite's systems. 

In regard to the on-surface conduction calculations (including a heat capacity budget), a thermal-electrical analogy model has been implemented, assuming the satellite is a rectangular prism. 

After evaluating all trade-offs among different materials, Kapton Film with aluminum backing has been opted for, given its overall advantageous thermal properties (0.50 mil, 𝛼 = 0.34, 𝜀 = 0.55).

tabella qui

As seen from the results in the table above, the TCS needs to take care of several issues, including the need of a heating system for in situ operations.

Thermofoil heaters have been selected for their low thickness and lightness (0.25 mm, 0.04 g/cm²), as well as their low power consumption (assuming a 100 % efficiency, 5 W should be enough to keep the system warm in any condition).

Overheating is another issue that needs to be faced, either by using passive cooling systems, active ones, or a combination of both. 

Despite not being a common solution in spacecrafts, a passive cooling system via *TVC*s (Titanium Vapor Chamber) has been implemented, taking into consideration that this solution can be relatively more lightweight and efficient, compared to traditional heat pipes. 

The dissipation principle is simple: a change of phase from a liquid to a vapor maintains a constant temperature until the transition is complete, while dissipating heat in the chambers. 

In addition to the TVCs, *MLI* (Multi Layer Insulation) has been chosen, as another passive thermal protection system. 

This kind of protection, which is generally reliable, lightweight, versatile and cost-effective, has been selected for particularly heat sensitive components, such as batteries, some payloads like the Chameleon Imager and fuel tanks.

Last but not least, it's crucial to point out that a good portion of the thermal analysis involves finding an excellent systems distribution inside the available volume, since a bad allocation of components can nullify the benefits of a well designed Thermal Protection System.



## EPS

The Electrical Power System comprises a set of custom solar panels, a battery pack and a PDCU (Power Conditioning & Distribution Unit). 

The first step needed to appropriately size the EPS is the evaluation of a power budget, where a 5% and a 20% margin have been taken into account, for COTS and other components, respectively (in compliance with AD3). 

As standard practice, the budget has been calculated assuming the worst case scenario (full load operational mode) and an average solar flux of 1367 W/m².

Triple junction Gallium Arsenide cells have been chosen for their superior efficiency and equipped with autonomous sun tracking sensors, which will maintain (when possible) a perpendicular angle between incident solar radiation and the panels themselves. 

The installation of these sensors reduces the load on the ADCS, avoiding unnecessary maneuvers and maximizes the array's efficiency.

As different systems require a diversified distribution of voltages and power, a PDCU has been installed as the power supply unit.

In order to cut down on costs and complexity, stock components (such as space qualified CubeSat solar panels by ISIS) have been preferred whenever possible.

Each of the chosen panels can produce 3V in nominal conditions and the array has been sized after a power conversion estimate, assuming this voltage for a 6 months mission (until EOL).

As abundantly explained in previous chapters, a battery pack is required during certain mission phases. 

Given their higher energy density and the absence of a memory effect, as well as their overall superior durability, Lithium-Ion batteries have been opted for. 

In-depth estimates have highlighted that the total daily energy output of the solar panel (for a 0.2420 m² surface area) roughly amounts to 25 Wh. 

This implies that during eclipses, the battery pack should output the same amount of energy.

As previously mentioned, recharge cycles should be taken into account when sizing the battery pack.

Despite being higher than usual, a 50% Depth of Discharge has been set to be adequate, given the overall short mission duration.

The EXA-BA01 Lithium-Ion battery cells have been opted for, after a thorough research. 

They can produce up to 88.8 Wh, at 3.7V or 7.4V, weighing only 215 g. 

In order to reach the desired total capacity and for redundancy reason, a dual double cell configuration has been chosen. 

This should keep the system functional, with a single cell failure tolerance. 

The power they produce will be, as earlier underlined, managed by the DPCU. 

This top grade PSU will meet each subsystem's demands, guarantee electromagnetic compatibility and protect the most sensitive components from sudden power surges.



## OBC

UNIBAP's *SpaceCloud iX5-100* is the onboard computer of choice for this mission. 

It features a *Cortex M3* 32-bit ARM CPU, which is a common chip architecture in server clusters and very specific applications that require high reliability and low power consumption (like spacecrafts), considering that it's substantially more efficient than common desktop architectures like x86 or AMD64.

The computing module supports a wide variety of I/O, such as a mini-PCIe Gen2 expansion card, SATA v3, USB 3.0 and 2.0, Gigabit Ethernet and more. 

The PCIe lanes allow for the addition of a dedicated GPU, essential for  image data handling. 

In addition to this, several Neural Processing Units have been added for AI algorithms. 

A custom GNU/Linux distribution, tailored to the very specific needs, is built and installed on an M.2 SATA SSD, used for the OS and various softwares. 

A RAID 6 NAS of high capacity space-rated M.2 SSDs is used for mission data storage and utilizes the onboard Gigabit Ethernet of the computing module. 

## Energy budget

Once the power generation and management have been studied and properly defined, as described in (reference a EPS e capitolo delle operational modes), the battery state of charge needs to be mapped for the entire mission. 

As visible from the plot below, a battery charge profile has been calculated. 

Three distinct profiles have surfaced from the analysis: 

+ *Pre-detachment phase*
+ *In orbit analysis*
+ *In situ analysis*

The following plot highlights the first phase, where power consumption will be driven by the initial powering on of the OBC.

(mettete qui il plot zoomato)

During system integrity checks, right before detachment, the satellite will be anchored to OSIRIS-REx and the solar arrays will not yet be deployed nor exposed to sufficient sunlight to be operative. 

Therefore, part of the battery energy needs to be used.

During the release phase, the solar panels will begin recharging the battery pack, although at a slower rate than the fully deployed configuration (1/6th of the total charge has been assumed, given that the satellite's attitude is unknown).

Once fully charged, the detumbling mode will take place, producing a modest  net power loss, despite the array being operative. 

At the end of this phase, however, solar panels will be deployed and outputting 67 Wh, charging the batteries at their nominal maximum pace. 

Once again, the battery pack will be fully charged and then the in orbit phase will begin. 

During this phase, net power consumption will never exceed the power output of solar panels, which will be solely used as a power source, assuming no emergency or malfuction of the system.

However, if any undesired event were to cause an unexpected failure, the battery pack should be able to keep BOSS in Safe Mode for over 7 eclipses. 

As the landing phase begins, the solar array will be undeployed, thus producing a lower power output. 

A battery drain, followed by a discharge, is expected to happen during this phase, since the satellite is predicted to land on the asteroid's surface during an eclipse. 

As soon as BOSS is exposed to sunlight, the solar array will be deployed and will start outputting ~ 50 Wh. 

The first in situ analysis will last a day on Bennu (roughly 2h 17m on Earth) and the solar array is powerful enough to keep the batteries charged, despite several payloads being in function.

Once the eclipse is reached again, the satellite will start moving on the surface of Bennu, activating the onboard electric engine. Additionally, electrodynamic dust shields will require additional power, discharging the batteris by roughly 30%.

As soon as this discharge threshold is exceeded, BOSS will enter Stand-by&Recharge mode for a few days, allowing for a new analysis cycle.

(plot di questa fase, non mettete screenshot per cortesia, qui come in ogni altro elemento del documento, salvare il plot come SVG o EPS o almeno PNG da matlab non richiede alcuno sforzo, non può farlo chi deve scrivere il documento)

Since a minimum degradation of the solar cells is intrinsecally unavoidable and the shields can't possibly eliminate all the cumulated dust or debris, a 0.3% cyclic degradation parameter has been assumed. 

The progressive performance reduction will increase each recharge cycle time, until the solar panels reach a point where they can't produce energy levels that exceed power consumption. 

Using the above mentioned factor as a reference point, the satellite is estimated to conduct a total of 32 in situ inspections.

(plot della fase finale qui)

Especially during the last cycles, given that the power consumption during eclipses will exceed that produced by the panels, the interval between each new analysis is reduced to four days. 


## Data budget

The data budget had to be estimated with very limited data from manufacturers of the various instruments comprising the payload. 

However, considering how inexpensive SATA SSDs are these days (even space-rated ECC NAND Flash is relatively low-price, given the budget) and considering that the M.2 format is extremely compact and lightweight, a RAID 6 NAS of high capacity SSDs has been implemented, in order to safely store months of image data.  

The Gigabit Ethernet might be a bottleneck, however the NAS is intended to be used as a reliable backup storage, while data is still initially stored onto the main M.2 drive and transfered to Earth, close to realtime. 

The realtime data transfer, relayed to OSIRIS-REx, requires that the satellite and the mothercraft are in LOS. 

If this condition is not met, the onboard main SSD should have enough residual capacity that all the sensors' data collected during that time span can be stored and backed up, knowing that the ethernet connection might be saturated. 

Assuming a daily 5 hours eclipse duration and no compression algorithms, a rough estimate of a data budget for the main SSD has been evaluated. 

Each raster image size depends on its color space (number of channels), color bit-depth and pixel density and can be calculated with the following formula: 

formula del data volume

The Chameleon Imager outputs 12 bits uncompressed RAW images (JPEG output is available, but it is a lossy compression) and operates with 148 channels. 
Spatial resolution is given by its datasheet. 

There are still perplexities, since the datasheet is not abundantly clear: despite being a hyperspectral cam that detects data in a 148 bands spectrum, the output picture should still be an RGB (or RGBA) image, thus 3 or 4 channels should be used in the formula. 

However, for lack of clearer data, 148 channels have been assumed as a worst case scenario. 

This should result in 1.9 GB single images, with a resolution of 1 MP.

Other instruments lack sufficient data for performing an equivalent estimate.

The LIDAR doesn't produce raster images, but rather outputs point clouds and stores information in LAS files, which are typically very large (although LAZ, their compressed version, could be used) and cointain information required for the reconstruction of a 3D model. 

What makes LAS file sizes increase is not the information stored in single points, but rather the increase in scan time, surface areas and cloud density.

Given that the data rate of all instruments has been estimated to be approximately 50 Mbps and using a 5 hour eclipse time span, a temporary storage requirement has been calculated. 

Considering the lack of data and the fact that the operating system and software already use part of the main storage (and might require more in the future), taking into consideration that, depending on the file system, read/write performance can degrade when a drive is close to being full, an extra 30% margin has been added, resulting in a 137 GB maximum daily requirement, which will be backed up in the NAS and transferred to OSIRIS-REx, once in LOS again.

## Velocity budget

The ΔV has been estimated to be 0.68 m/s, taking four contributions into account:

+ Changes in operative orbit, including orbit insertion maneuvers, the three Hohmanns maneuvers used to reduce orbital altitude and station-keeping maneuvers, assuming a 5% margin of error 

+ Landing maneuvers, whose intrinsecally higher uncertainty required a 10% margin

+ Attitude control, including velocity budgets for 15 cycles of reaction wheels' desaturation, calculated by taking disturbances and thrusters features into consideration. Given the attitude control has the highest uncertainty, a margin of 100% has been assumed

All the margins are compliant to ESA Margin Philosophy.




## Structures

Among the numerous options, a CFRP (Carbon Fiber Reinforced Polymer) deployable structure has been designed, as it's a common solution in space applications, where reducing volume and inertia during launch is a key aspect of a successfull mission.

This design arises several challenges, ranging from the complexity of the concept itself, all the way to the appropriate choice of deployment mechanisms. 

The supporting frame is made with Al6061 and, after mesh optimization studies, its mass has been cut down by 70%, resulting in a light 3.39 kg structure. 

The prism faces are supported by stringers, which protect the inner systems and payload from landing shocks:

+ 2 side faces, 7 stringers
+ 2 side faces, 2 stringers
+ top face, 3 stringers 
+ bottom face, 3 stringers

The overall dimensions, in its non deployed configuration are 36.6 x 22.9 x 23.9 cm (L x H x W).

The solar panel deployment is handled by four rotational joints, directly installed on the top face. 

Another structural problem is that of landing impacts. 

Several Solidculo simulations have been run with varying parameters. 

Initial conditions had been set to 20 cm/s (collision velocity) and a 0.3 damping coefficient, however, further studies highlighted that these values were too high, due to Bennu's low gravity.

That same simulation has thus ben run with Earth's gravity, showcasing a good stress resistance of the structures. 

Further details are available in (reference all'annesso). 





## Spacecraft configuration

The spatial allocation of systems and instruments requires the ability to find an optimal compromise that takes into consideration multiple issues, including - but not limited to - well-thought-out volume utilization, thermal dissipation and electromagnetic interference (this one being generally minimized by design in space-rated components).

Most importantly, a vital requirement is that payload instruments are distributed in a way that doesn't interfere with their correct functioning.

Since most of the instruments require directly pointing at their target, they've been oriented towards the outside of the satellite. 

Three AsGa solar arrays have been placed onto the faces with the highest surface area, in order to produce the highest power output. 

non dite che per mostrare X è fornita la seguente immagine, non c'è alcun bisogno

mettete direttamente l'immagine in questo caso

## Dust and particles problems

Dust and particles accumulation is a serious hazard in space missions. 

At first, the absence of dust and debris during the in situ stage's critical phases (e.g. rotational transfer) has been assumed and the hypothesis of a worse yearly life degradation has been made in order to compensate for the strong assumption. 

However, this oversimplification might be a critical issue that should be addressed with a better solution. 

Among the many possibilities, an Electrodynamic Dust Shield has been used for the solar panels, given that it's a tried and tested technique. 

The shield is comprised of a transparent film of ITO (Indium Tin Oxide) and glass, which can actively employ electrostatic and dielectrophoretic forces that remove dust on its surface. 

An electromagnetic wave is produced along its surface by out of phase and indipendently charged electrodes. 

As seen in [bibliographic reference], there's over a 90% recovery of the initial voltage, once the shields are active. 



## Mobility mechanism & attitude and anti-bouncing control 

The satellite employs a mobility mechanism in order to move on the asteroid's surface. 

The mechanism involves an impulse electric engine, which transfers angular momentum to the spacecraft through a mass, connected to the frame by a mechanical arm.

The angular range can be controlled by a specific support, depending on the impulse's intensity. 

The motion is controlled by an algorithm, specifically optimized for attitude and anti-bouncing control. 

Its attitude controller handles the angle with respect to Bennu's surface with adequate corrections at landing. 

The algorithm effectively damps and redistributes rotational kinetic energy in the system.

The system is thus capable of protecting the satellite from impacts and pure rolling motion, which is a critical issue for exposed and easily degradable components like solar arrays. 

The mathematical model and implementation of the algorithm can be found in AD_mob_mech.

## Risk assessment 

The analysis has been carried out since the beginning and progressively fine tuned as the mission design improved. 

Potential risks have been identified and mapped onto a critical paths map and a risk matrix, once causal links among risks have been recognized, starting from a brainstorming analysis of hypothetical scenarios. 

The critical paths map is color-coded in order to highlight association and cross-links between risks and their team of origin. 

The process is analogous for the evaluation of project quality risks and risks related to the ongoing learning process. 

The risk matrixes showcase unacceptable risks, in terms of severity and likelihood. 

Once the unacceptable risks have been assessed, several mitigation responses 
have been implemented, promoting all risks to acceptable. 

The entire analysis is compliant to ECSS-M-ST-80C31July2008 Risk Management.

# Study management 

## Organization Breakdown Structure

The organization has been structured into a horizontal hierarchy, comprised of three main working groups (Management, Engineering, Science) and each unit has been managed by two or three individuals, chosen with consent of the entire team. 

## Work management

During the very first meetings, the entire team worked in unison to common goals and tasks, discussing various topics, including the organization breakdown itself. 

The decision to use a horizontal hierarchy, rather than a pyramid structure, allowed for a better management of the group, as well as plenty of chances to 
be exposed to constructive criticism, mutual supervision of the work in progress and necessary data and documentation provision. 

Last but not least, this kind of structure emphasized the optimized parallelization of tasks and a fair distribution of workload.

## Work Breakdown Structure

The entire work has been broken down into seven packages:

+ *Study organization (WP0)* - Group organization and coordination, first individual assignments
+ *Mission overview (WP1)* - Research and definition of mission goals
+ *High Level Analysis (WP2)* - Identification of stakeholders' needs, definition of mission requirements, STM and TTM development
+ *Feasibility Analysis (WP3)* - Mission architecture, concept of operations and operational modes definition
+ *Systems preliminary design (WP4)* 
    + *Subsystems design (WP4a)*
    + *Payload identification (WP4b)*
+ *Budgets (WP5)* - Evaluation of budgets in terms of mass, volume, cost, etc
+ *Spacecraft mechanical design (WP6)* - Structural design of the spacecraft and systems allocation
+ *Risk assessment (WP7)* - Risk assessment of all the project's phases
  


## Study Timeline

The entire project has been broken down onto a timeline, using Gantt's web client. 

tutto quello che segue è ridondante rispetto a quanto detto nei capitoli precedenti e alla timeline che è self explanatory, non riempite di filler pls

# Conclusions and recommendations
 








