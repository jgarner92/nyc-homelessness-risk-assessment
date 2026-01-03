# nyc-homelessness-risk-assessment

This algorithm generates a daily **homelessness risk score** for each ZIP code in New York City, helping nonprofits and outreach teams prioritize areas for intervention. It combines multiple public-data sources, including:

- **311 complaints related to homelessness**, capturing recent and recurring reports of unsheltered individuals  
- **Weather data**, accounting for extreme temperatures, precipitation, and other environmental hazards  
- **Historical housing patterns**, highlighting locations with persistent or seasonal risk  
- **Shelter location data**, providing context on nearby resources and service gaps  

The algorithm produces a **risk score per ZIP code** that reflects both immediate and ongoing factors contributing to vulnerability. Each high-risk area is accompanied by **human-readable explanations**, so users can understand why a location has been flagged and make informed decisions.  

Outputs are visualized as an **interactive heatmap**, highlighting the areas of greatest concern each day. The platform is designed to be **ethical, transparent, and fully privacy-conscious**, relying only on aggregated public data and avoiding individual profiling.  

This tool provides actionable insights to support **street outreach teams, shelters, and nonprofits** in efficiently allocating resources and responding to homelessness in New York City.

## How It Works

The homelessness risk assessment algorithm follows a simple, transparent workflow:

1. **Data Collection**  
   - Pulls **311 homelessness complaints**, **weather data**, **historical housing patterns**, and **shelter locations** from public sources.  

2. **Data Processing & Feature Engineering**  
   - Aggregates complaints and historical data by ZIP code.  
   - Applies time decay to recent 311 reports to emphasize current risk.  
   - Computes environmental risk factors from weather (temperature, precipitation, extreme events).  

3. **Risk Scoring**  
   - Combines the processed features into a **composite risk score** per ZIP code.  
   - Weights factors to balance immediate risk (recent complaints, extreme weather) and persistent vulnerability (historical patterns, shelter gaps).  

4. **Explanation Generation**  
   - Identifies the **top contributing factors** for each high-risk ZIP code.  
   - Produces human-readable explanations to help outreach teams understand why an area is flagged.  

5. **Visualization**  
   - Displays the results on an **interactive heatmap** of NYC, highlighting areas of greatest concern each day.  
   - Allows nonprofits and outreach teams to **prioritize interventions** effectively.


