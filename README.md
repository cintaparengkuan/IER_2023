# Design modifications of the Portable Hand Trainer to Increase the Longevity and Minimize Stress Concentration on the Flexible Shell

This repository contains the code, data, and results for the project on optimizing shell designs using Finite Element Analysis (FEA). The project aims to investigate design modifications to minimize stress concentrations and improve the durability of shells under static and fatigue loading conditions.

## Getting Started

These instructions will give you a copy of the project up and running on your local machine for development and testing purposes. See deployment
for notes on deploying the project on a live system. 

First off, I would to recommend to clear out 20 GB. You are going to need that space, sorry :)
If by any chance you don't have this luxury, please make use of the on-campus computers.

### Prerequisites

Requirements for the software and other tools to build, test and push 
- [SolidWorks](https://software.tudelft.nl/498/)
- [EduVPN](https://tudelft.eduvpn.nl)

### Installing
1. Make sure that you have activated EduVPN first, as the SolidWorks installation would require using this VPN in order to both install and run the software.
2. Download the SolidWorksSetup file from the software portal: software.tudelft.nl or via the link provided above.
3. Start the installation by clicking on the SolidWorksSetup file.
4. Once the Installation Manager is running, select the option Install on this computer and click the Next arrow.
5. Input SOLIDWORKS CAD serial number under 3D Design, you can find this number [here](https://software.tudelft.nl/498/) under the installation tab.
6. Check also the add-ins that you need with the same serial number and leave other fields blank, click next. You can find the serial number on the software portal.
The Installation Manager will now check and verify you have the system requirements to run SOLIDWORKS.
7. Once your system has been checked, you will be taken to a summary screen displaying all of the products you will be
installing. Check the box marking that you accept our terms and conditions and click Download and Install.
8. Use the right licence server, you can find it [here](https://software.tudelft.nl/498/) under the installation tab.
9. Once the installation is complete, click Finish to close the Installation Manager.
10. 
**Note: This is for if you have a student licence only. If you don't have this, you can access it via the on-campus desktops or [weblogin](https://weblogin.tudelft.nl).**

## Running the tests
**First make sure that you have are running EduVPN. If you are using weblogin or an on-campus desktop, then please skip this step.**

1. After running SolidWorks, open one of the models.
2. Click on either "New Study" or on "Simulation" and then "New Study"

### Static Loading Test
1. On the right hand side of the screen, select "Static" and then click the green checkmark.
2. Underneath "Static (-Default-), right-click the model and make sure that you have the same material as mentioned in the paper by checking the values and close the material tab.
3. Underneath "Static (-Default-), click the dropdown arrow and right-click one of the two parts that need to be excluded from the analysis. You can figure out which one it is by first clicking on that part.
4. Next, click "Exclude from Analysis" and do this for the other part as well. Please note that you cannot do these two at the same time.
5. Right-click "Fixtures" and click "Fixed Geometry". Select the backside of the shell, as shown in the paper and click the green checkmark.
6. Now right-click "External Loads" and select "Force...". Select the side parts of the shell with the arrows of the force facing inwards, just like shown in the paper.
7. For the force, select 15 N and click on the green checkmark.
8. Right-click "Mesh" and click "Create Mesh"
9. do not move the mesh density arrow and click green checkmark. The this might take a while, depending on which model you have chosen.
10. Somewhere on the same bar as "New Study", you can click "Run this Study".
11. Now you should be able to interchange between the various results underneath the "Results" dropdown.
12. If you would like to see the exact numbers of for instance the maximum stress, on the same bar as "Run this Study" you can find "Report".
13. This would create a Word document that represents the exact numbers.

### Fatigue Loading Test
1. For the fatigue loading test, make sure to have already run the static loading test.
2. Click "New Study" and select "Fatigue", make sure that you have selected "constant amplitude events with defined cycles" and then the green checkmark.
3. Right-click "Loading (-Constant Amplitude) and only change the number of cycles to 3000
4. Now you should see a dropdown arrow next to the name of the model you have chosen, make sure that the parts that you have excluded before, are excluded once again.
5. Right-click the name of the model you have chosen and click "Apply Fatigue Data to All Bodies". Here you can select your Fatigue SN Curve.
6. Select Derive from material Elastic Modulus Based on ASME Carbon Steel curves and click on apply and then close.
7. Now you can run this study, please keep in mind that this also going to take a while.
8. If you get an error asking to rerun it, click yes.
9. Now you should have the results from this test. If you would like to see the exact numbers from the result, you can click "Report" and this should create a Word document.


## Built With

  - [SolidWorks](https://software.tudelft.nl/498/) - Used for CAD modeling and FEA simulations
  - [EduVPN](https://www.eduvpn.org/client-apps/) - Used run SolidWorks and to secure a private network connection during data transfer and collaboration

## Repository Contents
- Shell_Large, Shell_Medium, Shell_Small: These directories contain models for three different sizes: small, medium and large. Each size includes three variations:
    - Original model
    - Rib structure model
    - TPU material model
 - For the SolidWorks part, please select the SLDPRT file.
 - The docx file is a report that shows the exact numbers of the tests run by me.
 - All the other files are files that were made when conducting the tests, make sure to also download these to conduct the tests.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [Semantic Versioning](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/PurpleBooth/a-good-readme-template/tags).

## Authors

  - **Cinta Parengkuan** 

## License

This project is licensed under the [CC0 1.0 Universal](LICENSE.md) Creative Commons License - see the [LICENSE.md](LICENSE.md) file for
details
