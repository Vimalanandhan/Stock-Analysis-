Here’s a `README.md` file for your project that includes an overview, setup instructions, and details about the libraries used:

```markdown
# Data Visualization of Stock Price Increases for Major Tech Companies

## Project Overview

This project involves creating a horizontal bar chart to visualize the percent increase in stock prices from June 2012 to June 2017 for four major tech companies. The chart uses vertical grid lines to enhance readability and facilitate comparison between companies.

## Libraries Used

- **Altair**: For creating and customizing interactive and informative visualizations.
- **Pandas**: For data manipulation and preparation.
- **NumPy**: For numerical operations and data transformations.
- **Jupyter Notebook**: For interactive exploration and presentation of the visualization.

## Setup Instructions

To run this project, you need to have the following libraries installed. You can install them using pip:

```bash
pip install altair pandas numpy jupyter
```

## Usage

1. **Prepare Data**: Ensure you have your stock price data in a format similar to the example provided in the script.
2. **Run the Notebook**:
   - Open Jupyter Notebook in your terminal by running `jupyter notebook`.
   - Navigate to the notebook file (`.ipynb`) and open it.
   - Execute the cells to generate the bar chart visualization.

## Example Code

Here is a basic example of how to create the horizontal bar chart using Altair:

```python
import pandas as pd
import altair as alt

# Sample data
data = {
    'Company': ['Company A', 'Company B', 'Company C', 'Company D'],
    'Percent Increase': [50, 80, 60, 40]  # Replace with actual percent increase values
}
df = pd.DataFrame(data)

# Create the chart
chart = alt.Chart(df).mark_bar().encode(
    y=alt.Y('Company:N', sort='-x', title=None),
    x=alt.X('Percent Increase:Q', title='Percent Increase (%)'),
    color='Company:N',
    tooltip=['Company:N', 'Percent Increase:Q']
).properties(
    title='Percent Increase in Stock Price (June 2012 to June 2017)',
    width=600
).configure_axis(
    grid=True,
    gridColor='lightgray',
    gridDash=[2,2],
    tickSize=0
).configure_view(
    strokeWidth=0
)

chart
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or comments, please reach out to vimalsivanandham@gmail.com
```

Feel free to adjust the content to better fit your project's specifics or personal preferences!
