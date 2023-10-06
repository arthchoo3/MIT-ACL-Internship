# MIT-ACL-Internship
In this repository are descriptions and files of the work I did at the MIT Aerospace Controls Lab in the summer of 2023.

# Overarching Research Topic
All of our research was built around relative pose estimation for multi-agent robotics using ultrawideband (UWB) sensors. As opposed to Global Positioning Systems (GPS) or Local Positioning Systems (LPS) which have radio antennas mounted in known fixed positions, the relative pose estimation would use only the communication between agents to determine their positions relative to each other.

## **Drone Antenna Holder:**
  The Drone Antenna Holder is a two-piece clamp that is attached to the propeller guard of a hexacopter to hold radio antennas.
The two parts of the antenna holder are held together by two zip ties.
![IMG-8882](https://github.com/arthchoo3/MIT-ACL-Internship/assets/140445967/b629756d-b484-46dc-9cdf-456ed7d329ec)


## **Drone Sensor Mount:**
  The Drone Sensor Holder mounts internally in the hexacopter and holds six NoopLoop Ultrawideband (UWB) sensors. These sensors connect via SMA cables to the antennas mounted on the propeller guards. It also contains a rectangular slot to hold USB hubs into which the UWB sensors plug.
 ![IMG-8887](https://github.com/arthchoo3/MIT-ACL-Internship/assets/140445967/9bb806f1-7c85-4d7d-87de-daf3ea0c2be2)
![IMG-8888](https://github.com/arthchoo3/MIT-ACL-Internship/assets/140445967/94926381-06a3-444e-ae3e-2211aeb7508e)

## **Drone Spacer:**
  The Drone Spacer is designed to separate the top and bottom carbon fiber plates in the drone so there is space for the circuitry.
![IMG-8957](https://github.com/arthchoo3/MIT-ACL-Internship/assets/140445967/cc11ef52-8fb0-4f10-a771-4516c6f4443c)

## **Cube Experiment**
  The Motion Capture (MoCap) space in the ACL only permits the flight of drones up to a certain size due to safety regulations. However, we aimed to test our research on large-scale drones. To simulate the positioning of the UWB sensors on a larger drone, we built PVC cubes on which we mounted the UWB sensors. The positioning of the UWB sensors on these PVC cubes exactly matched that of a drone that our supervisor tested in an outdoor flight space in California--allowing us to have data from true flight conditions as well as high-precision MoCap data.
![IMG-8990](https://github.com/arthchoo3/MIT-ACL-Internship/assets/140445967/e8649644-f419-46bc-b488-be12dd49b182)

## **PVC Turtlebot Drones**
  Adding the UWB sensors to the drones made them heavier than normal thus decreasing their flight time. In order to collect larger amounts of continuous data, we build PVC drones the exact size of our drones to simulate the UWB's relative positions. Placing these PVC drones on TurtleBots allowed us to "fly" for longer and collect more continuous data. It also eliminated the risk of drone and sensor damage due to a drone crash. We also built one of the PVC drones to be higher off the ground to simulate altitude variance.
![IMG-9078](https://github.com/arthchoo3/MIT-ACL-Internship/assets/140445967/a206d6fc-a32a-4249-95a1-e975d27f012c)

## **Artificial Neural Network for UWB Orientation Bias Correction**
  Due to the torus-shaped propagation pattern of the UWB radio waves, the sensors' relative orientations affect the accuracy of their measurements. Objects on the plane perpendicular to the antennas at the antennas' midpoints are perceived closer than objects that are above or below the antennas. To correct for this orientation bias, we began working on a neural network that could take into consideration the antennas' relative orientations and calculate the actual distance between them. To collect data for neural network training, we built two platforms actuated by servo motors which sat on two turtlebots. This allowed us to collect data at several distances and orientations without being present to manually adjust the antennas. We intended to use this data, in conjunction with mocap data (which is accepted as ground truth due to its high accuracy), to train the neural network. We were working on this project when the summer ended so I was not able to continue my work on the project beyond the aforementioned. 
