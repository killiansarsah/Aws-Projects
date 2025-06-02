# 📊 Legendary AWS Analytics Project with Amazon QuickSight



## 🔍 Project Overview

In this project, I will demonstrate how to upload, connect, visualize, and publish data
insights using Amazon Web Services (AWS), specifically focusing on **Amazon S3** and **Amazon QuickSight**.



## 🧰 Tools Used

- **Amazon Web Services (AWS)**
- **Amazon S3**
- **Amazon QuickSight**
- **IAM Permissions**
- **manifest.json**



## 📁 Project Workflow

1. Upload dataset and manifest file to Amazon S3
2. Create and configure a QuickSight account
3. Connect dataset from S3 via manifest
4. Build bar/pie chart visualizations
5. Apply filters to refine insights
6. Create and export a polished dashboard



## Project reflection

It took me approximately 2 to 3 hours to complete the entire project, including setting
up the S3 bucket, configuring permissions, uploading the manifest, building
visualizations in QuickSight, and finalizing the dashboard.

After this project, I plan to work on analyzing e-commerce sales data using Amazon
QuickSight and Athena to uncover customer trends and optimize inventory decisions. I
will start this project on Monday, June 3, 2025.


## 🖼️ Upload project files into S3


Amazon S3 stores two files in this project: netflix_titles.csv and manifest.json. The CSV
file contains the Netflix data, while the manifest file tells QuickSight how to read the
CSV.

I edited the `manifest.json` to add the correct S3 path to the `netflix_titles.csv` file. This
helps QuickSight locate and understand the data format for proper import and
visualization from the S3 bucket.

  ![Screenshot 2025-05-30 202106](https://github.com/user-attachments/assets/cb2c51d5-41fc-4169-a80b-5d6a4d7a2db7)

  
![Screenshot 2025-05-30 203643](https://github.com/user-attachments/assets/bdcf197a-7ccd-4c4e-8ff6-7a5235042ef6)


## Create QuickSight account


Amazon QuickSight offers a free 30-day trial, but charges apply afterward based on
the edition and user type. Pricing starts at $9 per user/month for the Standard Edition,
with additional costs for features like SPICE storage and Amazon Q.

Opening a QuickSight account usually takes only a few minutes if you already have an
AWS account. Creating a new AWS account first may extend the process to about 10–
15 minutes.

<img width="958" alt="image" src="https://github.com/user-attachments/assets/5b4e1118-2929-4502-ba42-ced7d60621cd" />


## Download the Dataset

I went to the Datasets page in QuickSight, clicked New dataset, and selected S3. I
named the source kaggle-netflix-data and pasted the S3 URL for the manifest.json file
to connect my Netflix data for visualization.

The `manifest.json` file tells QuickSight where the dataset is in S3 and how to read it. It
provides the file location, format, and structure so QuickSight can correctly import and
visualize the data without errors.

![Screenshot 2025-05-30 210035](https://github.com/user-attachments/assets/47554da2-e6bf-44f3-8136-999d071c2fde)


## My first visualization

To create visualizations in QuickSight, choose a dataset, select a visual type like bar or
pie chart, then drag fields from the left panel into the graph area. Customize by
filtering, sorting, or changing chart types to best represent your data.

The visualization shows Netflix content by release year, split into TV shows and
movies. It highlights trends over time, revealing which years had more movies or TV
shows, helping analyze Netflixʼs content distribution and production focus each year.

I created this visualization by dragging **release\_year** to the Y Axis to show the
timeline and **type** to the Group/Color heading to differentiate between TV shows
and movies. This setup clearly compares content types by year.

![Screenshot 2025-05-30 215317](https://github.com/user-attachments/assets/e0e57633-0a36-4ea6-8a4f-9c74d9e3ef7f)


## Using filters
Filters are useful because they let you focus on specific parts of your data, making
analysis clearer and more relevant. They help narrow down large datasets to see
trends, patterns, or details without distraction from unrelated data.

The visualization shows the count of Netflix TV shows and movies released each year.
It breaks down content by type, helping identify trends over time, such as which years
had more movies or TV shows, revealing viewing content patterns.

![Screenshot 2025-05-30 220912](https://github.com/user-attachments/assets/e0b66b67-70a9-46ab-b1ef-1dc03b1e2d25)


## Setting up a dashboard
As a finishing touch, I added descriptive titles to each visualization for clarity, adjusted
the layout for a clean and organized look, and reviewed the data for accuracy before
publishing and exporting the dashboard as a PDF.

I exported my QuickSight dashboard as a PDF by clicking the "Share" button in the
top-right corner. Then I selected "Export to PDF" from the dropdown menu. After
confirming the layout, I downloaded the PDF file for sharing.

![Screenshot 2025-05-30 222616](https://github.com/user-attachments/assets/623bbe95-b56f-4add-9b88-44df3d330fa0)



## 🧠 Key Learnings

- How to securely manage datasets in AWS S3
- Connecting datasets using `manifest.json` in QuickSight
- Creating charts with filtering and grouping in QuickSight
- Designing and exporting dashboards for sharing insights

---

## 📅 Project Duration

**Estimated Time:** 2–3 hours  
**Next Steps:** Exploring AWS Athena with QuickSight for e-commerce data analysis (starting June 20, 2025)



