<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" /></a>

### About Geo-MOD
[Geo-MOD](https://unisvalbard.github.io/Geo-MOD/landing-page.html) is a module to teach students how to collect and process AUV-based field data for geoscientific use using advanced techniques. The course is designed to be interactive and openly accessible to everyone.

The course is complemented by different modules to cover each stage of the UAV photogrammetry workflow. [Geo-UAV](https://unisvalbard.github.io/Geo-UAV/landing-page.html), is a tool for UAV-based data acquisition in the field, [Geo-SfM](https://unisvalbard.github.io/Geo-SfM/landing-page.html) is a tool for acquisition, processing and analysis of structure-from-motion photogrammetry data in the geosciences and [AG-222 Compendium](https://unisvalbard.github.io/AG222/landing-page.html) is a tool that provides different resources for analyzing the data and publish your research.

The reference work is primarily developed as a class-room aid. Best practices and tutorials are based on the experience acquired as part of the [Svalbox project](https://svalbox.no), which aims to digitize as many outcrops as possible in Svalbard (Norwegian Arctic).

### Contribute or improve the resource
```{admonition} Under construction
Geo-MOD is still in development, with additional tutorials and how-tos added continously to keep the work up-to-date with recent developments and evolving best practices.
```

Notice some unclear sections? A typo in the text? Want to add a cool tutorial or how-to on processing? Get in touch and let's make thing happen!

### Compile it

The minimal Python environment to compile this tutorial can be created as follows:

```
mamba env create --file geomod_environment.yaml
```

Subsequently, one may build the pages by using the following command from the root folder:

```
jupyter book build .
```


### Acknowledgements and licensing
Geo-MOD is implemented through Jupyter Book and the Executable Book Project.
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.