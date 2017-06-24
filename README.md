# cubesat-book
## Author's Note
Dear Reader,

Cubesats are an incredibly exciting platform. If you are thinking about building a cubesat, I hope some of this content is useful for you!

My goal with this book is to provide some lessons learned for cubesat development, as well as share some models that can help educate design constraints for both your mission and your spacecraft.

Note that the opinions are my own, and do not represent my employer.

## Launch :rocket:
### Why start with launch?
Normally it would make sense to start with mission design, but if you want to iterate hardware and software quickly start with launch. If you plan to have many spacecraft, your goal should be to launch as early and often as possible.

It makes sense to target an aggressive time line for your first launch. Avoid becoming a company with a satellite waiting to launch. This can misalign your short term incentives (mission assurance, simulation, etc) with your long term incentives (many spacecraft, automation, production line).

The "Agile Aerospace" way is to try to close the value chain as soon as possible. This means _delivering_ - a pixel, a packet, etc with your first spacecraft. We can call this _closing the value chain_, and then _iterating_ on all of the pieces of the value chain that need improvement. This methodology ensures that you don't have surprises, and that you are _working on the right thing_!

Many spacecraft designers ignore the complexities of operations, as well as the ground network. A few half-working satellites in space is worth a great deal for a company building out these capabilities.

Launches are usually few and far between, and launch dates are difficult to predict, as they can slip several months to years.

### Differences between Launches
You should understand enough about the launch to understand if it is a non-starter for your mission, but in general being open to various orbits is beneficial.

The main differences between various launches are:
1. orbit geometry
  1. lifetime
  2. power
  3. thermal
2. launch vibration

#### Orbit
##### Brief Overview of Orbits
In order to talk about orbits in general terms, there are a few classifications of orbits that are useful to build intuition around.

###### Circular vs. Elliptical
No orbit is truly circular, but in general orbits that have a similar apogee (point of closest approach) and perigee (point of furthest approach) are called circular.

Other orbits may be described as elliptical, or sometimes highly elliptical depending on the ratio of the perigee to apogee.

The ellipse will also precess (rotate) within the orbital plane. This is called apseidal precession. You can think of it as so the point of closes approach will slide along the orbital plane over time.

###### Polar vs. Equatorial and everything in-between (inclination)
The inclination is the angle between the orbit and the Earths equator. Polar orbits tend to have inclinations ~90deg, while equatorial orbits have inclinations around 0deg.

##### Lifetime
You should avoid launches to orbits with lifetimes that are much longer than you actually want to operate your spacecraft. International guidelines state that you should deorbit your spacecraft within 25 years. If you are rapidly iterating, then last-generation spacecraft quickly become a pain to operate, so deorbiting them sooner is ideal.

[//]: # (lifetime study)

##### Power
In terms of duty cycle, the fraction of time you will be in sun will range from ~50% (sun-synchronous, noon crossing), to ~100% (sun-synchronous dawn/dusk).
[//]: # (explain beta angle, eclipse fraction)

##### Thermal
[//]: # (explain beta angle, eclipse fraction)

#### Vibration
[//]: # (explain launch vibration, bubble wrapped cargo)

### Test Launches
A good solution for test launches is to go through the international space station. Currently [NanoRacks](http://nanoracks.com/products/smallsat-deployment/) offers a service which is relatively inexpensive. While the ISS orbit is not ideal for many missions (see above), the deployment altitude is ideal and launch vibration is fairly low because the satellite goes 'bubble-wrapped' as crew cargo.


## About the Authors
### Daniel Grossmann-Kavanagh
I started my career at [Planetary Resources](https://planetaryresources.com) as an intern. I was a sophomore at the school of Electrical Engineering at the University of Washington. I was lucky enough to join up as the third employee working directly with some fantastic engineers from JPL.

I caught the space bug, and focused the remainder of my degree in embedded systems. After graduationg, I worked at Planetary Resources on the A3 spacecraft - a 3U cubesat that exploded in the bountiful flames of the Antares rocket explosion.
[//]: # (https://youtu.be/BSr4hUcROwo?t=241)

I was fortunate to learn about system architecture, board design, board layout, board bring-up, embedded software, and system test.

Next, I wanted to learn about at-scale automated spacecraft operations, so I joined [Planet Labs](https://planet.com), an earth imaging startup in San Francisco. The "Mission 1" goal at Planet Labs was to image all of the land on earth every day, and make that data widely accessible to the general public.

As I write this, Planet has 100 satellites in a polar, sun-synchronous orbit. Once the fleet is fully phased around the orbital plane it will be capable of delivering on this mission.

Planet has leveraged the cubesat standard heavily, and has launched over 250 satellites (many of which have already deorbited). The company evangelizes the concept of "Agile Aerospace", a vertically integrated and highly iterative methodology for delivering value from space.
