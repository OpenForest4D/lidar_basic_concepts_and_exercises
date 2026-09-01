# Lidar Point Clouds and Gridded Data for Forest Analysis

> **Part of a two-repo lidar activity sequence.** These are **Activities
> 1–2**. A follow-up activity on measuring individual trees is available
> separately.
> - [Activity 3: Measuring Tree Structure from a Lidar Point Cloud](https://github.com/OpenForest4D/lidar-applied-tree-measurements)

This repository contains a set of hands-on activities that introduce
lidar (Light Detection and Ranging), an active remote sensing method,
and its derivative raster products. Students first learn what lidar is 
and how to download it from a public data portal. They then
process the lidar point cloud in R to build a digital elevation model
(DEM), a digital surface model (DSM), a digital terrain model (DTM), and
a canopy height model (CHM).

Each activity follows a two-part sequence: a short lesson (background
reading plus a brief questionnaire to check understanding) followed by a
hands-on worksheet. No prior experience with lidar or coding is required,
and all materials run directly in a web browser.

**Estimated time:** ~20 minutes per lesson + questionnaire, ~45-60
minutes per hands-on activity - roughly 2 hours for the full
two-activity sequence.

**Learning goal:** By the end of this lab exercise, students will be able
to locate and download airborne lidar data, and use it to derive and
interpret gridded terrain and canopy datasets.

**Objectives:**

- Navigate a public lidar data portal and select a dataset appropriate
  for a research question.
- Describe how a lidar pulse produces multiple returns and what those
  returns represent in a forested landscape.
- Distinguish among a DEM, DSM, DTM, and CHM, and explain how each is
  derived.
- Generate raster products from a point cloud and evaluate how
  processing choices affect the results.

## Audience

This lab is designed for lower-level undergraduate students (**freshmen
and sophomores**) and assumes no prior experience with lidar or
programming in R. It fits courses in forest ecology, remote sensing, GIS,
natural resource management, and environmental science. Each activity is
self-contained and can be assigned individually or run as a multi-part
sequence.

## How this is organized: lessons, then activities

Each numbered activity has two parts, and the folder names reflect that:

- **[`lessons/`](lessons/)** - background reading for that activity,
  ending with a short questionnaire to check understanding before moving
  on.
- **[`activities/`](activities/)** - the hands-on worksheet, done after
  the matching lesson.

We recommend working through `lessons/lesson_1...` before
`activities/activity_1...`, and the same for Activity 2. The two parts of
each activity can be split across two class sessions if your schedule
doesn't allow both in one sitting.

**Lesson/Activity 1: Lidar remote sensing basics and getting lidar data**
Students read an introduction to remote sensing and lidar, and complete
a short questionnaire in the lesson. As part of the activity, they then
search the OpenTopography data facility for a lidar dataset, define an
area of interest, and download the point cloud. Questions ask students
to interpret dataset metadata such as acquisition date, point density,
and coordinate reference system, and to justify their selection.

**Lesson/Activity 2: Deriving gridded datasets from lidar point cloud data**
Students read about lidar point clouds, gridded datasets, and surface
interpolation, followed by a short questionnaire. As part of the
activity, they classify ground returns and generate DEM, DSM, DTM, and
CHM outputs. Questions ask students to compare processing choices and
interpret the resulting canopy structure.

## Software

Activity 1 runs in a web browser using the OpenTopography portal; no
local software installation is required.

Activity 2 runs in Google Colab with an R runtime. No software needs to
be installed locally - students only need a web browser and a Google
account.

## Getting Started

All instructions are provided in the lesson and activity documents.

1. Read [`lessons/lesson_1_Introduction_to_Remote_Sensing_and_Lidar.docx`](lessons/)
   and complete the questionnaire at the end.
2. Open [`activities/activity_1_get_lidar_point_cloud_from_OpenTopography.docx`](activities/)
   and follow it to retrieve a lidar point cloud from OpenTopography.
3. Read [`lessons/lesson_2_Point_Clouds_and_Gridded_Datasets.docx`](lessons/)
   and complete the questionnaire at the end.
4. Open [`activities/activity_2_create_gridded_data_from_point_clouds.docx`](activities/)
   and open the linked Colab notebook.
5. Go to [`notebooks/Act1_Act2_combined.ipynb`](Act1_Act2_combined.ipynb) and Open in Colab link. In Google Colab, select **File -> Save a copy in Drive**. Edit that copy so
   you keep your own version of the work.

## Document formats

Lesson and activity documents are provided as PDF as well as editable
Word documents so you can customize and adapt them to your course.

| Format | Use it for | Link |
| --- | --- | --- |
| `.docx` | Editing in Word — the source files, fully customizable | [`lessons/`](lessons/), [`activities/`](activities/) |
| `.pdf` | Quick preview or a print/read-only version for students | *[add PDF preview links]* |

Google docs links can also be made available upon request.

## Data

The notebook expects a lidar point cloud file in the  `.laz` or `.las` format, downloadable
[here](https://zenodo.org/records/21517293).

The laz file is also available in the `data` folder of this repository.

## Repository Structure

```
lidar-basics-concepts-and-exercises/
├── lessons/
│   ├── lesson_1_Introduction_to_Remote_Sensing_and_Lidar.docx     # Reading + questionnaire for 1
│   └── lesson_2_Point_Clouds_and_Gridded_Datasets.docx            # Reading + questionnaire for 2
├── activities/
│   ├── activity_1_get_lidar_point_cloud_from_OpenTopography.docx  # Hands-on worksheet for Activity 1
│   └── activity_2_create_gridded_data_from_point_clouds.docx      # Hands-on worksheet for Activity 2
├── notebooks/
│   └── Act1_Act2_combined.ipynb                                   # Colab notebook for Activities 1 and 2
├── LICENSE
└── README.md
```

## For Instructors

The lesson and activity documents are fully editable, allowing you to
adapt them to your course needs. For an answer key to the in-activity
and questionnaire questions, please contact [OpenForest4D](https://openforest4d.org/contact/).

## Acknowledgments

- This material is developed as part of the OpenForest4D project funded
  by NSF awards 2409885, 2409886, and 2409887.
- Lidar data from NSF-funded
  [OpenTopography Facility](https://www.opentopography.org): State of Utah Acquired LiDAR Data - Wasatch Front. Distributed by OpenTopography. https://doi.org/10.5069/G9TH8JNQ . Accessed 2026-08-31
- [lidR](https://github.com/r-lidar/lidR), [terra](https://rspatial.github.io/terra/),
  [ggplot2](https://ggplot2.tidyverse.org/), [plotly](https://plotly.com/r/),
  and other open source libraries.
