Tank Cascade Simulator

An interactive canvas-based physics simulation modeling ancient Sri Lankan reservoir engineering —
built with vanilla JavaScript, no libraries or frameworks.

Live demo: https://nethara20.github.io/tank-cascade-simulator/


What it does

Drag on empty canvas to draw a reservoir — the size of the drag sets its capacity
Click one tank, then a lower one to open a channel between them (uphill connections and
loops are rejected)
Drag an existing tank to reposition it
Click a channel's valve icon to close it
Scroll while a tank is selected to resize it
Toggle rain to fill the system and watch it cascade downhill
A live telemetry panel shows real-time capacity, volume, fill %, and inflow/outflow rate for
the selected tank


The physics

This isn't just an animation — it's a small real-time simulation:

Outflow rate from a tank scales with √(fill level), similar in shape to Torricelli's law
(fuller tanks push harder)
Every channel has a maximum flow rate, which caps outflow regardless of pressure — modeling the
bisokotuwa, a valve-pit design used in Sri Lankan reservoirs starting around 300 CE to
prevent outflow pressure from damaging the embankment
Tanks with no outlet simply hold water up to capacity, then visibly "spill" (a pulsing ring) once
full during rain — a stand-in for a real spillway


Tech stack

HTML5 Canvas (2D context) for all rendering — no SVG, no DOM-per-tank
Vanilla JavaScript — pointer events for mouse + touch, requestAnimationFrame simulation loop
No dependencies, no build step


Running locally

Just open index.html in a browser. Everything — rendering, physics, and interaction — runs
client-side with no server required.


Part of a series
This is the second of three connected projects exploring the same theme:

Portfolio — the site this links back to
Tank Cascade Simulator (this repo)
Heritage Reservoir Archive — a
PHP/MySQL catalog of real ancient Sri Lankan reservoirs


Author
Nethara Bashudi — LinkedIn · netharabashudi@gmail.com
