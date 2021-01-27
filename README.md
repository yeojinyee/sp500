# sp500

## About The Project
A S&P500 stock price web app is created using Streamlit. It is an open-source Python library that makes it easy to create and share beautiful, custom and interactive web apps for machine learning and data science.

The list of S&P500 companies has been web scrapped from the table provided on wikipedia. The sectors are then grouped and sorted.
```
@st.cache
def load_data():
    url = 'https://en.wikipedia.org/wiki/List_of_S%26P_500_companies'
    html = pd.read_html(url, header = 0)
    df = html[0]
    return df
```

User can multi-select the sectors from the side bar. 

```
selected_sector = st.sidebar.multiselect('Sector', sorted_sector_unique)
```
![](images/s%26p500%20dashboard.PNG)

User can select the number of chart to be shown.
![](images/closing%20price%20chart.PNG)

## Built With
* Streamlit
* Python
* Yahoo Finance
