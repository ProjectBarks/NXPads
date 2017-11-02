# NXPads 

A minecraft plugin for Bukkit servers that allows for two pads to be placed and users to then be sent to the other pad smoothly. *This project is **outdated** and most likely will not execute on a modern minecraft server. However, this was one my first projects and reflects my progression as a developer of and would love to share with everyone.* 

### Commands

| Command           | Description                              |
| ----------------- | ---------------------------------------- |
| /pads pos1        | Sets the position of the launch pad that the player will be sent from. |
| /pads pos2        | Sets the position of target pad that the player will land at. |
| /pads save        | Takes the two positions set by the user and saves it perminantly |
| /pads delete [id] | Removes a saved pad                      |
| /pads list        | Lists all pads and their according ids   |

### Equation

In order to properly calculate the players projection to the platform an equation was drafted from minecraft's sourcecode to proply send one user to another side of the map. The equation that was created is represented as following: 

<p align="center">
<img src="https://latex.codecogs.com/gif.latex?Vector%20%3D%20%5Cbegin%7BBmatrix%7D%20x%3D%28x_%7Bt%7D-x_%7Bu%7D%29%5Cfrac%7B%28100/91%29%5E%7B10%7D%7D%7B20%7D%20%5C%5C%20y%3D3.92%281%20-%200.98%5E%7B10%7D%29%20&plus;%20%5Cfrac%7BY_%7Bt%7D%20-%20Y_%7Bu%7D%7D%7B20%7D%20%5C%5C%20z%3D%28z_%7Bt%7D-z_%7Bu%7D%29%5Cfrac%7B%28100/91%29%5E%7B10%7D%7D%7B20%7D%20%5Cend%7BBmatrix%7D">
</p>

Please feel free to use this in your own project as well. The java implementation is available in the `getVectorToTarget` method in [this](/src/main/java/com/projectbarks/targetpads/Commands.java) class.
