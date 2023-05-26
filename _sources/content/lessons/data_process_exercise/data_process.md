# Exercise 4 - Process and analyze your data
```{admonition} Deadline
:class: note
Please complete this exercise **by the end of SESSION 5 by Friday 23rd of June, 2023**.
```

After collecting data using UAV in the field, it's time to process it by creating a 3D model and analyzing it. In this exercise, you'll learn how to:
- Structure the field data in your computer.
- Use Agisoft Metashape to digitalize outcrops.
- Discover and implement basic tips and tricks for data acquisition in the field.
- Measure your models.
- Annotate and interpret your 3D model using Metashape GUI.
- Upload the 3D model to Sketchfab and export an orthomosaic and digital elevation model (DEM).

```{admonition} Support
:class: warning
Please note that we only provide feedback and support for the **participants of the Geo-MOD course**.
```

## 1. Data and project structure
After coming back from the field, the first step is to download and organize the images collected during the acquisition campaign. 

```{admonition} Do it asap!
:class: tip
It's important to download and organize your images as soon as possible. This not only creates a backup of your data but also allows you to sort them by flights and outcrops while the flight survey is still fresh in your memory. Otherwise, it can be easy to forget.
```

It's crucial to utilize a standardized project environment when creating a project to ensure automated processing and archiving. Keep this in mind.

```{admonition} Standardised project environment
:class: note
Our recommendation is to utilize the standardized project environment that is outlined in the [Metashape tutorial](https://unisvalbard.github.io/Geo-SfM/content/lessons/l1/tutorial#a-standardised-project-environment).
```

````{margin} Network processing

For those present at UNIS and following this tutorial as part of the Geo-MOD Course, please enable network processing.
Proceed to *Tools* in the menu bar and click on *Preferences...*.
Then proceed to *Network* and check the *Enable network processing* setting.

The following parameters should be used to connect to the server:

Host name:
```
svalbox
```
Root:
```
\\svalbox\metashape-processing$
```
Port number:
```
5840
```

Whenever you want to use the network for processing, you will have to place your project within the *Root* folder specified above.
````

## 2. Process your digital outcrop model (DOM)
For processing your digital outcrop model, we suggest utilizing the structure-from-motion [Metashape tutorial](https://unisvalbard.github.io/Geo-SfM/content/lessons/l1/tutorial#metashape-tutorial) available on the Geo-SfM tutorial pages.


```{admonition} Use the processing network!
:class: note

Make sure to submit your processing requests to the network!
Else processing may take forever!
```

## 3. Measure your 3D model
Since your digital model is scaled 1:1 with the actual outcrop, we can utilize it for measuring purposes.

### Calculate bulk density
Metashape provides a built-in feature to determine a model's volume (*Tools/Mesh/Measure Area and Volume...*).

```{admonition} Metashape volume measurement
:class: note
Be careful, though, as this calculates the total volume of *all* closed surfaces/meshes in your project.
```

The calculated volume is furthermore given in m3 - so make sure to apply the correct conversion.

## 4. Annotate and interpret the 3D model
You can find a description of the tools used for interpreting and annotating digital outcrop models in the [geomodelling tutorial](https://unisvalbard.github.io/Geo-SfM/content/lessons/l5/geomodel_tutorial.html).

## 5. Export and publish your model
````{margin} 
```{admonition} Sketchfab
:class: note

Sketchfab is an online platform that allows uploading 3D models. While it doesn't keep the original quality of the model due to web limitations, it is an excellent way to share and visualize your models online.
```
````

Finalise the outcrop metadata form and discuss it with the course responsible. Remember to include the SketchFab ID, which can only be obtained after the submission has been quality controlled and the model has been uploaded to [SketchFab](https://sketchfab.com/).

You can upload your model to Sketchfab directly from Agisoft Metashape or throught the webpage. In case you choose the second option, you have to export the _Mesh_ and _Texture_ files from your project and upload them manually online.

## 6. Import the DEM to a GIS project
You can import the DEM you created to a GIS project.

Follow the tutorial on _Importing a digital terrain model_ a the [AG-222 Compendium - GIS 101](https://unisvalbard.github.io/AG222/content/lessons/gis/gis.html).

```{admonition} 2D representation
:class: note

Keep in mind that both  ArcGIS and QGIS allow you import the DEM and associated data fields. However, and while the elevation data is preserved, the visualizaiton will be in 2D.
```