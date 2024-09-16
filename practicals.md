# Data Analytics Methods for Marketing


## Overview

This unit delves into the essential data analytics methods that drive effective social media marketing. It includes audience segmentation techniques, customer data platforms (CDPs), and advanced clustering methods such as K-Means. By applying these methods, marketers can gain valuable insights into their audience, optimize marketing strategies, and achieve better results.

## 1. Introduction to Data Analytics Methods for Marketing

### **Understanding Data Analytics in Marketing**
- **Purpose**: Data analytics involves analyzing data to extract actionable insights that can enhance marketing strategies and performance. It provides a way to make data-driven decisions rather than relying on intuition alone.
- **Types of Analytics**:
  - **Descriptive Analytics**: Analyzing historical data to understand what has happened in the past (e.g., website traffic, sales figures).
  - **Diagnostic Analytics**: Investigating data to understand why something happened (e.g., why a campaign performed well or poorly).
  - **Predictive Analytics**: Using data to forecast future outcomes (e.g., predicting customer behavior or sales trends).
  - **Prescriptive Analytics**: Recommending actions based on data analysis to achieve desired outcomes (e.g., optimizing marketing strategies).

### **Key Metrics and KPIs**
- **Engagement Rates**: Measures interactions such as likes, comments, and shares relative to the number of followers or views.
- **Click-Through Rates (CTR)**: The percentage of people who click on a link in your ad or post compared to the number of times it was viewed.
- **Conversion Rates**: The percentage of users who complete a desired action (e.g., making a purchase or signing up for a newsletter) compared to the total number of visitors.
- **Return on Investment (ROI)**: Calculates the profitability of marketing efforts by comparing the revenue generated to the costs incurred.

## 2. Find Your Audience with Segmentation

### **Audience Segmentation**
- **Definition**: The process of dividing a broad consumer or business market into sub-groups of consumers based on shared characteristics or behaviors. This allows for more targeted and effective marketing.
- **Benefits**:
  - **Personalization**: Tailoring marketing messages to specific audience segments increases relevance and engagement.
  - **Efficiency**: Allocating resources more effectively by targeting segments that are most likely to convert.
  - **Insights**: Gaining a deeper understanding of different customer groups and their needs.

### **Examples of Segmenting Audiences**
- **Demographic Segmentation**:
  - **Age**: Targeting different age groups with age-appropriate content and offers.
  - **Gender**: Creating gender-specific campaigns based on preferences and interests.
  - **Income Level**: Offering products or services that align with different income brackets.
- **Behavioral Segmentation**:
  - **Purchase History**: Segmenting customers based on their past purchase behaviors to offer personalized recommendations.
  - **Usage Patterns**: Identifying users who frequently engage with certain features or content and targeting them with related offers.
- **Geographic Segmentation**:
  - **Location-Based Marketing**: Targeting users based on their geographic location, such as country, region, or city.
  - **Local Offers**: Providing promotions or content relevant to users in specific areas.

### **Programmatic Creative**
- **Definition**: The use of automated technology to deliver personalized ad content based on user data and behavior.
- **Implementation**:
  - **Data Integration**: Collecting and analyzing data from various sources to understand user preferences and behaviors.
  - **Dynamic Creative**: Creating ads that change based on user data, such as showing different products or messages based on browsing history.
  - **Optimization**: Continuously analyzing performance data to refine and improve ad creatives for better results.

## 3. Customer Data Platforms (CDP)

### **What is a CDP?**
- **Definition**: A CDP is a unified platform that consolidates customer data from various sources into a single database. It provides a comprehensive view of each customer and enables personalized marketing.
- **Functionality**:
  - **Data Collection**: Aggregates data from multiple sources such as websites, social media, email campaigns, and CRM systems.
  - **Data Integration**: Combines data from disparate sources to create a unified customer profile.
  - **Segmentation**: Enables the creation of detailed customer segments for targeted marketing.

### **Benefits of Using a CDP**
- **Enhanced Customer Insights**: Provides a 360-degree view of customer interactions and behaviors.
- **Personalization**: Facilitates the delivery of personalized experiences based on integrated customer data.
- **Efficiency**: Streamlines data management and reduces the complexity of handling multiple data sources.





### **1. Data Collection**

**Objective:** This lab aims to guide you through the process of collecting data from YouTube using the YouTube Data API, focusing on retrieving and storing key video metrics.

**Platform:** YouTube  
**API Used:** YouTube Data v3

---
## **API Setup: YouTube Data API**

**Objective:** Learn how to set up and generate API credentials for the YouTube Data API to fetch and analyze video data.


#### **Step-by-Step Guide to Set Up the YouTube Data API**

**Step 1: Create a Google Cloud Project**
1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Sign in with your Google account.
3. Click on the "Select a project" dropdown at the top, and then click "New Project."
4. Enter a Project Name and click **Create**.
5. After a few seconds, your new project will be created, and you’ll be directed to the project dashboard.

