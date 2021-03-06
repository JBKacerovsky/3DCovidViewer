# 3DCovidViewer

Building a Unity app that downloads and displays the covid19 database from http://ourworldindata.org

The goal of this "game"/app is to access the current Our World in Data COVID-19 database and to allow the user to select multiple country specific datasets, to display the data in 3D. 

This repo contains the most recent compiled WebGL build.

A working version of the Viewer can be accessed here: [3DCovidViewer](https://jbkacerovsky.github.io/3DCovidViewer/)

The Unity3D project building this Viewer can be accessed here: [current build](https://github.com/JBKacerovsky/3DCovidViewer_UnityProject)

With this app I wanted to explore using Unity3D to view and navigate the owid-covid dataset in 3D. This is still a very unfinished and experimental project. Mostly it is a toy project where I wanted to see whether I could use Unity3D in this way, to load publicly available datasets from an online source, parse the data in c#, and build an interface to display the data in 3D

The data (online .csv text file) is loaded during startup and parsed into a list based datastructure. Through a UI the user can select a country and 2 data dimensions and add the data to the current view. The data will be displayed as a sreies of spheres in the 3D environment. Each sphere (along the x axis) represents one day. The first selected data dimension will be displayed on the y-axis, as height of the spheres, while the second dimension defines the size of the spheres. Data-dimensions are displayed as realative height/size not as absolute values (to deal with the extremely large range of values). The scale is defined by the first dataset added to thee current view. Two text boxes allow the user to adjust the scale for the next series to be added. 

Camera Rotation (mouse drag to rotate, scroll to zoom in/out) can be unlocked/locked with a UI button. Camera panning (mouse click and drag) an be unlocked/locked with a UI button.

The WebGL implementation was built using the [better-unity-webgl-template](https://github.com/greggman/better-unity-webgl-template), which worked amazingly well for me. 


# Data Source
[ourworldindata.org](https://ourworldindata.org/coronavirus) does amazing work compiling this data daily and providing it [free](https://github.com/owid/covid-19-data/tree/master/public/data) to use. They offer a number of fantastic 2D interactive charts on their website. 

> Max Roser, Hannah Ritchie, Esteban Ortiz-Ospina and Joe Hasell (2020) - "Coronavirus Pandemic (COVID-19)". Published online at OurWorldInData.org. Retrieved from: '[https://ourworldindata.org/coronavirus](https://ourworldindata.org/coronavirus)' [Online Resource] 
