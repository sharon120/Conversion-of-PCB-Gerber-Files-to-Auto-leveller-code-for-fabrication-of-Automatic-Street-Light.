# Conversion-of-PCB-Gerber-Files-to-Auto-leveller-code-for-fabrication-of-Automatic-Street-Light.
## Exp 9: Conversion of PCB Gerber Files to CNC G-Code and G Code into Auto leveller code for Precision Engraving, Drilling, and Cutting of Automatic Street Light Control Circuits.

## AIM:
To convert PCB Gerber files of an automatic street light control circuit into CNC-compatible G-Code, and G-Code into Auto leveller Code to ensure precise engraving, drilling, and cutting operations during PCB manufacturing using a CNC machine.
## EQUIPMENT REQUIRED:
●	Hardware: Personal Computer (PC)<br>
●	Software: Copper CAM, Auto leveller<br>
## PROCEDURE:
### Copper CAM
1.	Open your Gerber file (File → Open → New circuit)<br>
2.	Open your Drill file (File → Open → Drill)<br>
3.	Match the drill file and engraving file if not matched<br>
4.	Right click the pad and set define as pad and then Right click and select edit all identical pads as set the drill size as 0.8mm,1mm.<br>
5.	Open your Cutting file (File → Open → Additional Layer and load your cutting file<br>
6.	Go to file/Orgin and set x=0,y=0<br>
7.	Go to file/offset and select the option shift manually<br>
8.	Select the layer 6 and move the cutting file and set the border<br>
9.	Go to parameter/ tool library and check the identifaication and specification<br>
10.	Go to parameter/selected tool and check the engraving tool, cutting tool and drill tool<br>
11.	Go to machine/ Contours/calculate Contours<br>
12.	Go to machine/mill and select engraving you will get the g code,similarly for Drill and cut.<br>
13.	Save the G code<br>
### Auto leveller
1.Open the Autoleveller software<br>
2. Select the software option as Mach3 <br>
3. Load the G Code - Click “Browse for G Code” button and open your Engraving G-Code.<br>
4. After loading G-Code below a window will open. In that Select Unit “millimeters”<br>
5. Create level code and the save the code<br>
6. Remove the unwanted portion from your Auto Levelled G-Code.<br>
7. Add few lines in the code and save the file<br>
8. Follow this same procedure for remaining all G-codes ( Drill and cut).<br>
9.Autolevelling should be done for only engraving file.<br>
## THEORY:
In the process of PCB prototyping using CNC machines, converting Gerber files into G-Code is a crucial step. Gerber files, which are generated from PCB design software such as Eagle, KiCad, or Altium, contain all the essential data related to copper traces, drill holes, and board outlines. These files are loaded into CopperCAM, a specialized software tool used to convert Gerber data into machine-readable G-Code. G-Code is the standard language for CNC machines, containing instructions for tool paths, feed rates, and operations like drilling, engraving, and cutting. CopperCAM allows users to define tool parameters and optimize machining paths for precise and efficient milling. It separates different PCB layers (top, bottom, drill, outline) and converts each into a suitable toolpath, which is then saved as G-Code.
Once the G-Code is generated, it is essential to ensure that the CNC engraving bit maintains consistent depth across the entire surface of the copper-clad board, as even minor surface irregularities can affect trace quality. To overcome this, AutoLeveller software is used. This tool takes the original G-Code and enhances it by adding auto-leveling commands, which probe various points on the PCB surface to measure height differences. Based on these measurements, it adjusts the Z-axis movements dynamically during machining, ensuring that the engraving depth remains constant. This results in high precision and better-quality PCB fabrication. By integrating CopperCAM and AutoLeveller in the workflow, the process from Gerber file to fully auto-leveled CNC-ready code becomes streamlined, accurate, and suitable for creating reliable circuit boards such as the automatic street light control system.
## EXPECTED OUTPUT:
### Copper CAM
### Engraving G Code

### Drill G Code

### Cut G Code

## Auto leveller

### Engraving G Code

### Drill G code

### Cut G Code 

## RESULT:
Thus, the Gerber files of the automatic street light control circuit were successfully converted into CNC G-Code and G-Code into Auto leveller Code for accurate and high-quality PCB engraving, drilling, and cutting using the CNC machine.