**Step 2: Enable the YouTube Data API**
1. In the Google Cloud Console, navigate to the **API & Services** menu on the left side.
2. Click on **Library**.
3. Search for "YouTube Data API v3" in the API Library.
4. Click on the YouTube Data API v3 result.
5. Click the **Enable** button to enable the API for your project.

**Step 3: Create API Credentials**
1. Once the API is enabled, go to the **Credentials** tab in the API & Services section.
2. Click on the **Create Credentials** button at the top.
3. In the dropdown, select **API Key**.
4. An API Key will be generated. Copy this key, as it will be used in your Python code.

**Step 4: Set Quotas (Optional)**
1. In the same **Credentials** tab, you can set up quotas and monitor the usage of your API to ensure you stay within the free limits.
2. You can also request higher quotas if your project requires more extensive data collection.

**Step 5: Usage Limits**
1. The free tier offers up to 10,000 units per day (each request has a unit cost, e.g., fetching video details costs 1 unit per call).
2. To check the usage, go to the **Quota** tab within the API & Services section.


**Cost Information:**  
As long as your application stays within the free usage limits, you won't be charged. Review YouTube API pricing if you expect higher usage.


For detailed guidance, refer to the following video tutorial:  
[How to Setup YouTube Data API with Python](https://youtu.be/fN8WwVQTWYk?si=dxKXZaa0O_otSy1c)



---


**Key Concepts:**

1. **YouTube Data API:**
   - **Video Details:** The API provides detailed information about individual videos, including titles, descriptions, view counts, likes, and comments.
   - **Channel Statistics:** It allows you to fetch data related to channel performance, such as subscriber count, total views, and the number of uploaded videos.
   - **Playlist Information:** You can retrieve details about playlists, including their titles, descriptions, and the list of videos contained within.

2. **API Requests and Responses:**
   - **Requests:** To retrieve data, you send a request to the API with specific parameters (e.g., video IDs, part of the video data you want).
   - **Responses:** The API responds with JSON data, which includes the requested information about videos or channels.

3. **Data Fields:**
   - **Snippet:** Contains basic information about the video such as title, description, and publish date.
   - **Statistics:** Provides numerical metrics such as view count, like count, and comment count.

4. **Data Storage:**
   - **CSV Files:** A common format for storing tabular data, which can be easily used for further analysis in tools like Excel or Python pandas.
   - **Databases:** For larger datasets, storing data in databases might be more efficient for querying and analysis.

5. **Ethical Considerations:**
   - **Privacy:** Ensure that the data you collect and use complies with YouTube’s terms of service and privacy policies.
   - **Data Usage:** Use the collected data responsibly, particularly if it involves user interactions or sensitive content.
  


**Imports:**

```python
from googleapiclient.discovery import build
import pandas as pd
import seaborn as sns
from matplotlib import pyplot as plt
import json
```

- `googleapiclient.discovery.build`: This function is used to create a service object for interacting with the YouTube Data API.
- `pandas as pd`: Pandas is used for data manipulation and analysis. It helps in creating data frames, which are useful for storing and processing the collected data.
- `seaborn as sns`: Seaborn is a data visualization library based on matplotlib, which provides a high-level interface for drawing attractive statistical graphics.
- `matplotlib.pyplot as plt`: Matplotlib is used for creating static, animated, and interactive visualizations in Python.
- `json`: This module is used to handle JSON data, which is the format used for data returned by the YouTube Data API.

```python
api_key = 'XXXXXXXXXXXXXX'
```

- **API Key:** This line assigns your YouTube Data API key to the variable `api_key`. The API key is essential for authenticating your requests to the YouTube Data API. Make sure to keep your API key secure and avoid sharing it publicly.

```python
youtube = build('youtube', 'v3', developerKey=api_key)
```

- **Building the YouTube Service Object:** This line creates a service object for the YouTube Data API.
  - `build('youtube', 'v3', developerKey=api_key)` initializes the API client, specifying the service name (`youtube`), the version of the API (`v3`), and the API key for authentication. This service object will allow you to make various requests to the YouTube Data API.

```python
# channel_id ='UCLwc4plOL_MRHQnpFVTPQnw'
channel_id = [
    "UCJIfeSCssxSC_Dhc5s7woww", # lex clips
    "CYI_ychRnL7sJrG6PUSBpQA" , # cbn news
]
```

- **Channel IDs:** This line defines a list of YouTube channel IDs. Each channel ID is a unique identifier for a specific YouTube channel.
  - The commented line shows an alternative way to define a single channel ID, while the list format allows you to include multiple channel IDs. In this case, the channels are:
    - `"UCJIfeSCssxSC_Dhc5s7woww"`: This ID represents the channel for "lex clips."
    - `"CYI_ychRnL7sJrG6PUSBpQA"`: This ID represents the channel for "cbn news."
- You will use these channel IDs later in your code to fetch specific data (e.g., videos, playlists, statistics) associated with these channels.
To get the YouTube Channel IDs, you can follow these steps:

### **1. Method 1: Through YouTube Website**

1. Go to the YouTube channel page for the desired channel.
2. In the browser’s address bar, the URL will look something like this:  
   `https://www.youtube.com/channel/UCLwc4plOL_MRHQnpFVTPQnw`
   
   Here, the string after `/channel/` is the **Channel ID**. For example:
   - **Channel ID**: `UCLwc4plOL_MRHQnpFVTPQnw`

3. Alternatively, some URLs might look like this:  
   `https://www.youtube.com/c/CBNNews`
   
   In such cases, replace `/c/` with `/channel/` in the URL and then press Enter. It will redirect you to the new URL that contains the **Channel ID**.

### **2. Method 2: Using YouTube API**

You can retrieve channel IDs programmatically through the YouTube Data API v3 by using the **search.list** method. Here’s an example of how to get the **Channel ID** for specific queries using Python:

```python
from googleapiclient.discovery import build

# Initialize the YouTube API
api_key = 'YOUR_API_KEY'
youtube = build('youtube', 'v3', developerKey=api_key)

# Function to search for channels and get their Channel ID
def get_channel_id(query):
    request = youtube.search().list(
        part="snippet",
        q=query,
        type="channel",
        maxResults=1
    )
    response = request.execute()
    
    for item in response['items']:
        print("Channel Name:", item['snippet']['title'])
        print("Channel ID:", item['snippet']['channelId'])
        
# Example usage
get_channel_id("CBN News")
get_channel_id("Lex Clips")
```

- Replace `"YOUR_API_KEY"` with your actual API key.
- Replace the `query` parameter with the name of the channel you want to search for.

This will output the **Channel ID** of the YouTube channels matching your query.

### Requesting Data from the API

The following code snippet demonstrates how to request and retrieve statistics and other details for YouTube channels using the YouTube Data API:

```python
def getStats(youtube, channel_id):
    all_data = []
    request = youtube.channels().list(
        part='snippet,contentDetails,statistics',
        id=','.join(channel_id)
    )
    response = request.execute()
    return response
```

- **`getStats` Function:**
  - **Parameters:**
    - `youtube`: The YouTube API service object.
    - `channel_id`: A list of YouTube channel IDs to retrieve data for.
  - **Functionality:**
    - Constructs and executes an API request to fetch details for the specified channels.
    - **`part='snippet,contentDetails,statistics'`**: Requests data from the `snippet`, `contentDetails`, and `statistics` parts of the channel resource.
    - **`id=','.join(channel_id)`**: Converts the list of channel IDs into a comma-separated string for the API request.
    - Returns the API response containing the requested data.

```python
allchannestats = getStats(youtube, channel_id)
```

- **`allchannestats` Assignment:**
  - Calls the `getStats` function with the `youtube` service object and the list of channel IDs.
  - Stores the API response in `allchannestats`, which contains the detailed information for the specified channels.

### Printing Response

When you print the `allchannestats` variable, you get a detailed response from the YouTube API, which includes comprehensive information about the requested YouTube channels. The printed output will look like this:

```json
{
  'kind': 'youtube#channelListResponse',
  'etag': 'naLBSjom5HGKnLxNKcMKB0AaD-o',
  'pageInfo': {'totalResults': 1, 'resultsPerPage': 5},
  'items': [
    {
      'kind': 'youtube#channel',
      'etag': 'dl0Jofb2ymP2hDOgV3ArB7uTywA',
      'id': 'UCJIfeSCssxSC_Dhc5s7woww',
      'snippet': {
        'title': 'Lex Clips',
        'description': 'Clips from the Lex Fridman podcast. Visit the main channel for full conversations and other videos.',
        'customUrl': '@lexclips',
        'publishedAt': '2019-08-06T22:07:58Z',
        'thumbnails': {
          'default': {'url': 'https://yt3.ggpht.com/ytc/AL5GRJWSpZEszRakeC3YZs41nv_KUzSvaDAwn75umPey=s88-c-k-c0x00ffffff-no-rj', 'width': 88, 'height': 88},
          'medium': {'url': 'https://yt3.ggpht.com/ytc/AL5GRJWSpZEszRakeC3YZs41nv_KUzSvaDAwn75umPey=s240-c-k-c0x00ffffff-no-rj', 'width': 240, 'height': 240},
          'high': {'url': 'https://yt3.ggpht.com/ytc/AL5GRJWSpZEszRakeC3YZs41nv_KUzSvaDAwn75umPey=s800-c-k-c0x00ffffff-no-rj', 'width': 800, 'height': 800}
        },
        'localized': {'title': 'Lex Clips', 'description': 'Clips from the Lex Fridman podcast. Visit the main channel for full conversations and other videos.'},
        'country': 'US'
      },
      'contentDetails': {
        'relatedPlaylists': {
          'likes': '',
          'uploads': 'UUJIfeSCssxSC_Dhc5s7woww'
        }
      },
      'statistics': {
        'viewCount': '252848198',
        'subscriberCount': '829000',
        'hiddenSubscriberCount': False,
        'videoCount': '4896'
      }
    }
  ]
}
```

**Explanation:**

- **`kind`**: Specifies the type of resource returned by the API, in this case, a `youtube#channelListResponse`.
- **`etag`**: A unique identifier for the version of the resource returned.
- **`pageInfo`**: Contains information about the pagination of the results:
  - `totalResults`: Total number of results for the query.
  - `resultsPerPage`: Number of results per page.
- **`items`**: A list of channel objects containing the following details for each channel:
  - **`kind`**: Type of resource (`youtube#channel`).
  - **`etag

`**: Unique identifier for the version of the resource.
  - **`id`**: The unique identifier for the channel.
  - **`snippet`**: Contains basic details about the channel:
    - `title`: The title of the channel.
    - `description`: The description of the channel.
    - `customUrl`: The custom URL for the channel.
    - `publishedAt`: The date and time when the channel was published.
    - `thumbnails`: URLs for different sizes of the channel's thumbnail image.
    - `localized`: Translated title and description of the channel.
    - `country`: The country where the channel is based.
  - **`contentDetails`**: Contains details about the channel's content:
    - `relatedPlaylists`: Information about playlists related to the channel, such as uploads.
  - **`statistics`**: Contains various metrics related to the channel:
    - `viewCount`: Total number of views for the channel.
    - `subscriberCount`: Total number of subscribers.
    - `hiddenSubscriberCount`: Indicates whether the subscriber count is hidden.
    - `videoCount`: Total number of videos uploaded to the channel.

Sure, here’s a structured way to incorporate your new content into the existing lab document. I’ve included all the code snippets and outputs as well.

---

## **YouTube Analytics**
The provided  below code is performing **YouTube Channel and Video Analytics** through a few key steps, which allow for comprehensive analysis of YouTube data. Here’s an overall view of the types of analysis being done:

### **1. Channel-Level Analysis**
The code retrieves statistics for YouTube channels and focuses on understanding each channel's overall performance. This includes:
- **Subscribers**: The number of subscribers each channel has.
- **Views**: The total number of views for each channel.
- **Total Videos**: The total number of videos each channel has uploaded.
- **Visualization**: Scatter plots and bar charts are used to compare subscriber counts, views, and video upload counts across multiple channels. The visualizations help in understanding:
  - Relationships between the number of subscribers and views.
  - Comparison of how many videos different channels have uploaded.

### **2. Video-Level Analysis**
The code also drills down into video-level details for a more granular analysis of content performance. This includes:
- **Individual Video Statistics**: For each video, the following data is retrieved:
  - **Title**: The video’s title.
  - **Published Date**: The date the video was published.
  - **Views**: The number of views each video has received.
  - **Likes**: The total number of likes.
  - **Comments**: The number of comments.

- **Video Upload Trends**: The code extracts the month from the video’s publish date to analyze upload patterns over time. This includes:
  - Counting how many videos were uploaded each month.
  - Creating a bar plot to visualize the number of videos uploaded per month.

### **3. Key Insights**
- **Channel Growth and Popularity**: By comparing subscriber and view counts across multiple channels, you can identify which channels are growing faster or have more engagement.
- **Content Volume**: The number of videos uploaded by each channel is analyzed, showing the volume of content produced.
- **Video Engagement**: Views, likes, and comments on individual videos provide insights into how well the audience engages with each piece of content.
- **Seasonal Upload Patterns**: By analyzing the number of videos uploaded each month, you can identify potential seasonal trends in content production.

### **Overall Purpose**
The overall purpose of this analysis is to:
- **Evaluate Channel Performance**: See how channels perform in terms of subscribers, views, and video uploads.
- **Analyze Content Trends**: Understand which content types are performing better and detect any seasonal or monthly patterns in video uploads.
- **Guide Strategic Decisions**: Use these insights to improve content strategies, such as focusing on high-engagement periods, optimizing video frequency, or tailoring content to boost views and subscribers.

In summary, this code helps in analyzing both macro-level channel performance and micro-level video details, providing a comprehensive view of YouTube performance for content creators or marketers.






**Platform:** YouTube  
**API Used:** YouTube Data API v3  
**References:** [Python Quickstart](https://developers.google.com/youtube/v3/quickstart/python), [Console](https://console.developers.google.com/), [API Docs](https://developers.google.com/youtube/v3/docs)

---

### **1. Introduction**

In this lab, you will use the YouTube Data API v3 to retrieve and analyze statistics from various YouTube channels. We will cover how to set up the API, extract channel data, and visualize the information.

---


**Imports:**

```python
from googleapiclient.discovery import build
import pandas as pd
import seaborn as sns
from matplotlib import pyplot as plt
import json
```

**2. API Key and YouTube Object Initialization:**

```python
api_key = 'AIzaSyBT3GkJ8WUvdum1PGd3aFAXHc3eXgs19Sg'
youtube = build('youtube', 'v3', developerKey=api_key)
```

---

### **3. Retrieve Channel Statistics**

**Channel IDs:**

```python
channel_id = [
    "UCJIfeSCssxSC_Dhc5s7woww",  # lex clips
    "CYI_ychRnL7sJrG6PUSBpQA",   # cbn news
    "UCeVMnSShP_Iviwkknt83cww",  # code with harry
    "UC1bwliGvJogr7cWK0nT2Eag",  # mkiceandfire
    "UCchBatdUMZoMfJ3rIzgV84g",  # viva la dirt league
    "UCsooa4yRKGN_zEE8iknghZA"   # TED-ED
]
```

**Function to Retrieve Channel Stats:**

```python
def get_channel_stats(youtube, channel_id):
    all_data = []
    request = youtube.channels().list(
                part='snippet,contentDetails,statistics',
                id=','.join(channel_id))
    response = request.execute()
    for i in range(len(response['items'])):
        data = {
            'Channel_name': response['items'][i]['snippet']['title'],
            'Subscribers': response['items'][i]['statistics']['subscriberCount'],
            'Views': response['items'][i]['statistics']['viewCount'],
            'Total_videos': response['items'][i]['statistics']['videoCount'],
            'playlist_id': response['items'][i]['contentDetails']['relatedPlaylists']['uploads']
        }
        all_data.append(data)
    return all_data
```

**Retrieve Data and Create DataFrame:**

```python
allchannestats = get_channel_stats(youtube, channel_id)
channel_data = pd.DataFrame(allchannestats)
```

**Output:**

| Channel_name         | Subscribers | Views      | Total_videos | playlist_id                |
|----------------------|-------------|------------|--------------|-----------------------------|
| CodeWithHarry        | 3,740,000    | 482,375,029| 1,982        | UUeVMnSShP_Iviwkknt83cww   |
| MKIceAndFire         | 3,320,000    | 1,798,326,438| 7,072      | UU1bwliGvJogr7cWK0nT2Eag   |
| Viva La Dirt League  | 4,700,000    | 1,593,198,977| 1,236      | UUchBatdUMZoMfJ3rIzgV84g   |
| Lex Clips            | 828,000      | 252,453,828| 4,888        | UUJIfeSCssxSC_Dhc5s7woww   |
| TED-Ed               | 18,200,000   | 3,483,375,297| 2,013      | UUsooa4yRKGN_zEE8iknghZA   |


---

### **4. Data Preprocessing**

**Convert Data Types:**

```python
channel_data['Subscribers'] = pd.to_numeric(channel_data['Subscribers'])
channel_data['Views'] = pd.to_numeric(channel_data['Views'])
channel_data['Total_videos'] = pd.to_numeric(channel_data['Total_videos'])
channel_data.dtypes
```



**Output:**

| Column_name    | Data Type |
|----------------|-----------|
| Channel_name   | object    |
| Subscribers     | int64     |
| Views           | int64     |
| Total_videos    | int64     |
| playlist_id     | object    |


---

### **5. Data Visualization**

**1. Subscribers vs. Views:**

```python
plt.figure(figsize=(12, 6))
sns.scatterplot(data=channel_data, x='Subscribers', y='Views', hue='Channel_name')
plt.title('Subscribers vs. Views')
plt.xlabel('Subscribers')
plt.ylabel('Views')
plt.xscale('log')
plt.yscale('log')
plt.legend(title='Channel Name')
plt.show()
```

**2. Number of Videos per Channel:**

```python
plt.figure(figsize=(12, 6))
sns.barplot(x='Channel_name', y='Total_videos', data=channel_data)
plt.title('Number of Videos per Channel')
plt.xlabel('Channel Name')
plt.ylabel('Total Videos')
plt.xticks(rotation=45)
plt.show()
```

**3. Subscribers Count Bar Graph:**

```python
sns.set(rc={'figure.figsize':(10,8)})
ax = sns.barplot(x='Channel_name', y='Subscribers', data=channel_data)
plt.title('Subscribers Count by Channel')
plt.xlabel('Channel Name')
plt.ylabel('Subscribers')
plt.xticks(rotation=45)
plt.show()
```

**4. Views Count Bar Graph:**

```python
ax = sns.barplot(x='Channel_name', y='Views', data=channel_data)
plt.title('Views Count by Channel')
plt.xlabel('Channel Name')
plt.ylabel('Views')
plt.xticks(rotation=45)
plt.show()
```

**5. Total Videos Bar Graph:**

```python
ax = sns.barplot(x='Channel_name', y='Total_videos', data=channel_data)
plt.title('Total Videos Count by Channel')
plt.xlabel('Channel Name')
plt.ylabel('Total Videos')
plt.xticks(rotation=45)
plt.show()
```

---

### **6. Retrieve Video Details**

**Function to Get Video IDs:**

```python
def get_video_ids(youtube, playlist_id):
    request = youtube.playlistItems().list(
                part='contentDetails',
                playlistId=playlist_id,
                maxResults=50)
    response = request.execute()
    
    video_ids = []
    
    for item in response['items']:
        video_ids.append(item['contentDetails']['videoId'])
        
    next_page_token = response.get('nextPageToken')
    while next_page_token:
        request = youtube.playlistItems().list(
                    part='contentDetails',
                    playlistId=playlist_id,
                    maxResults=50,
                    pageToken=next_page_token)
        response = request.execute()
        for item in response['items']:
            video_ids.append(item['contentDetails']['videoId'])
        next_page_token = response.get('nextPageToken')
        
    return video_ids
```

**Retrieve Video IDs for a Specific Playlist:**

```python
playlist_id = channel_data.loc[channel_data['Channel_name'] == 'MKIceAndFire', 'playlist_id'].iloc[0]
video_ids = get_video_ids(youtube, playlist_id)
print("For channel YouTube MKIceAndFire we have over ", len(video_ids), " video ids")
```

**Output:**

```
For channel YouTube MKIceAndFire we have over  7072  video ids
```



### Function to Get Video Details

**Objective**: Fetch details for each video in the given playlist.

```python
def get_video_details(youtube, video_ids):
    all_video_stats = []
    
    for i in range(0, len(video_ids), 50):
        # Fetch video details in batches of 50
        request = youtube.videos().list(
            part='snippet,statistics',
            id=','.join(video_ids[i:i+50])
        )
        response = request.execute()
        
        for video in response['items']:
            # Collect relevant video statistics
            video_stats = {
                'Title': video['snippet']['title'],
                'Published_date': video['snippet'].get('publishedAt', 'N/A'),
                'Views': video['statistics'].get('viewCount', 'N/A'),
                'Likes': video['statistics'].get('likeCount', 'N/A'),
                'Comments': video['statistics'].get('commentCount', 'N/A'),
                'Favourites': video['statistics'].get('favoriteCount', 'N/A')
            }
            all_video_stats.append(video_stats)
    
    return all_video_stats
```

### Retrieve Video Details and Create DataFrame

**Objective**: Use the above function to get video details and convert them into a DataFrame.

```python
# Get video details using the function
video_details = get_video_details(youtube, video_ids)

# Create a DataFrame from the video details
video_data = pd.DataFrame(video_details)

# Output sample DataFrame
print(video_data.head())
```

**Output**:
```
           Title           Published_date        Views  Likes Comments Favourites
0  Mortal Kombat X Goro Gameplay  2013-02-27T17:54:01Z   9850       57       0           0
...
```

### **Analyzing Video Data by Month**



#### **1. Saving Data to CSV**

```python
# Save video data to a CSV file for further analysis
video_data.to_csv("mkiceandfire_video_stats.csv")
```

- **Purpose**: Exports the DataFrame `video_data` to a CSV file named `mkiceandfire_video_stats.csv`. This file can be used for additional analysis or reporting.

#### **2. Extracting Month from Published Date**

```python
# Extract the month from the 'Published_date' column and format it
video_data['Month'] = pd.to_datetime(video_data['Published_date']).dt.strftime('%b')
```

- **Purpose**: Converts the 'Published_date' column to datetime format and extracts the month abbreviation (e.g., Jan, Feb) to create a new column 'Month'. This helps in grouping the data by month.

#### **3. Counting Videos per Month**

```python
# Count the number of videos per month
videos_per_month = video_data.groupby('Month', as_index=False).size()
```

- **Purpose**: Groups the data by the 'Month' column and counts the number of videos in each month. The result is a DataFrame showing the number of videos for each month.

#### **4. Sorting Data by Month**

```python
# Define the order of months
sort_order = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
# Set the month column as a categorical type with the defined order
videos_per_month.index = pd.CategoricalIndex(videos_per_month['Month'], categories=sort_order, ordered=True)
# Sort the DataFrame by month
videos_per_month = videos_per_month.sort_index()
```

- **Purpose**: Ensures that the months are sorted in the correct calendar order rather than alphabetical order. This is achieved by setting the 'Month' column as a categorical type with the specified order and then sorting the DataFrame.

#### **5. Creating a Bar Plot**

```python
# Plot the number of videos per month
ax2 = sns.barplot(x='Month', y='size', data=videos_per_month)
```

- **Purpose**: Uses Seaborn to create a bar plot of the number of videos per month. This visual representation helps in understanding the distribution of video uploads throughout the year.


---
### **Analyzing YouTube Data with Segmentation and K-Means Clustering**



## **1. Introduction to Segmentation**

### **1.1 What is Segmentation?**

Segmentation involves dividing a dataset into distinct groups based on shared characteristics. For YouTube data, segmentation can help identify different types of videos or audience segments based on metrics like views, likes, and engagement.

### **1.2 Why Use Segmentation?**

- **Targeted Analysis:** Understand various audience preferences and behaviors.
- **Improved Strategies:** Develop tailored marketing and content strategies based on identified segments.

### **1.3 Applying Segmentation to YouTube Data**

**1.3.1 Prepare the Data**

Ensure your data is clean and contains relevant features such as `Views`, `Likes`, and `Comments`.

**Code:**

```python
import pandas as pd

# Load the dataset
video_data = pd.read_csv("mkiceandfire_video_stats.csv")

# Display the first few rows
print(video_data.head())
```

**Explanation:**
- **Loading Data:** Load the YouTube data into a DataFrame for analysis.

**1.3.2 Segment the Data**

Define segments based on `Views` and `Likes`. For example, categorize videos into low, medium, and high engagement.

**Code:**

```python
# Define segments based on Views and Likes
def segment_video(row):
    if row['Views'] > 500000 and row['Likes'] > 10000:
        return 'High'
    elif row['Views'] > 100000 and row['Likes'] > 2000:
        return 'Medium'
    else:
        return 'Low'

video_data['Segment'] = video_data.apply(segment_video, axis=1)

# Display the segmented data
print(video_data[['Views', 'Likes', 'Segment']].head())
```

**Explanation:**
- **Segment Definition:** Create a function to categorize videos based on their `Views` and `Likes`.
- **Apply Function:** Assign segments to each video based on the defined criteria.

### **1.4 Visualize Segments**

**Code:**

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Visualize the segments
plt.figure(figsize=(10, 6))
sns.scatterplot(x='Views', y='Likes', hue='Segment', data=video_data, palette='coolwarm', s=100)
plt.title('Video Segmentation Based on Views and Likes')
plt.xlabel('Views')
plt.ylabel('Likes')
plt.legend(title='Segment')
plt.show()
```

**Explanation:**
- **Scatter Plot:** Visualize segments to understand how videos are distributed across different categories.

**1.5 Additional Visualizations for Segmentation**

- **Segment Distribution Pie Chart**

**Code:**

```python
# Plot a pie chart showing the distribution of segments
plt.figure(figsize=(8, 8))
segment_counts = video_data['Segment'].value_counts()
plt.pie(segment_counts, labels=segment_counts.index, autopct='%1.1f%%', colors=['#FF9999','#66B3FF','#99FF99'])
plt.title('Distribution of Video Segments')
plt.show()
```

**Explanation:**
- **Pie Chart:** Shows the percentage distribution of each segment, providing a visual representation of video categories.

- **Box Plot by Segment**

**Code:**

```python
# Box plot to compare views and likes across segments
plt.figure(figsize=(14, 7))
sns.boxplot(x='Segment', y='Views', data=video_data, palette='Set2')
plt.title('Distribution of Views by Segment')
plt.xlabel('Segment')
plt.ylabel('Views')
plt.show()

plt.figure(figsize=(14, 7))
sns.boxplot(x='Segment', y='Likes', data=video_data, palette='Set2')
plt.title('Distribution of Likes by Segment')
plt.xlabel('Segment')
plt.ylabel('Likes')
plt.show()
```

**Explanation:**
- **Box Plot:** Visualizes the distribution of `Views` and `Likes` across different segments, highlighting variations and outliers.

---

## **2. Applying K-Means Clustering**

### **2.1 Introduction to K-Means Clustering**

K-Means clustering is a technique used to partition data into clusters based on feature similarity, helping to uncover patterns and groupings in the data.

### **2.2 Preparing the Data for K-Means**

**2.2.1 Load and Extract Features**

Select the relevant features for clustering, such as `Views` and `Likes`.

**Code:**

```python
from sklearn.preprocessing import StandardScaler

# Extract relevant features
features = video_data[['Views', 'Likes']].dropna()

# Normalize the features
scaler = StandardScaler()
features_normalized = scaler.fit_transform(features)

# Display the normalized features
print(pd.DataFrame(features_normalized, columns=['Views', 'Likes']).head())
```

**Explanation:**
- **Feature Extraction:** Select features for clustering.
- **Normalization:** Standardize features to ensure equal weight in clustering.

### **2.3 Apply K-Means Clustering**
 - **Overview**: K-Means is an algorithm that partitions data into K clusters based on feature similarities. Each cluster is represented by its centroid, which is the mean of the data points within the cluster.
- **How It Works**:
  - **Initialization**: Randomly selecting K initial centroids.
  - **Assignment**: Assigning each data point to the nearest centroid based on distance metrics.
  - **Update**: Recalculating centroids based on the mean of data points assigned to each cluster.
  - **Iteration**: Repeating the assignment and update steps until centroids stabilize and no longer change significantly.

### **Determining the Number of Clusters**
- **Elbow Method**:
  - **Process**: Plotting the sum of squared distances from data points to their centroids for different values of K.
  - **Identification**: The "elbow" point on the graph indicates the optimal number of clusters where adding more clusters yields only marginal improvements.
- **Silhouette Score**:
  - **Measurement**: Evaluates how similar a data point is to its own cluster compared to other clusters.
  - **Interpretation**: A higher silhouette score indicates better-defined clusters with clear separation between them.
**2.3.1 Fit the K-Means Model**

Apply K-Means clustering to the normalized data.

**Code:**

```python
from sklearn.cluster import KMeans

# Apply K-Means clustering
kmeans = KMeans(n_clusters=3, random_state=42)
video_data['Cluster'] = kmeans.fit_predict(features_normalized)

# Display the first few rows with cluster assignments
print(video_data[['Views', 'Likes', 'Cluster']].head())
```

**Explanation:**
- **K-Means Initialization:** Set the number of clusters and fit the model.
- **Cluster Assignment:** Assign cluster labels to each video based on the clustering result.

### **2.4 Analyze and Visualize Clusters**

**2.4.1 Visualize Clusters**

**Code:**

```python
# Visualize the clustering
plt.figure(figsize=(10, 6))
sns.scatterplot(x='Views', y='Likes', hue='Cluster', data=video_data, palette='viridis', s=100)
plt.title('K-Means Clustering of Videos Based on Views and Likes')
plt.xlabel('Views')
plt.ylabel('Likes')
plt.legend(title='Cluster')
plt.show()
```

**Explanation:**
- **Scatter Plot:** Visualize clusters to understand how videos are grouped based on `Views` and `Likes`.

**2.4.2 Analyze Cluster Centroids**

**Code:**

```python
# Calculate and display cluster centroids
centroids = kmeans.cluster_centers_
print("Cluster Centroids:\n", centroids)

# Display cluster sizes
cluster_sizes = video_data['Cluster'].value_counts()
print("Cluster Sizes:\n", cluster_sizes)
```

**Explanation:**
- **Centroids:** Show the average feature values for each cluster.
- **Cluster Sizes:** Count the number of videos in each cluster to understand the distribution.

**2.4.3 Additional Visualizations for K-Means Clustering**

- **Cluster Distribution Pie Chart**

**Code:**

```python
# Plot a pie chart showing the distribution of clusters
plt.figure(figsize=(8, 8))
cluster_counts = video_data['Cluster'].value_counts()
plt.pie(cluster_counts, labels=cluster_counts.index, autopct='%1.1f%%', colors=['#FF9999','#66B3FF','#99FF99'])
plt.title('Distribution of Video Clusters')
plt.show()
```

**Explanation:**
- **Pie Chart:** Shows the percentage distribution of each cluster, indicating how many videos fall into each cluster.

- **Cluster Profiles**

**Code:**

```python
# Calculate cluster means for features
cluster_profiles = video_data.groupby('Cluster').mean()

print("Cluster Profiles:\n", cluster_profiles)

# Visualize cluster profiles
plt.figure(figsize=(14, 7))
sns.heatmap(cluster_profiles, annot=True, cmap='coolwarm', fmt='.2f')
plt.title('Cluster Profiles: Average Views and Likes')
plt.show()
```

**Explanation:**
- **Cluster Profiles:** Compute and display the average `Views` and `Likes` for each cluster.
- **Heatmap:** Visualizes the cluster profiles with a color gradient for easy comparison.

- **Pair Plot with Clustering**

**Code:**

```python
# Pair plot to visualize relationships between features within clusters
sns.pairplot(video_data, hue='Cluster', palette='viridis', vars=['Views', 'Likes'])
plt.suptitle('Pair Plot of Views and Likes by Cluster', y=1.02)
plt.show()
```

**Explanation:**
- **Pair Plot:** Visualizes pairwise relationships between features (`Views` and `Likes`) and color-codes by cluster.

- **Elbow Method for Optimal K**
The elbow method helps determine the optimal number of clusters for the K-Means algorithm by plotting the sum of squared distances (SSE) for different numbers of clusters.
This code performs the following:

- **Calculates SSE**: Computes the sum of squared distances between data points and their assigned cluster centers for different numbers of clusters.
- **Plots the Elbow Curve**: Creates a plot showing how SSE changes with the number of clusters.
- **Identifies the Optimal Number of Clusters**: The "elbow" of the curve indicates the optimal number of clusters where adding more clusters does not significantly improve the model.

**Code:**

```python
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt

# Calculate the sum of squared distances for different numbers of clusters
sse = []
for k in range(1, 11):
    kmeans = KMeans(n_clusters=k, random_state=42)
    kmeans.fit(features_normalized)
    sse.append(kmeans.inertia_)

# Plot the elbow curve
plt.figure(figsize=(8, 6))
plt.plot(range(1, 11), sse, marker='o', linestyle='--')
plt.title('Elbow Method for Optimal Number of Clusters')
plt.xlabel('Number of Clusters')
plt.ylabel('Sum of Squared Distances')
plt.show()
```



**Silhouette Score**

The Silhouette Score measures how similar an object is to its own cluster compared to other clusters. It helps evaluate the quality of clustering.

**Code:**

```python
from sklearn.metrics import silhouette_score

# Calculate Silhouette Score
silhouette_avg = silhouette_score(features_normalized, kmeans.labels_)
print(f'Silhouette Score: {silhouette_avg:.2f}')
```

**Explanation:**
- **Silhouette Score:** Provides an average measure of how well-separated and distinct the clusters are. Scores closer to 1 indicate well-defined clusters.

**Davies-Bouldin Index**

The Davies-Bouldin Index measures the average similarity ratio of each cluster with its most similar cluster, where a lower value indicates better clustering.

**Code:**

```python
from sklearn.metrics import davies_bouldin_score

# Calculate Davies-Bouldin Index
db_index = davies_bouldin_score(features_normalized, kmeans.labels_)
print(f'Davies-Bouldin Index: {db_index:.2f}')
```

**Explanation:**
- **Davies-Bouldin Index:** Helps assess the clustering quality. Lower values indicate better clustering performance.
  ## **Quiz Section**

Please take the following quiz:

[https://forms.gle/6BsAtRBpPiGWV9Ke6](https://forms.gle/6BsAtRBpPiGWV9Ke6)

