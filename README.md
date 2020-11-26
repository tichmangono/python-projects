# python-projects
python project portfolio to implement my ideas


# COVID-19 Testing Pipeline - Helper Functions
#Data on locations and volumes of testing in the US

print("Importing Requirements...")
#!pip install haversine
#!pip install geoplot
from haversine import haversine, Unit
import pandas as pd
import geopandas as gpd
import numpy as np
import urllib
import json
import requests
import datetime as dt
import ast
import facets_overview as fo
import pandas_profiling as pp
import bs4 as bs
import matplotlib.pyplot as plt
import missingno as mno
import pandas_profiling as prof
from math import cos, sin, asin, sqrt, radians
import matplotlib.pyplot as plt
import os
import pickle
#import descartes

from shapely import wkt

def make_folder_structure():
    print("Making/checking folder structure...")
    # Declare folders or make them if they do not exist
    ROOT = "./"
    RES_LATEST = os.path.join(ROOT, "results", "latest")
    RES_ARCHIVE = os.path.join(ROOT, "results", "archive") 
    SRC_DOCS = os.path.join(ROOT, "source", "docs")
    SRC_GEO = os.path.join(ROOT, "source", "geo")
    SRC_MAIN = os.path.join(ROOT, "source", "main")
    SRC_OTHER = os.path.join(ROOT, "source", "other")

    for folder in [ROOT , RES_LATEST ,RES_ARCHIVE , SRC_DOCS ,SRC_GEO ,SRC_MAIN ,SRC_OTHER]: 
        if not os.path.exists(folder): 
            os.mkdir(folder)
    return ROOT , RES_LATEST ,RES_ARCHIVE , SRC_DOCS ,SRC_GEO ,SRC_MAIN ,SRC_OTHER

ROOT , RES_LATEST ,RES_ARCHIVE , SRC_DOCS ,SRC_GEO ,SRC_MAIN ,SRC_OTHER = make_folder_structure()
