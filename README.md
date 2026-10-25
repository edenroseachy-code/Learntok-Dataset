# Learntok-Dashboard
# Project overview
LearnTok is a University of Technology Sydney (UTS) Information Systems Capstone project investigating how content characteristics and educational quality indicators relate to audience engagement in educational YouTube Shorts. The dataset supports an interactive Tableau dashboard intended to help teachers explore and evaluate short-form educational content.

# Research question:
What content characteristics and quality indicators in YouTube Shorts are associated with higher audience engagement across different subject areas, and how can these insights inform teachers creating short-form learning content?

# Dataset overview
The project examines educational YouTube Shorts across 10 subjects: Art, Business, Economics, Geography, History, Law, Mathematics, Music, Science and Technology.

The project's combined spreadsheet contained 644 rows at the time of reporting. The Tableau dashboard displayed 636 distinct video IDs under its selected filters. These are different counts; users should inspect the uploaded dataset and its filtering rules before reporting a final number of records.

The dataset combines publicly available video information, engagement metrics, manually classified content characteristics and manually assessed educational quality scores.
Data collection and preparation
1. Data retrieval: Python scripts in Google Colab accessed the YouTube Data API v3 to collect publicly available video metadata and engagement metrics.
2. Search refinement: Searches covered educational topics and subtopics. Broad queries were refined using keywords such as explained, lesson, learn, tutorial and what is.
3. Filtering and screening: API short-video filtering and a maximum duration of 180 seconds were applied. Videos were manually reviewed to exclude irrelevant, entertainment-focused, non-English or otherwise unsuitable content.
4. Data understanding and preprocessing: The team explored the data, consolidated separate spreadsheets, checked missing values and duplicates, standardised categories, and converted durations and numerical fields as needed.
5. Manual classification and quality assessment: The team coded content characteristics and assessed educational quality using a 12-criterion rubric.
6. Analysis: The prepared data was used to calculate engagement measures and build interactive visualisations in Tableau.
Main variables
The dataset includes variables in the following groups. Exact column names may differ slightly in the exported file; consult the accompanying data dictionary if supplied.
Group	Variables	Description
Video identification	Video ID, title, channel, YouTube URL	Identifies and describes each video
Video metadata	Publication date, duration, duration in seconds	Describes when the video was published and its length
Engagement	Views, likes, comments	Publicly available audience interaction metrics
Normalised engagement	Like rate (%), comment rate (%)	Likes or comments divided by views, multiplied by 100
Educational classification	Educational topic, educational subtopic	Subject area and more specific learning topic
Content characteristics	Content format, presenter style, visual aids, on-screen text, educational hook, examples/demonstrations	Manually coded presentation features
Educational quality	12 criterion scores, overall quality score, quality level	Manually assessed indicators of potential educational value


Engagement metrics
Like rate (%) = (Likes / Views) × 100 

Comment rate (%) = (Comments / Views) × 100

Records with zero views require special handling to avoid division by zero.
Educational quality assessment
Each video was evaluated against 12 criteria, grouped under four principles:
Principle	Criteria
Cognitive Load	Learning Focus; Information Clarity; Information Structure; Distractions; Multimedia Support
Student Engagement	Language Clarity; Engaging Delivery; Educational Hook
Active Learning	Encouraged Thinking; Applied Learning
Teaching Value	Supports Understanding; Classroom Usefulness


Each criterion was scored from 0 to 2:
- 0: Weak or absent
- 1: Adequate or partially demonstrated
- 2: Strongly demonstrated

The 12 scores were summed to obtain an overall score out of 24:

Quality level	Overall score
- Low:	0–8
- Medium:	9–16
- High:	17–24

These are project-defined assessment categories, not independently validated measures of student learning outcomes.
# Using the dataset
1. Download the dataset file from this repository.
2. Open it in Microsoft Excel, Python/pandas, Tableau or another analysis tool.
3. Review the data dictionary and inspect missing or invalid values before analysis.
4. Use video IDs to check for duplicate records, and apply consistent filters when comparing results.
5. Compare engagement metrics, content characteristics and educational quality across subjects and subtopics.

# Limitations
- The dataset represents a selected sample of educational YouTube Shorts, not all educational videos on the platform.
- Search terms, subtopic selection and manual screening may affect which videos were included.
- Manual content classification and educational quality scoring involve subjective judgement.
- Views, likes and comments may be influenced by channel popularity, publication date and YouTube's recommendation system.
- Engagement measures reflect audience interaction; they do not directly measure learning or prove causal relationships.
- Engagement metrics may change over time as videos receive additional interactions. Related project resource
- LearnTok project website


# Data source and acknowledgement
Video metadata and public engagement counts were retrieved using the YouTube Data API v3. Content classifications and educational quality assessments were created by the LearnTok project team. This repository is an academic research project and is not affiliated with or endorsed by YouTube.
