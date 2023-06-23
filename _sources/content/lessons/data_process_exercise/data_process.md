# Exercise 4 - Process and analyze your data
````{admonition} Deliverable
- Brief animation of your model recorded in Agisoft Metashape
- Export Model/Mesh with textures; orthomosaic
- Export processing report
- Upload the model to Sketchfab from Agisoft Metashape using the API key
- Annotate and export features/shapes
- Import orthomosaic and shapes in GIS and embed the Sketchfab model
- Fill out metadata form

```{admonition} Don't use PowerPoint
:class: warning

The use of PowerPoint and screenshots for presenting your data is not allowed.
```
````

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

````{admonition} Standardised project environment
:class: note
Our recommendation is to utilize the standardized project environment that is outlined in the [Metashape tutorial](https://unisvalbard.github.io/Geo-SfM/content/lessons/l1/tutorial#a-standardised-project-environment).

```
{project_directory} (The folder with all files related to this project)
|   overview_img.{ext}
|   description.txt
├───config (where you place your configuration files)
        {cfg_0001}.yml
        {cfg_0002}.yml
        ...
├───data (where you unzipped the files to)
├───────f0001 (The folder with images acquired on the first flight)
|           {img_0001}.{ext}
|           {img_0002}.{ext}
|           ...
├───────f0002 (The folder with images acquired on the second flight)
|           {img_0001}.{ext}
|           {img_0002}.{ext}
|           ...
|       ...
├───────f9999 (The folder with images acquired on the last flight)
|           {img_0001}.{ext}
|           {img_0002}.{ext}
|           ...
├───────gcps
|           (We'll get back to this in a later session)
├───────GNSS
|           (We'll get back to this in a later session)
├───export (where you place export models and files to)
        ...
└───metashape (This is where you save your Agisoft Metashape projects to)
        {metashape_project_name}.psx
        .{metashape_project_name}.files
        {metashape_project_name}_processing_report.pdf
        (optionally: {metashape_project_name}.log)
```
````

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
Finalise the outcrop metadata form and discuss it with the course responsible. Remember to include the SketchFab ID, which can only be obtained after the submission has been quality controlled and the model has been uploaded to [SketchFab](https://unisvalbard.github.io/Geo-SfM/content/lessons/l6/sketchfab.html).

```Metadata form
acq_camera_lens: # mm
acq_camera_model: 
acq_date:  # STRING DD.MM.YYYY
acq_georeferencing:  # STRING, pick: built-in GPS, dGPS, GCPs, GCPs/GPS, GCPs/dGPS
comments: 
data_author:
  - name: 
  affiliation: 
  orcid: 
data_model_crs_epsg: # INT EPSG number of model CRS
data_model_file_name:  # STRING with model file name and obj extension.
data_project_path:
data_type: 
#
keywords:  # Separated by ;. Last item without.
location_altitude:  # altitude used for hand sample models
location_easting:  # easting used for hand sample models
location_island: # Island the outcrop is found on PICK: Hopen / Spitsbergen / Kong Karls Land / Edgeøya / Barentsøya / Tusenøyane / Nordaustlandet / Kvitøya / Prins Karls Forland / Bjørnøya / Other
location_land:   # PICK Albert I Land / Andrée Land / Bünsow Land / Dickson Land / Haakon VII Land / Heer Land / James I Land / Nathorst Land / Nordenskiöld Land / Ny-Friesland / Olav V Land / Oscar II Land / Sabine Land / Sørkapp Land / Torell Land / Wedel Jarlsberg Land / Gustav Adolf Land / Gustav V Land / Orvin Land
location_locality: 
location_northing:  # northing used for hand sample models
#
proc_alignment_accuracy: Highest
proc_camera_stations: 
proc_camera_total_error: 
proc_coverage_area: # kmÂ²
proc_dc_filter_conf_min:  # changed from proc_dense_cloud_confidence_minimum
proc_dem_point_density: # points/mÂ²
proc_dem_resolution: # m/pix
proc_depth_map_accuracy: 
proc_flying_altitude: # m
proc_georeferencing_count:  # number of gcps used
proc_georeferencing_crs:  # INTEGER, epsg CRS number
proc_georeferencing_type:  # STRING, e.g., Aruco or Agisoft markers, also indicate marker version.
proc_ground_resolution: # m/pix
proc_mesh_filter_con_comp: 
proc_sc_filter_proj_acc: 
proc_sc_filter_recon_uncert: 
proc_sc_filter_reproj_error: 
proc_software: Agisoft Metashape
proc_software_version:
proc_volume:  # volume of the digitized handsample in cm3 / digitalized outcrop model in km3
#
publ_sketchfab_id: 
publ_v3geo_model: 
```

## 6. Import the DEM to a GIS project
You can import the DEM you created to a GIS project.

Follow the tutorial on _Importing a digital terrain model_ a the [AG-222 Compendium - GIS 101](https://unisvalbard.github.io/AG222/content/lessons/gis/gis.html).

```{admonition} 2D representation
:class: note

Keep in mind that both  ArcGIS and QGIS allow you import the DEM and associated data fields. However, and while the elevation data is preserved, the visualizaiton will be in 2D.
```