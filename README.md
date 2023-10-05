# Project 1: Approach to measuring the success of IGTV

Instagram TV (IGTV) is a video platform that allows users to view and upload long videos on the Instagram app.
It enables users to easily watch videos along with regular instagram posts on their feed or from a dedicated
IGTV section.

In the digital era, social media platforms such as IGTV have become a vital medium for businesses to connect with their target audience, build relationships and promote their products and services.
The digital landscape is continuously evolving with new platforms coming up and it is therefore it is important for IGTV to keep up with the new trends to ensure it's on top of the game.

As a data scientist at Instagram, you need to measure the success of IGTV to identify areas of improvement, to understand user needs and experience to make changes accordingly. This task would involve a combination of qualitative and quantitative metrics to provide a comprehensive view of IGTV's perfomance. The following is an outline of the steps to be undertaken:

## Define Clear Objectives

Start by defining clear and specific objectives. These objectives should align with Instagram's overall goals, such as user engagement, user retention, or revenue generation. The objectives could be as follows:

1. To examine user engagement on the platform

2. To identify the types of content popular among users.

3. To explore the impact of marketing campaigns.

At this stage, you also need to identify the key metrics to study such as;

- Impressions: The number of times an IGTV video is displayed on a user's screen.
- Reach: The number of unique users who see an IGTV video.
- Average watch time: The average amount of time that users spend watching an IGTV video.
- Engagement rate: The percentage of users who interact with an IGTV video by liking, commenting, or sharing it.
- Audience growth: The number of new followers that an IGTV creator gains over a period of time.

## Data Collection

After identifying the key metrics, the next step is to identify the relevant data to track them. In this case, the data required include: user engagement(number of likes, shares and comments), average impressions per post, audience growth (number of app downloads after the campaign, number of new followers per creator) and number of unique users. This is how I'd do it:

``` python
import pyforest
# load the data
data = data.read_csv('igtv_data.csv')
```

## Data cleaning

This stage involves eliminating any inconsistencies in the data. We will explore the data to remove missing values, duplicate entries and any outliers.

Here's an illustration with code:

```python
# Remove any missing values
  data = data.dropna()

  # Drop duplicate rows
data = data.drop_duplicates()

  # Fill in any remaining missing values with the mean of the column.
  data = data.fillna(data.mean())

```

## Data Analysis

This is where you use  various statistical methods such as mean to analyse the data. This is how I would get the average number of views:

``` python
# calculate the average number of views
average_video_views = data['campaign_video_views'].mean()

print(average_video_views)

# calculate the video completion rate
video_completion_rate = data['campaign_video_completion_rate'].mean()

print(video_completion_rate)

```

### Engagement Metrics

- User Engagement: Measure the number of users actively engaging with IGTV content. Key metrics include the number of video views, likes, comments, shares, and the time users spend watching IGTV videos.
- User Interaction: Analyze how users interact with the IGTV product, such as how often they swipe up to view content, how frequently they engage with IGTV Stories, and the percentage of users who upload their own videos to IGTV.

### Retention and Growth

- User Retention: Assess how IGTV impacts user retention by comparing the retention rates of users who engage with IGTV content versus those who don't.
- Audience Growth: Monitor the growth of IGTV's user base and assess how effectively it attracts new users to the Instagram platform.

### Content Metrics

- Content Consumption: Analyze the types of content that perform well on IGTV, such as the most-watched categories, popular creators, and trending topics.
- Content Creation: Track the number of content creators using IGTV and their level of activity. Encourage influencers and creators to produce content for IGTV.

### Monetization

- Revenue Generation: Measure the revenue generated through IGTV, which may include advertising revenue, sponsored content deals, or other monetization strategies.
- Ad Effectiveness: Evaluate the performance of IGTV ads, including click-through rates, engagement with sponsored content, and advertiser satisfaction.

### User Feedback

Gather qualitative data through surveys, user interviews, and feedback forums to understand user satisfaction and identify areas for improvement.

### Competition Benchmarking

Compare IGTV's performance with similar platforms and competitors to gain insights into market share and user preference.

### User Experience Metrics

Monitor user experience metrics such as app crashes, loading times, and overall performance to ensure a seamless IGTV experience.

### Long-Term Impact

Assess the long-term impact of IGTV on Instagram's brand image, user loyalty, and overall business growth.

### Iteration and Improvement

Continuously analyze the collected data to identify trends, challenges, and opportunities. Use insights to iterate on the IGTV product, introducing new features, and improving existing ones.

## Conclusion

Ultimately, the success of the IGTV product should be evaluated based on how well it aligns with Instagram's strategic goals, enhances user engagement, and contributes to the company's bottom line. Regularly reviewing and adapting your measurement strategy will be crucial in ensuring its ongoing success.
