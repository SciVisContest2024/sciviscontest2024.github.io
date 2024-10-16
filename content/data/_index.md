---
title: 'Data'
date: 2018-11-28T15:14:39+10:00
weight: 1
---

If you want to skip the background for now, go and [download the data]({{< relref "#Download Data" >}}) directly.

This year's contest deals with the Visualization of Sonar Imaging data for Hydrothermal Systems.
A team of scientists from Rutgers and UW have developed acoustic imaging methods to detect hydrothermal discharge, quantify volume or areal fluxes, and estimate heat contents of discharge from deep sea hot springs.  Deep sea hot springs discharge both focused high temperature fluids at black (and white) smokers to produce buoyant plumes and diffuse lower temperature fluids from a broad area of cracks and other features in the seafloor.  As part of this, we built and deployed the Cabled Observatory Vent Imaging Sonar, usually called COVIS.  COVIS had three modes of operation: discharge mapping, plume imaging, and plume velocity detection.  The plume imaging and plume velocity detection produced fully 3D observational volume data sets.  COVIS imaging operated by sending sound out into the water column and listening for the reflections and backscattering from particles and discontinuities (technically impedance contrasts) in the water.  COVIS was based on a standard multibeam sonar so each outward ping yielded a plane of data.  Mechanical rotation pivoted this plane vertically through the water column to provide full 3D imaging.  Most of the backscatter observed is believed to result from temperature fluctuations that change both density and compressibility.

{{< rawhtml >}}
<img src="/image1.gif" alt="Animation of COVIS data" class="matlab">
<p style="color: grey;">A month of COVIS imaging data (Oct 2019) is combined with bathymetry to showcase some of the variations and changes that occur over a month. This is an overlay of three isosurfaces (blue, purple, red) of the imaging data onto a base surface (green).</p>
{{< /rawhtml >}}

COVIS uses sonar to capture information about hot fluids discharging at the seafloor [\[ 1 \]]({{< relref "#References and Acknowledgments" >}}).  Sonar is like radar only using sound.  Sound is sent out actively; it scatters or backscatters off of density and impedance contrasts (related to compressibility) and returns. Known scatterers include temperature contrasts, density contrasts, and particulates.  Rapid fluctuations in temperature are believed to be the main scatterers in hydrothermal plumes [\[ 2 \]]({{< relref "#References and Acknowledgments" >}}). COVIS produces the following data products:

- **Plume images** are 3D volumes with the main variable the backscattering strength at every point within the volume.  The three dimensions come from the multiple beams of the sonar instrument, the travel time to the scatterers and back, and the rotation or movement of the sonar instrument through space.  See details in [\[ 1 \]]({{< relref "#References and Acknowledgments" >}}). Raw data are in native coordinates (roughly spherical coordinates from the sonar receiver).  Processed data is interpolated onto a uniform rectangular grid.
- **Plume doppler velocity estimates** are also 3D volumes but with vertical velocity and backscattering strength as variables.  The initial processed values are line-of-sight velocities but the plume orientation is used to estimate the relative horizontal and vertical components.
- **Diffuse maps** are 2D datasets which map out the heat flux density or decorrelation intensity stemming from low temperature, low flow rate discharge on the seafloor.  This data differs in several ways: the recorded signal bounces off the seafloor, we are looking at travel time changes and ping-to-ping correlation of the signals, and the outgoing sound comes from a wide angle transmitter.  The processed data is interpolated onto the local bathymetry.

COVIS imaging data is collected by rotating a multibeam sonar up and down from a horizontal base position.  The three dimensions then come from the multiple beams, the elevation angles of the physical rotation, and the travel time of the sound signal out to a scatterer and back to the sonar.  

The plume imaging data is intended to capture an overview of the structure, size and shape of the buoyant plume rising above the hot springs.  Of primary interest are capturing the response of the plume to local ocean currents (including tidal currents) and understanding the connections between the multiple points of discharge and the overall shaping of the plume or plumes present above the discharge. The anticipated decrease in backscatter intensity as the plume dilutes has the potential to additionally provide direct estimates of heat flux. 

Work with the first deployment of COVIS at Endeavour Ridge resulted in a paper that suggested that changes in the typical plume bending directions could be indicative of mid-ocean ridge segment scale changes in hydrothermal venting [\[ 3 \]]({{< relref "#References and Acknowledgments" >}}).  Preliminary analysis of data from the second deployment at Axial Seamount observed great variation in the apparent merging of sources and overall plume structure.

One of the major challenges in working with this data is extracting the plume and its centerline from a relatively undersampled volume.  There are two basic issues.  First, isosurfaces cross the plume centerline due to the increasing dilution as the plume rises and entrains seawater. Additionally, the plume shows lateral dilution.  Unless the surrounding ocean is very clean acoustically and the plume signal is much stronger than the base level of the sonar, defining a boundary for the plume is not straightforward.  Previous work used either multiple isosurfaces [\[ 4 \]]({{< relref "#References and Acknowledgments" >}}) or fit Gaussian functions to slices perpendicular to the plume centerline [\[ 1 \]]({{< relref "#References and Acknowledgments" >}}).  The second issue stems from the relative wispiness of a weak plume in a strong current combined with the relatively low spatial resolution of the acoustic data.  This results in disconnected isosurfaces and challenges in identifying the exact location of the centerline of the plume. A final note should mention that all the above assumes the analysis starts with the standard gridded data but that is an interpolation from the semi-structured raw data (composed of multiple planes or pings directed in a series of different angles of elevation).

Based on this, we have provided a list of visualization [tasks](/tasks) for this contest.


{{< rawhtml >}}
<div style="height:  20px"></div>
{{< /rawhtml >}} 

----------   

{{< rawhtml >}}
<div style="height:  20px"></div>
{{< /rawhtml >}}