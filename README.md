# Magnetic Field Art & Percolation Simulation
## Project Description
This web-based application is an interactive art and science tool that simulates a 2D grid of interacting bar magnets. The project visualizes the dynamic, self-organizing behavior of these magnets as they attempt to align with their neighbors. It is a form of digital art rooted in the principles of statistical physics, specifically percolation theory and phase transitions.
The simulation features two key components: a visual representation of the magnetic field and an analytical graph that tracks the distribution of connected clusters. This allows users to not only create mesmerizing visual art but also to observe how macroscopic patterns emerge from microscopic interactions.
## How to Use
Simply open the [index.html](index.html) file in a modern web browser to run the simulation. No installation or server is required.
### Controls
 * Magnetic Field Strength: Adjusts the influence each magnet has on its neighbors. Higher values lead to stronger interactions and faster pattern formation.
 * Initial North Orientation Probability: Sets the likelihood of a magnet starting in a northern-facing direction. A value of 0.5 creates a random mix, while 1.0 or 0.0 creates a completely uniform initial state.
 * Grid Size: Changes the number of magnets on the grid, from a small 10x10 to a large 100x100.
 * Show Magnet Bars: Toggles the display of the white lines that indicate each magnet's specific orientation.
 * Show Binarized Plot & Colors:
   * Plot: Switches the graph from a log-log distribution of cluster sizes to a simple bar chart showing the total count of magnets in the north, south, and diagonal categories.
   * Colors: Changes the main simulation display to a solid red for northern magnets and solid blue for southern magnets, removing the color gradient.
 * Pause/Resume Simulation: Halts or restarts the simulation's dynamic updates.
 * Reset Simulation: Initializes the grid with a new, random set of magnet orientations based on the current slider settings.
## Technical Details
The simulation is built using vanilla HTML, CSS, and JavaScript, leveraging the `canvas` element for high-performance rendering.
 * Simulation Core: A custom algorithm iterates through each magnet, calculating the net magnetic field from its 8 nearest neighbors. It then applies a rotational force to move the magnet toward alignment with the net field. Damping is used to prevent the system from oscillating indefinitely.
 * Connected Component Analysis: The findConnectedComponents() function uses a Breadth-First Search (BFS) or flood-fill algorithm to identify contiguous clusters of magnets with similar orientations.
 * Plotting: The two-dimensional canvas is used to render both the main simulation grid and the analytical graph. The log-log plot displays the power-law distribution often found in critical phenomena, while the binarized plot offers a simple count for easy comparison.
## License
This project is licensed under the MIT License. See the LICENSE file for more information.
