Project Overview

CosmicStream Pro is an interactive web-based Disk Scheduling Simulator that visualizes classic algorithms like FCFS, SSTF, SCAN, C-SCAN, LOOK, and C-LOOK. It features a cosmic-themed UI with animated rocket navigation across disk tracks (planets), real-time telemetry, buffer health monitoring, and performance comparisons.

Users input a request queue (track numbers 0-199), initial head position, and select an algorithm to launch simulations with smooth rocket animations and seek distance calculations.

Key Features

Visual Galaxy Map: Planets represent disk tracks; rocket moves precisely to service requests without overlap.

Real-Time Metrics: Tracks total seek distance, buffer events, current track, and progress with a dynamic buffer fill bar.

Graph Visualization: Canvas-based buffer flow graph during seeks.

Algorithm Comparison: "COMPARE ALL" button ranks algorithms by minimal seek distance, highlighting the best.

Customizable Speed: Slider adjusts animation delay (250-1200ms).

Responsive Glassmorphism UI: Cosmic gradients, starfield background, and backdrop blur effects.

Usage

Enter comma-separated track requests (e.g., 98,183,37,122,14,124).

Set initial head position (default: 53).

Select scheduling algorithm from dropdown.

Click "LAUNCH ROCKET" to simulate; "COMPARE ALL" for benchmarks; "ABORT" to stop.

Default queue loads on start for quick testing.

Technologies
Frontend: Pure HTML5, CSS3 (radial gradients, backdrop-filter, animations), Canvas API for stars/graph.

JavaScript: Vanilla JS for all logic—sequence generation, rocket movement, buffer simulation, and DOM updates.

No Dependencies: Self-contained single HTML file, runs offline in any modern browser.

Algorithms Implemented
Algorithm	Description	Seek Logic
FCFS	First Come First Serve	Services in input order.
SSTF	Shortest Seek Time First	Always picks closest track.
SCAN	Elevator	Head to end (199), then reverse.
C-SCAN	Circular SCAN	Head to end, jumps to 0, repeats direction.
LOOK	Intelligent SCAN	Only to farthest request, no full traversal.
C-LOOK	Circular LOOK	Circular but only to farthest request.
File Structure
micro_project.html: Complete, standalone application (24KB).

Save as .html and open in browser. Resize handles responsive layout.

Controls Reference
Inputs: Queue (text), Head (number), Algo (select).

Buttons: LAUNCH ROCKET, COMPARE ALL, ABORT.

Telemetry: Active Algo, Current Track, Total Seek, Buffer Events, Progress.

Status: READY → ROUTE → COMPLETE/CRITICAL.

Example Simulation
Queue: 98,183,37,122,14,124 | Head: 53 | SSTF
Rocket visits closest tracks sequentially, buffer drops on long seeks, graph shows flow.

Ideal for OS education on disk scheduling optimization
