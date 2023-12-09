# FAST (FlightAware Scraping Thingy) II

_by [Josh Glottmann](https://github.com/glott)_

**Version 2.1.4** - 12/09/2023

Creates scenario files for [ATCTrainer](https://atctrainer.collinkoldoff.dev/#about) by [Collin Koldoff](https://github.com/collink2451) using data from [FlightAware](https://flightaware.com/)\* and [Flightradar24](https://www.flightradar24.com/)\*.

A newer and fancier version of [FAST](https://github.com/glott/FAST).

__[Download v2.1.4](https://github.com/glott/FAST-II/releases/latest/download/FAST-II.ipynb)__ 

---
### Installation

1) Download `FAST-II.ipynb` from the link above or on this repository's [releases](https://github.com/glott/FAST/releases/latest) page.
2) Download and install the latest version of [Python](https://www.python.org/downloads/).
3) Download and install the latest version of [Jupyter](https://jupyter.org/install).
4) Run `FAST-II.ipynb` from Jupyter.

---
### How it works

- Every minute (if possible) FAST II finds all planes in the box you define. The API to get plane data isn't fast so it takes ~0.5-1 s/plane to get the plane's position data. It spawns the plane in at the position it was capture at at the time it was at that position.

- Every minute (or whatever you define), it looks to see what planes are in the airspace again. If the plane has already been spawned in, it is ignored.

- From a practical perspective, this means that a lot of planes appear everywhere, in final airspace, etc. since they've never been "seen" before.

- After you get that initial blob, all other planes should be departures, planes entering the boundary, or planes that happened to not be broadcasting data to FR24 before (rare)

---
*\* Josh Glottmann is not responsible for any misuse of this software.*
