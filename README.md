# Cricket-Data-Analysis-T20
This project examines the influence of Indian cricket captaincy styles (Aggressive vs Defensive) on team performance in T20 International cricket (20-over cricket format). We aim to analyze how different leadership styles affect critical match outcomes such as powerplay performance, margins of victory, toss outcomes, and match results.

## Research Question: How do Indian cricket captaincy styles (Aggressive vs. Defensive) influence team performance in T20 Internationals?

The goal of this study is to investigate the influence of captaincy styles, categorized as Aggressive or Defensive, on the performance of the Indian cricket team in T20 International matches from 2006 to 2024. By examining various performance metrics, the study aims to understand how different leadership approaches impact match outcomes, strategic decisions, and consistency over time.

This question is essential for understanding whether a particular captaincy style is more advantageous in specific scenarios or against certain opponents and provides insights into optimal leadership strategies in T20 cricket.

## Data Visualisation Tools explored:
1. Bubble plot: Visualise Indian Captaincy Styles vs Powerplay Performance
2. (Interactive) Radar Chat: Visualises the performance metrics of the captains based on tenure (matches captained), tosses won (percetange) and match wins (percentage).
3. Box plot: Visualising the effect of captaincy style on the match margins, both for matches that are won and lost.
4. Violin plot: Highlights the performance of the Indian cricket team under aggressive and defensive captaincy styles, focusing on powerplay performance (both wickets and runs) of the Indian and opponent team, and match margins.
5. Pair Plots (with KDE): While distinguishing between Aggressive and Defensive captaincy styles, the pair plot shows associations between Margin (in runs), Year, and Toss Won by India.
6. t-SNE plot: Visualises the clustering of Indian cricket captains based on their performance metrics (Win Percentage, Matches Won, Matches Lost, and Relative Opponent Strength) and their captaincy styles.
7. Interactive Time Series plot: Illustrates how the captaincy styles and their effect has evolved over time.
8. Heatmap: India's win ratios against opponents for agressive and defensive styles, showing the effect of captaincy style on team performance against other teams.
9. World Map: Visualise India's wins by aggressive and defensive captains.
10. Sankey Diagram: provides a detailed flow visualization of the relationship between captaincy styles, toss outcomes, toss decisions, and match results in T20 International matches.

## Data Description
### Overview
The dataset used in this project comprises match-level details of T20 International matches played by Indian cricket team between 2006 and 2024, sourced from ESPN Cricinfo. After comprehensive cleaning, the final dataset included 230 rows of match details with detailed match and captaincy-specific data, along with derived performance metrics. This cleaned dataset serves as the foundation for analyzing the influence of captaincy style on team performance.

The dataset includes the following key attributes:
1. Match Information: There are two teams, Team 1 and Team 2. These teams compete among themselves in the matches. A Winner column that represents which team won the match. A Margin column representing the margin of victory (e.g., runs or wickets). The venue where the match was played is represented by Ground column. Match Date represents the specific date of the match.
2. Captain-Specific Details: India Captain contains the name of the Indian captain for the match. Indian_Captaincy_Style categorizes the captain’s leadership style as either Aggressive or Defensive. Opponent Captain represents the captain of the opposing team. And Toss Result shows the Toss outcome, including which team won the toss and their decision to bat or field.
3. Performance Metrics: Powerplay Runs India represents the runs scored by India in the first six overs ( called as powerplay). Powerplay Runs Opponent represents the runs scored by the opposing team in the first six overs. Relative Opponent Strength represents a derived metric representing the historical win percentage of the opponent team.
4. Derived Features: This includes Powerplay Impact Score which is a composite score that is used to quantify India's powerplay dominance in terms of both run scoring and wicket conservation. Win Type represents a binary indicator denoting whether the win was margin-based (runs = 1, wickets = 0). India_Won_Toss represents a binary indicator for whether India won the toss or not. And Margin Value is a numerical representation of the victory margin (in runs or wickets).

### Suitability of Dataset:
This dataset provides a comprehensive view of match-level details, leadership styles, and team performance. By incorporating derived metrics like Powerplay Impact and Relative Opponent Strength, it enables an in depth analysis of how captaincy styles influence various performance dimensions. The temporal range (2006–2024) ensures a broad perspective, covering multiple captains and playing conditions.

## Data Acquisition
1. Match Details Scraping: Utilized BeautifulSoup to scrape match-level data from ESPN Cricinfo's year-wise records (2006–2024) Additionally, geographic information, such as the longitudinal and latitudinal coordinates of match venues, was retrieved using the Google Maps API, facilitated by an API key. This data was used to create an informative world map plot, enriching the visual analysis of match locations.
2. Captaincy Data Scraping: Extracted captaincy performance data (tenure, matches, and win percentages) from ESPN Cricinfo's individual captaincy records.
3. Derived Data: Merged datasets to map captaincy styles to individual matches. And calculated advanced features like Powerplay Impact and Relative Opponent Strength.
4. Technical Complexity: First we scraped data dynamically for multiple years and pages. Then extracted powerplay performance and toss outcomes from scorecard URLs. And mapped captaincy styles using custom logic and external datasets.
