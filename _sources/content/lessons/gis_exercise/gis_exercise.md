````{admonition} Assignment due date and formatting
:class: warning

Throughout this page you will find several Task blocks with metadata requests.
It is important to copy these into a text document (Word or otherwise), provide them with a header (e.g., *Task 1* for first task, etc.), and hand them in no later than 17:59 on the 11th of February 202.
Do so by uploading the compiled file to your personal Teams folder.

The filename should be formatted as:

```
Exercise-2_GIS_{first-name}-{surname}.{extension}
```

Herein the curly brackets and text between them are variables, in this case first and surnames.
As an example, using Kim Senger and saving the file as a Word file, the filename becomes:

```
Exercise-2_GIS_Kim-Senger.docx
```

````

# Exercise - where did he go?

Most phones and tablets have built-in GPS nowadays, allowing you to track your movements and trips.
Without doing anything, photos taken are often automatically geotagged with their locations, allowing you to easily retrace your steps based on a bunch of images alone!
In this exercise, we follow our enthusiastic snowmobile guru Kim Senger as he scooters throughout central Spitsbergen.
Kim recorded his whereabouts and routes with his phone, something we very much recommend you to do as well when you go out into the field or on field trips.

````{margin}
```{admonition} YAML configurations and the use of #
:class: note

Configuration files and lists often contain the special # character.
Also known as the hashtag sign, # is a common delimiter between values and comments that should be ignored by computers.
For instance, the *land*-key is followed by an explanation of what can be filled in, *e.g., Albert I Land -> perhaps use Toposvalbard data for this?*.
Always make sure there are spaces before and after the #.
Also make sure to end the key with a *:*.
```
````

````{margin}
```{admonition} Accessing layer information
:class: note
You can access layer information by clicking on the map, as this action presents you with the layer-specific information in the form of a “pop-up”.
Try this by clicking on one of the points of the imported GPS track.

Alternatively, you can access information by right-clicking the layer in the contents window, and then selecting the *Attribute Table* option.
This shows you all information that is available in table-form; it even allows you to sort the columns!
```
````

The recorded GPS tracks (so-called *.gpx* files) have been uploaded to:

```
AG222-2022 Microsoft Teams folder/Documents/General/Modules/ArcGIS Pro/Exercise Data/GPS Tracks
```

````{admonition} Task 1
:class: tip

1. Plot the GPS tracks in ArcGIS Pro to find out where Kim went.
2. Figure out the following metadata for each of the three tracks:

```yaml
land visited: # e.g., Albert I Land -> perhaps use Toposvalbard data for this?
island visited: # e.g., Bjørnøya -> perhaps use Toposvalbard data for this?
localities passed: # key locations passed on his way, e.g., Longyearbyen, Barentsburg
lowest elevation: # name locality and coordinates in EPSG:32633
highest elevation: # name locality and coordinates in EPSG:32633
time started: # name locality and coordinates in EPSG:32633
time stopped: # name locality and coordinates in EPSG:32633
```
````

### Does Svalbox have digital datasets in the area visited by Kim?

The Svalbox database lives both in a Petrel project as well as on the web -see [svalbox](www.svalbox.no/map).
The online component mainly consists of the Digital Model Database and geospatially placed data sets, e.g., seismic line locations, geological data, etc..
Let’s use the available map data to see whether the Svalbox database has any digital models and / or photos in the places visited by Kim, and, if so, whether these could have been acquired by Kim.

````{margin}
```{admonition} Zenodo
:class: note

Zenodo is a general-purpose open-access repository. It allows researchers to deposit research papers, data sets, research software...
All the DTM in Svalbox.no are uploaded there to assure free access to the data.
```
````

````{admonition} Task
:class: tip

1. Add the Svalbox.no database as a server within the ArcGIS Pro project
2. What is the outcrop model that Kim got closest too?
3. Provide the following metadata for the model.
4. Go to [www.doi.org](https://www.doi.org) to resolve the data_doi you obtained from the Svalbox.no database layer.
5. Download the digital terrain model of the outcrop from the Zenodo repository and plot it in your GIS project.
6. Visualise the 3D model on SketchFab, using the url construction below:

```url
https://sketchfab.com/3d-models/ + publ_sketchfab_id
```

```yaml
northing of centroid: # in EPSG:32633
easting of centroid: # in EPSG:32633
locality:
acq_date:
svalbox_dom_id:
publ_sketchfab_id:
publ_data_doi:
publ_date_archived:
model_description:
```


````

### Which geological units did Kim cross?

````{margin}
```{note}
Other than just importing the entire G_Geologi_Svalbard_S250_S750 layers into your map,
it is probably a better idea to import only the *Geological units / Geologiske enheter* from the *Geologi 1:250000 layer* group.
Then you can click on the map and get information about the layer.
```
````

As per the above, we can also check which geological units Kim crossed on his trips.
Make sure you have the NPI server available within your ArcGIS Pro project, as this will make your life a lot easier!

````{admonition} Task
:class: tip

1. Make a list of all *Formations* that Kim passed during his trips
2. Complete the list by adding *Groups* and *Lithologies*
````

### Bird's view

Kim is not the only one who likes to cruise around Svalbard.
Luckily, we have some artificial birds contributing to the Svalbox.no project by providing some spectacular 360 degree imagery.
One such view is available in Tempelfjorden.

````{margin}
```{note}
Make sure to include the images_360 layer from the Svalbox server in your project.
```
````

````{admonition} Task
:class: tip

1. Find the 360 degree image in Tempelfjorden and find the following metadata.
2. Visualise the 360 degree image using the tools provided in [](section:gis:360image-to-frame).
3. Which *Formations* are you looking at on the northern shore? Which on the southern?

```yaml
image_identifier:
image_acquisition_date:
svalbox_i0wpurl:
```

````

### Your own points of interest

Although there is already a lot of information available, it is perhaps equally important to be able to add your own data to the project.
[](section:gis:new_features) provides an overview with how to create a new *Point* layer.

````{admonition} Task
:class: tip

1. Pick three locations and create new Point for them.
2. Provide each Point with the following metadata:
3. Export the layer as a shapefile, and upload it to the Teams Folder

```yaml
Name: # a unique name to distinguish it
Elevation: # how high it is
Date: # i.e., when you would like to go there
Description: # i.e., why you would like to go there.
Owner: # i.e., who it is that would like to go there.
```

````
