# HelloFresh-UK
I explored the HelloFresh YouTube channel by scrapping data from YouTube with an API key from Google Cloud and performing EDA

We start this project by first creating a YouTube API Key which will be our credential to access YouTube data. I will show you in detail, how to create an API Key. Once the API Key is generated, we will then learn how to use this API key to access different YouTube data. I.e. we will walk through the documentation given by Google to use YouTube API. We will look at the different sections in the documentation to access different data we need to build this project. We will also look at the sample Python code given by Google to call different resources and methods to fetch YouTube data.

https://developers.google.com/youtube/v3/code_samples/code_snippets?apix=true Please refer to the documentation and install the required libraries.


Exploratory Data Analysis by Scrapping API key from Youtube

Build a Python project to access and analyze data from the YouTube API

Extracting data from YouTube API

Extract channel name, subscriber count, and view count from YouTube API response.

Function modified to handle multiple channel ids

Extracted channel details and visualized them

Extract video ids from YouTube playlist

Iterate requests to fetch all 147 video details

Fetch video details for a range of 50 videos at a time

Analyzed HelloFresh UK's video posting pattern and found he posted most videos in July and least in October.

Convert channel data into CSV format for video details of HelloFresh UK

---------------------------------

 Build a Python project to access and analyze data from the YouTube API
- Create an API key through Google Developer Console
- Refer to the YouTube Data API documentation for necessary resources and methods

 Extracting data from YouTube API
- Using Google API client and Pandas to extract data for channels
- Comparing channels based on their total number of videos, views, and subscribers

 Extract channel name, subscriber count, and view count from YouTube API response.
- Access response from items[0] -> statistics -> subscriber count for subscribers.
- Access response from items[0] -> statistics -> view count for view count.
- Access response from items[0] -> snippet -> title for channel name.

 Function modified to handle multiple channel ids
- Loop added to iterate through each channel detail
- Index value updated to dynamically fetch details for each channel

Extracted channel details and visualized them
- Subscribers and views do not always correlate with number of videos posted
- A playlist id can be used to extract all videos from a channel

Extract video ids from YouTube playlist
- Use YouTube Data API to fetch playlist items
- Access content details to extract video id

Iterate requests to fetch all 147 video details
- Current code only fetches details for 50 videos at a time
- Use a for loop to iterate requests until all 147 videos are fetched

Fetch video details for a range of 50 videos at a time
- Loop through the response object to get details for each video
- Create a dictionary to store details such as title, published date, views, likes, dislikes, and comments
- Append each dictionary into a list
- Return the list of dictionaries with all video details

Analyzed HelloFresh UK's video posting pattern and found they posted most videos in September and least in March.
- Used pandas to group data by monthly video count
- Sorted data by month
- Visualized data using seaborn library

Convert channel data into CSV format for video details of HelloFresh UK
- Use 'to_csv' command to convert data frame into CSV file
- Name the CSV file as 'video_details(HelloFresh UK).csv'
