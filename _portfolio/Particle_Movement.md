---
title: "Particle Movement - Visualization with Python and VMD"
excerpt: "Utilized Python to simulate particles in a box. I analzed the simulation and generate a xyz file to visualize using VMD."
collection: portfolio
---
This [project](https://gitfront.io/r/janellecheung/QHBtzxc8cMTW/Compiled-projects/blob/LJs-fluid/LJfluid.md)  looks at modeling fluid mechanics using Lennard Jones and Velocity-Verlet scheme. Velocity-Verlet scheme is a simple way to calcualte the trajectories of a particles used in molecular dynamic simulations using Newton's equations of motion while Lennard Jones models VanderWaal interactions. After analysis, I also visualized the system using [VMD](https://www.ks.uiuc.edu/Research/vmd/). Current works on this project includes using [GROMACs](https://www.gromacs.org/) and comparing the scripts written in python and 

In the [python script](https://gitfront.io/r/janellecheung/QHBtzxc8cMTW/Compiled-projects/blob/LJs-fluid/Molecular_dynamics.ipynb) I wrote a script that generates a coordinate file of atoms using FCC lattice and add velocities to each particles in a normal distribution with an inizitalized Temperature. Then I wrote a script that will loop over the velocities and accerlation of atoms close to each other for a period of time allowing for equilibration of the system, if the system is not at equilibrium, I continue looping the system until it reaches equilibrium. 
<div class="container"> 

<figure>
    <img src="\images\Energytempdata.png"
         alt="Energy tempture data"
          width="400" height="300">
    <img src="\images\Radialdistribution.png"
         alt="Energy tempture data"
          width="400" height="300">
</figure>
</div>

When the Energy, Temperature of the system is not fluctuating anymore the system is at equilibirum as shown in the image on the left. The image on the right is one of the analysis plot that I ran was the Radial distriubtion, which is shown below indicating the system is a gas. 

Visualizing the system I used VMD to generate a mpg file and changed it into a gif using the following script in command line. 

```ffmpeg -i LJ_pytho.mpg LJ_python.gif```

![Gif of particle movement](/images/LJ_python.gif) 