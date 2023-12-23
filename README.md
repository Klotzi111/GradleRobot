# GradleRobot
This repo is a template for creating robots for [RoboCode](https://github.com/robo-code/robocode) using Gradle.  
This makes it easy to use any IDE to code Robots.  

You get all the benefits from using an IDE and can easily export a jar file that [RoboCode](https://github.com/robo-code/robocode) can import.

This repo comes with an example robot implementation class so you can get started immediately.

## How to Use

### Setup
- Clone this repository
- [Change Robot/Project Name](#change-robotproject-name)

### Change and Export
- Change the robot code (Open this repo as a Gradle project in your IDE)
- [Export your Robot as a jar file](#export-a-jar-file-for-robocode) and import it in [RoboCode](https://github.com/robo-code/robocode)


## Change Robot/Project Name
Because you want your robot to be special and non-generic you want to change the name of your Robot.

For this a simple java program is contained in this repo which renames your project, namespaces and classes.  

*Before running the command it is recommended to close your IDE completely (unloading the project from you IDE might be enough).*  
The program can be run via the commandline with the following command (cd into the repo folder first):  

```sh
java -jar RenameProject.jar <YOUR_NEW_PACKAGE_NAME>.<YOUR_NEW_PROJECT_NAME>
```

Replace `<YOUR_NEW_PACKAGE_NAME>` in the command above with a package name for your robot class. If you do not know what that means then just use the same as for `<YOUR_NEW_PROJECT_NAME>`.  
Replace `<YOUR_NEW_PROJECT_NAME>` in the command above with your new project name.  
*Keep the `.` between these two placeholders.*  

## Export a Jar File for RoboCode
To generate/export a jar file that can be imported into [RoboCode](https://github.com/robo-code/robocode) use the `shadowJar` Gradle task.  
This task can be run via the commandline with the following command (cd into the repo folder first):  

```sh
./gradle shadowJar
```

The exported jar file can be found in `build/libs/`.  