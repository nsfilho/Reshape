# Reshape

**A simple app to reshape your gcode files aimed for PCB milling.**

Features:

- Map your PCB working area using Z Probe for reshape Z axis.
- You can realign your double sided PCBs using X/Y drill roles.

What make this software different from any other:

1. You don't need a perfect align when you turn your PCB;
2. You can compensate your PCB Z axis easily by auto avoid drill holes;
3. Better re-mapping algorithm for compensate Z axis;

## Tips

As might of you know, PCB milling isn't a perfect process and different persons
have different preferences.

My personal preferences are:

- Kicad - **CAD** - For PCB design and generate the gerber file;
- Flatcam - **CAM** - To generate the basic gcode (for top and bottom faces, drill holes);
- Reshape - **Post-process** - For mapping the Z-Axis and realign gcode after turn the PCB;
- CNCjs - **Sender** - To send the gcode to the CNC;
- Grbl - **Controller** - The CNC controller;

IMHO, this is the best workflow for PCB milling, but you can use any other
software that you want.

Today my operation system is based on Arch Linux -- if you have any doubts about
how-to do something, please let me know.

## Design principles

- This project is based on [Tauri](https://tauri.app) and [React](https://reactjs.org/) as frameworks. The main reason for this choice is because you can use this software offline (and some workshop don't have internet near the machines).
- Flatcam is a great tool software, but the align process is a pain. This software is aimed to make this process easier.
- Remap gcode using one software (bCNC, Candle, CNCjs or other) plus another for realign X/Z could generate some errors.

## Contributing

If you would like to contribute, please fork the repository and use a feature branch. Pull requests are warmly welcome.

**Some important points for contributing:**

- **Front-end:** If you want to contribute with front-end, please feel free to do that;
- **Documentation:** If you want to improve the documentation, please let contribute for make this process more easily for all (including in the wiki and using videos);
- **Translation:** If you want to translate this software to your language, please let me know;
- **Post-process:** we need implement that for different controllers (like Marlin, LinuxCNC, TinyG, Mach3, etc);
- **Bug reports:** If you find a bug, please let me know;
- **Bug fixing:** please, feel free to fix the bug and send a pull request;

All contributions are welcome. If you contribute in any way, your name will be added to the contributors list. If you could, **please give a star for this project**, this will incentive me to continue this project.

If you are a company and want to support this project or donate in any way, please let me know.

## Developer notes

For you start the development environment, you need to have installed the requirements listed on [Tauri](https://tauri.app/v1/guides/getting-started/prerequisites).

After clone this project, you need to install the dependencies:

```bash
npm install
```

And for run the development environment:

```bash
npm run tauri dev
```

## Roadmap

- [ ] Implement the basic interface (without 3D Viewer);
- [ ] Implement Gcode parser;
- [ ] Algorithm for identify drill holes;
- [ ] Implement the Z-Axis mapping (avoiding drill holes);
- [ ] Reshape the Z-Axis;
- [ ] Implement the X/Y realign using drill holes center;
- [ ] Reshape the X/Y axis;
- [ ] Implement the post-process for different controllers;
- [ ] Implement the 3D Viewer for gcode;
- [ ] Implement a real time z-axis mapping viewer (3D);

## Screen sketches

[Main Screen](./docs/Reshape-main.png)
[Drill and Holes](./docs/Reshape-drill.png)
[Z-Axis Mapping](./docs/Reshape-map.png)
