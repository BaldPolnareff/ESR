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

## Mission analysis
### In orbit
### In situ

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

Three different configurations have been evaluated:

+ *VACCO® Micro Propulsion Systems-CPOD Cold gas propellers* - This system maneuvers the satellite by propelling a pressurized cold gas through eight nozzles (two for each spatial DOF, plus two extra nozzles for redundancy). 
    
    This technique allows the system to be steered, but a stabilization mechanism (like reaction wheels) is required in order to lock the desired orientation. 





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

## OBC

UNIBAP's *SpaceCloud iX5-100* is the onboard computer of choice for this mission. 

It features a *Cortex M3* 32-bit ARM CPU, which is a common chip architecture in server clusters and very specific applications that require high reliability and low power consumption (like spacecrafts), considering that it's substantially more efficient than common desktop architectures like x86 or AMD64.

The computing module supports a wide variety of I/O, such as a mini-PCIe Gen2 expansion card, SATA v3, USB 3.0 and 2.0, Gigabit Ethernet and more. 

The PCIe lanes allow for the addition of a dedicated GPU, essential for  image data handling. 

In addition to this, several Neural Processing Units have been added for AI algorithms. 

A custom GNU/Linux distribution, tailored to the very specific needs, is built and installed on an M.2 SATA SSD, used for the OS and various softwares. 

A RAID 6 NAS of high capacity space-rated M.2 SSDs is used for mission data storage and utilizes the onboard Gigabit Ethernet of the computing module. 



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





## Spacecraft configuration

The spatial allocation of systems and instruments requires the ability to find an optimal compromise that takes into consideration multiple issues, including - but not limited to - well-thought-out volume utilization, thermal dissipation and electromagnetic interference (this one being generally minimized by design in space-rated components).

Most importantly, a vital requirement is that payload instruments are distributed in a way that doesn't interfere with their correct functioning.

Since most of the instruments require directly pointing at their target, they've been oriented towards the outside of the satellite. 

Three AsGa solar arrays have been placed onto the faces with the highest surface area, in order to produce the highest power output. 

non dite che per mostrare X è fornita la seguente immagine, non c'è alcun bisogno

mettete direttamente l'immagine in questo caso

## Dust and particles problems



## Mobility mechanism & attitude and anti-bouncing control 

# Study management 

## Organization Breakdown Structure

## Study management

## Work Breakdown Structure

## Study Timeline

# Conclusions and recommendations













