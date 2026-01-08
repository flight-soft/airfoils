# Airfoils Repository

This repository contains over 1600 airfoils for fixed wing aircraft. Some of these are standard, like the *Clark-Y* airfoil.  Yet, others are experimental or historical, like the *Eiffel 10* used by the 1903 Wright Flyer.  And some are specifically for model aircraft, such as *S4094* used by RC sailplanes. 

The airfoil files are in Selig text format, which starts with the name of the airfoil followed by two columns of (x, y) coordinates. The coordinates have been normalized to x = 0 to 1 and y  = -1 to +1.  Files may also contain comments where the line starts with the # symbol. The format was developed by professor Selig at the Department of Aerospace Engineering at the University of Illinois. For more information visit the [UIUC website](https://m-selig.ae.illinois.edu/ads/coord_database.html).

**Files**
GitHub will only display the first 1000 files. For a complete directory listing see [files.json](https://cdn.jsdelivr.net/gh/flight-soft/airfoils@main/files.json)

Airfoil data files can be fetched using JavaScript by using the CDN address:

    const url = "https://cdn.jsdelivr.net/gh/flight-soft/airfoils@main";
    const path = "/dat/";
    const name = "clarky";
    const ext = ".dat";

    fetch(url + path + name + ext)
      .then(response => response.text())
      .then(text => {
    	  console.log(text);
    	  // parse the airfoil data and display
      })
      .catch(error => console.error(error.message));

*Coming soon ...*
Eventually there will be a web application that will allow you to search, view, and export airfoil data in different formats.
