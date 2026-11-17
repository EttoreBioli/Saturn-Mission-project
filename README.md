Kronos Mission: Interplanetary Trajectory Design

This repository contains the MATLAB codebase for Project Kronos, an interplanetary space mission design inspired by the ESA Rosetta mission.
The objective of the mission is to design a trajectory from Earth to Saturn—utilizing planetary Gravity Assists (Flybys)—to achieve Saturn Orbit Insertion (SOI) and observe
its moons, Titan and Enceladus. The mission timeframe spans from August 2034 to October 2046.

## Project OverviewThe trajectory is computed using the Patched Conics 
Approximation under the assumption of coplanar planetary orbits. 
The mission is divided into sequentially computed phases:
  1) Initial Parking & Plane Change: Aligning the spacecraft's orbit with the ecliptic plane.
  2) Interplanetary Transfer: Solving Lambert's Problem to find the required velocities to travel between planets.
  3) Earth Escape & Targeting: Computing the escape hyperbola and applying manual targeting corrections to compensate for orbital alignments.
  4) Planetary Gravity Assists: Executing flybys at Earth and Mars to gain $\Delta V$ without consuming propellant.
  5) Saturn Orbit Insertion (Capture): Performing a braking maneuver to enter a highly elliptical parking orbit around Saturn that intersects the orbits of Titan and Enceladus.

    
## Key Features & Methodologies
  Keplerian Mechanics: Direct and Inverse Kepler problem solvers to compute orbital anomalies and propagate planetary ephemerides.
  Lambert's Problem Solver: Designing the interplanetary cruise phases.Numerical 
  Integration (ODE45): High-precision propagation of the spacecraft's state vector (position and velocity) inside and outside the planetary Spheres of Influence (SOI).
  Event-Driven Simulation: Implementation of custom ODE event functions to automatically detect SOI entry/exit boundaries.
  $\Delta V$ Budgeting: Calculation of the total $\Delta V$ cost (approx. $14.74$ km/s) across all maneuvers (Plane change, Escapes, Corrections, and Saturn Capture).

## Author
Bioli Ettore 
Giugliano Rolando 
Modesti Alessandro 

Master's Students in Robotics and Automation Engineering | University of Pisa
