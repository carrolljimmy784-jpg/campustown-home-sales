# Agent log

Add a dated entry each time you work with your AI coding agent, with the newest entry at the bottom. Each entry records what you asked the agent, what it produced, and what you checked or changed. Paste your key prompts in exactly as you typed them. Include at least one time the agent got something wrong, and how you caught it.

Copy this outline for each entry:

```markdown
## YYYY-MM-DD: What you worked on

- **Asked:** "Paste your prompt here."
- **Agent produced:** What it made or changed.
- **Checked or changed:** How you checked it, and what you fixed.
```
## 2026-11-16: Reviewed dataset documentation and planned analysis and created first dashboard

Asked: "Read AGENTS.md and docs/data_description_sheet.md completely before making any changes.
Analyze data/college_town_home_sales.csv and explain:

Which columns are most useful for a housing market dashboard.
Which columns should be avoided based on the documentation.
Any data quality issues that must be handled.
Three possible dashboard concepts that would fit this assignment.
Do not modify any files.

First provide your analysis and a proposed plan. Wait for approval before making changes."

Agent produced: Reviewed the project instructions and dataset documentation, identified useful columns such as city, university, sale_price, sale_date, and miles_to_campus, advised against relying on home_type and address-based analysis, highlighted data quality concerns such as sales below $10,000 and missing date values, and proposed a College Town Housing Explorer dashboard focused on comparing housing markets across college towns.

Checked or changed: Compared the recommendations against the dataset documentation, confirmed that sales below $10,000 would be excluded from price-based calculations, and selected median sale price as the primary metric because the dataset contains extreme outliers.

Asked: "Based on the plan we selected, create Version 1 of the website.

Replace the placeholder index.html with a website called 'College Town Housing Explorer.'

Requirements:

Load data from data/college_town_home_sales.csv.
Exclude sales below $10,000 from all price calculations.
Display total sales analyzed.
Display number of cities.
Display number of universities.
Display overall median sale price.
Add a bar chart showing median sale price by city.
Add a data notes section explaining the filtering rule.
Use HTML, CSS, JavaScript, and Chart.js only.
Keep the site compatible with GitHub Pages.
Before editing files, explain your implementation plan and wait for approval."

Agent produced: Replaced the placeholder page with a responsive dashboard that loads the CSV file, filters out sales below $10,000, calculates summary statistics directly from the dataset, displays overall metrics, and visualizes median sale prices by city using a Chart.js horizontal bar chart. The page also includes responsive styling and a data notes section documenting the filtering rule.
Checked or changed: Reviewed the generated code, verified that data is loaded from the CSV file rather than hard-coded values, confirmed that sales below $10,000 are excluded from all price calculations, checked that median rather than average sale price is used for the primary visualization, and verified that the implementation follows the requirements in AGENTS.md.

## 2026-11-17: Add City Explorer Feature while following all rules
asked: "Read AGENTS.md and docs/data_description_sheet.md before making changes.

Add a city explorer section below the existing chart.

Requirements:
- Add a dropdown containing all cities in the filtered dataset.
- When a city is selected, display:
  - city name
  - associated university
  - number of sales
  - median sale price
  - average sale price
  - median miles_to_campus
- Use the same rule as the rest of the dashboard (exclude sales below $10,000).
- Match the existing visual style.
- Explain your implementation plan before editing files."

Agent Produced:"Added a city explorer below the chart in index.html. Its dropdown is populated from cities with qualifying sales; selecting one shows its associated university, sale count, median and average sale price, and median campus distance. All figures use sales priced at $10,000 or more. A note also flags that high prices can affect averages."

Asked: "Read AGENTS.md and docs/data_description_sheet.md before making changes.

Add a second Chart.js visualization comparing median sale prices by university.

Use the existing filtered dataset and sort universities from highest to lowest median price.

Match the existing styling and responsiveness.

Then, 
Add a histogram showing the distribution of sale prices after excluding sales below $10,000.

Include a short explanation of why median price is emphasized over average price.

- Use the same rule as the rest of the dashboard (exclude sales below $10,000).
- Match the existing visual style.
- Explain your implementation plan before editing files."

Agent Produced:"Added two responsive Chart.js visualizations in index.html: university median sale prices sorted high-to-low, and a histogram of qualifying sales using logarithmically spaced price ranges. Both use the existing $10,000 minimum-price filter. The university chart also explains why medians are less affected by unusually high prices than averages.

I checked the chart setup and filter in the source; I didn’t run a browser test. After publishing through GitHub Pages, open the site and scroll below the city chart to view both visualizations."