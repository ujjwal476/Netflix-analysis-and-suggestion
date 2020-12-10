## Finding count of high-rated movie and low-rated movie



```python
#Plotly chart - Bar chart to see the count of movies and shows in our data
#x-axis will show the content type and y-axis will show the count of content

color = ['steelblue','firebrick']
data = [go.Bar(x=['High-rated','Low-rated'],
y=[copy_count_rated.loc[copy_count_rated['rating_standard']=='High-rated'].shape[0],
   copy_count_rated.loc[copy_count_rated['rating_standard']=='Low-rated'].shape[0]],
    #marker_color =copy_count_rated['rating_num']
   marker=dict(color=color) 
    
)]
#create the layout of the chart by defining titles for chart, x-axis and y-axis
layout = go.Layout(title='Netflix content rating analysis',
            xaxis=dict(title='Type of ratings'),
            yaxis=dict(title='Total no. of ratings'),
            height =500,
            width = 700)

#Imbed data and layout into charts figure using Figure function
fig = go.Figure(data=data, layout=layout)
#Use plot function of plotly to visualize the data
fig.show()
```


<div>                            <div id="d2a3f26d-713f-489e-9fff-898fa75838be" class="plotly-graph-div" style="height:500px; width:700px;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("d2a3f26d-713f-489e-9fff-898fa75838be")) {                    Plotly.newPlot(                        "d2a3f26d-713f-489e-9fff-898fa75838be",                        [{"marker": {"color": ["steelblue", "firebrick"]}, "type": "bar", "x": ["High-rated", "Low-rated"], "y": [363, 401]}],                        {"height": 500, "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Netflix content rating analysis"}, "width": 700, "xaxis": {"title": {"text": "Type of ratings"}}, "yaxis": {"title": {"text": "Total no. of ratings"}}},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('d2a3f26d-713f-489e-9fff-898fa75838be');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>



```python
#making copy to new dataframe so that the edit do not change the original dataframe
copy_count_rated_country =copy_count_rated.copy()

#replacing abbreviation of country names with their full name
copy_count_rated_country = copy_count_rated_country.replace({'country': {'gb':'United Kingdom', 'ar':'Argentina', 'hk':'Hongkong','be':'Belgium','hu':'Hungary','cz':'cezhrepublic',
                  'de':'Germany','jp':'Japan','se':'Sweden','ru':'Russia','au':'Australia','nl':'Netherland','usa':'United States','in':'India',
                  'lt':'Luthvania','br':'Brazil','mx':'Mexico','sg':'Singapore','fr':'France','kr':'South Korea','it':'Italy'}})
copy_count_rated_country.head(1)

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>type</th>
      <th>title</th>
      <th>director</th>
      <th>cast</th>
      <th>country</th>
      <th>date_added</th>
      <th>release_year</th>
      <th>rating</th>
      <th>duration</th>
      <th>listed_in</th>
      <th>description</th>
      <th>added_year</th>
      <th>added_month</th>
      <th>rating_num</th>
      <th>unogsdate</th>
      <th>rating_standard</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>70234439</td>
      <td>TV Show</td>
      <td>Transformers Prime</td>
      <td>NaN</td>
      <td>Peter Cullen, Sumalee Montano, Frank Welker, J...</td>
      <td>United States</td>
      <td>2018-09-08</td>
      <td>2013</td>
      <td>TV-Y7-FV</td>
      <td>1 Season</td>
      <td>Kids' TV</td>
      <td>With the help of three human allies, the Autob...</td>
      <td>2018.0</td>
      <td>9.0</td>
      <td>7.8</td>
      <td>NaT</td>
      <td>High-rated</td>
    </tr>
  </tbody>
</table>
</div>




```python
#acessing specific columns
rating_analysis_country_filter = copy_count_rated_country.loc[:,['netflixid','type','title','country','rating','duration','listed_in','description','rating_num','rating_standard']]
print(rating_analysis_country_filter.shape)

rating_analysis_country_filter.head(3)

```

    (764, 10)





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>type</th>
      <th>title</th>
      <th>country</th>
      <th>rating</th>
      <th>duration</th>
      <th>listed_in</th>
      <th>description</th>
      <th>rating_num</th>
      <th>rating_standard</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>70234439</td>
      <td>TV Show</td>
      <td>Transformers Prime</td>
      <td>United States</td>
      <td>TV-Y7-FV</td>
      <td>1 Season</td>
      <td>Kids' TV</td>
      <td>With the help of three human allies, the Autob...</td>
      <td>7.8</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80045922</td>
      <td>Movie</td>
      <td>6 Years</td>
      <td>United States</td>
      <td>NR</td>
      <td>80 min</td>
      <td>Dramas, Independent Movies, Romantic Movies</td>
      <td>As a volatile young couple who have been toget...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>2</th>
      <td>80182115</td>
      <td>Movie</td>
      <td>Long Shot</td>
      <td>United States</td>
      <td>TV-14</td>
      <td>40 min</td>
      <td>Documentaries</td>
      <td>When Juan Catalan is arrested for a murder he ...</td>
      <td>7.4</td>
      <td>High-rated</td>
    </tr>
  </tbody>
</table>
</div>




```python
#country_high_rating_count = x
# in country column there are more than one country in a row, so making separate rows for each country 
#so creating a function and using for loop to separate the each country in different rows
def get_each_country(x):
    ids_list =[]
    countries_df=pd.DataFrame()   #making a new empty dataframe
    x['country'] = x['country'].astype(str)   #making sure that all values in country columns are in string format
    for i in range(len(x)):   #using for loop
        nid = x.iloc[i,0]                     #getting particular values
        typ = x.iloc[i,1]                       #getting particular values
        titl=x.iloc[i,2]                     #getting particular values
        value = x.iloc[i,3]                     #getting particular values
        rating_typ = x.iloc[i,4]                  #getting particular values
        dura = x.iloc[i,5]
        genre = x.iloc[i,6]
        desc = x.iloc[i,7]
        rate = x.iloc[i,8]
        rate_std = x.iloc[i,9]                       #getting particular values
        if ',' in value:                             #checking if comma is in the specific row value 
            splitted= value.split(',')         #splitting the value  separting with commas
            ids_list.append(nid)          #getting id of that value
            if len(splitted)==2:          #checking how many values were separated with commas (condition with 2 values)
                #making a list of series to append later in new dataframe
                listOfSeries = [pd.Series([nid, typ, titl, splitted[0].strip(),rating_typ, dura,genre,desc,rate,rate_std], index=x.columns ) , #making a complete row
                        pd.Series([nid, typ, titl, splitted[1].strip(),rating_typ, dura,genre,desc,rate,rate_std], index=x.columns )]          #making a complete row
            elif len(splitted) ==3:         # 3 country names separated with commas
                listOfSeries = [pd.Series([nid, typ, titl, splitted[0].strip(),rating_typ, dura,genre,desc,rate,rate_std], index=x.columns ) ,#making a complete row
                        pd.Series([nid, typ, titl, splitted[1].strip(),rating_typ, dura,genre,desc,rate,rate_std], index=x.columns ),#making a complete row
                        pd.Series([nid, typ, titl, splitted[2].strip(),rating_typ, dura,genre,desc,rate,rate_std], index=x.columns )]#making a complete row
            else:          #more tha three countries 
                listOfSeries = [pd.Series([nid, typ, titl, splitted[0].strip(),rating_typ, dura,genre,desc,rate,rate_std], index=x.columns ) , #making a complete row
                        pd.Series([nid, typ, titl, splitted[1].strip(),rating_typ, dura,genre,desc,rate,rate_std], index=x.columns ),#making a complete row
                        pd.Series([nid, typ, titl, splitted[2].strip(),rating_typ, dura,genre,desc,rate,rate_std], index=x.columns ), #making a complete row
                        pd.Series([nid, typ, titl, splitted[3].strip(),rating_typ, dura,genre,desc,rate,rate_std], index=x.columns )]#making a complete row

            countries_df = countries_df.append(listOfSeries , ignore_index=True) #appending all these rows in a new dataframe

    #print(len(id_list))
    #print(len(country_df))
    #print(country_df)


    countries_index = x.set_index('netflixid') #setting index in the dataframe that is passed to this funntion
    #country_index

    for each in range(len(x)):                
        if x.iloc[each][0] in ids_list:    #checking if the each id is in the appended list above
            val = x.iloc[each][0]            #getting id as val
            countries_index = countries_index.drop(val,axis=0) #dropping the val(id)from the dataframe
        else:
            continue
    countries_index  =   countries_index.reset_index() #resetting the index 


    countries_index = countries_index.append(countries_df, ignore_index =True)  #appending the index 
    return countries_index    #returning the dataframe

```


```python
rating_analysis_expand = get_each_country(rating_analysis_country_filter)  #calling above function to get each country rows separate
#print(rating_analysis_expand.shape)
rating_analysis_expand.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>type</th>
      <th>title</th>
      <th>country</th>
      <th>rating</th>
      <th>duration</th>
      <th>listed_in</th>
      <th>description</th>
      <th>rating_num</th>
      <th>rating_standard</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>70234439</td>
      <td>TV Show</td>
      <td>Transformers Prime</td>
      <td>United States</td>
      <td>TV-Y7-FV</td>
      <td>1 Season</td>
      <td>Kids' TV</td>
      <td>With the help of three human allies, the Autob...</td>
      <td>7.8</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80045922</td>
      <td>Movie</td>
      <td>6 Years</td>
      <td>United States</td>
      <td>NR</td>
      <td>80 min</td>
      <td>Dramas, Independent Movies, Romantic Movies</td>
      <td>As a volatile young couple who have been toget...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>2</th>
      <td>80182115</td>
      <td>Movie</td>
      <td>Long Shot</td>
      <td>United States</td>
      <td>TV-14</td>
      <td>40 min</td>
      <td>Documentaries</td>
      <td>When Juan Catalan is arrested for a murder he ...</td>
      <td>7.4</td>
      <td>High-rated</td>
    </tr>
  </tbody>
</table>
</div>




```python
#len(rating_analysis_expand.rating_standard.to_list())

#for i in range(len(rating_analysis_expand.rating_standard.to_list())):
#    print(rating_analysis_expand.rating_standard[i])
```


```python
# getting the rows that belongs to high-rated 
country_high_rating = rating_analysis_expand[rating_analysis_expand.rating_standard == 'High-rated']
#getting with high-rated
country_high_rating_count= country_high_rating.loc[:,['netflixid','country']]
high_rating_by_country = country_high_rating_count.rename(columns={'country':'high-rating_country'})
high_rating_by_country
#counting countries that has more high-rated
ccount_high = high_rating_by_country['high-rating_country'].value_counts()
#ccount_high
```


```python
 #getting the rows that belongs to low-rated
country_low_rating = rating_analysis_expand[rating_analysis_expand.rating_standard == 'Low-rated']
country_low_rating_count= country_low_rating.loc[:,['netflixid','country']]
#getting countries with low-rated and renaming the columns
low_rating_by_country = country_low_rating_count.rename(columns={'country':'low-rating_country'})
#counting the total number of low-rated movies in that country
ccount_low = low_rating_by_country['low-rating_country'].value_counts()

```


```python
#concating high -rated dataframe and lowrated dataframe
rating_compare = pd.concat([ccount_high, ccount_low], axis=1)
rating_compare =rating_compare.reset_index()
#rating_compare
```


```python
#renaming the columns of concatenated dataframe
rating_compare_e =rating_compare.rename(columns={'index':'country',
                                                    'high-rating_country':'High-rated',
                                                    'low-rating_country':'Low-rated'})

rating_compare_e.iloc[:]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>country</th>
      <th>High-rated</th>
      <th>Low-rated</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>United States</td>
      <td>156.0</td>
      <td>171.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>United Kingdom</td>
      <td>53.0</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Canada</td>
      <td>24.0</td>
      <td>25.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Japan</td>
      <td>20.0</td>
      <td>38.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Hongkong</td>
      <td>14.0</td>
      <td>19.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Germany</td>
      <td>13.0</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>India</td>
      <td>12.0</td>
      <td>13.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>cezhrepublic</td>
      <td>11.0</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Argentina</td>
      <td>9.0</td>
      <td>11.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Belgium</td>
      <td>8.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Australia</td>
      <td>8.0</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Sweden</td>
      <td>8.0</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Hungary</td>
      <td>7.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Mexico</td>
      <td>7.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>France</td>
      <td>7.0</td>
      <td>19.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Russia</td>
      <td>6.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>nan</td>
      <td>5.0</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Netherland</td>
      <td>4.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Spain</td>
      <td>4.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Colombia</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>20</th>
      <td>China</td>
      <td>3.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Ireland</td>
      <td>3.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Denmark</td>
      <td>3.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Brazil</td>
      <td>3.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Hong Kong</td>
      <td>3.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>25</th>
      <td>New Zealand</td>
      <td>2.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>26</th>
      <td>ca</td>
      <td>2.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Turkey</td>
      <td>2.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Singapore</td>
      <td>2.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Taiwan</td>
      <td>2.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Bermuda</td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Luthvania</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>32</th>
      <td>is</td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Israel</td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>34</th>
      <td>Philippines</td>
      <td>1.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Egypt</td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>36</th>
      <td>sk</td>
      <td>1.0</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>37</th>
      <td>Ukraine</td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Netherlands</td>
      <td>1.0</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>39</th>
      <td>Ecuador</td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>40</th>
      <td>Norway</td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>41</th>
      <td></td>
      <td>1.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>42</th>
      <td>South Korea</td>
      <td>1.0</td>
      <td>6.0</td>
    </tr>
    <tr>
      <th>43</th>
      <td>Italy</td>
      <td>NaN</td>
      <td>13.0</td>
    </tr>
    <tr>
      <th>44</th>
      <td>th</td>
      <td>NaN</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>45</th>
      <td>United Arab Emirates</td>
      <td>NaN</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Qatar</td>
      <td>NaN</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>47</th>
      <td>Poland</td>
      <td>NaN</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>48</th>
      <td>Bulgaria</td>
      <td>NaN</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>49</th>
      <td>pt</td>
      <td>NaN</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>50</th>
      <td>Pakistan</td>
      <td>NaN</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>51</th>
      <td>South Africa</td>
      <td>NaN</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>52</th>
      <td>gr</td>
      <td>NaN</td>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
#using melt functionality to set the columna name as valuues
rating_compare_edit = rating_compare_e.melt(id_vars=['country'], value_vars=['High-rated', 'Low-rated'])
#rating_compare_edit.columns.values
#rating_compare_edit.country.to_list()


#using iloc to get specific countries
rating_compare_country = rating_compare_edit.iloc[[0,53,1,54,2,55,3,56,4,57,5,58,6,59,7,60,12,65],:]
rating_compare_country
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>country</th>
      <th>variable</th>
      <th>value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>United States</td>
      <td>High-rated</td>
      <td>156.0</td>
    </tr>
    <tr>
      <th>53</th>
      <td>United States</td>
      <td>Low-rated</td>
      <td>171.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>United Kingdom</td>
      <td>High-rated</td>
      <td>53.0</td>
    </tr>
    <tr>
      <th>54</th>
      <td>United Kingdom</td>
      <td>Low-rated</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Canada</td>
      <td>High-rated</td>
      <td>24.0</td>
    </tr>
    <tr>
      <th>55</th>
      <td>Canada</td>
      <td>Low-rated</td>
      <td>25.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Japan</td>
      <td>High-rated</td>
      <td>20.0</td>
    </tr>
    <tr>
      <th>56</th>
      <td>Japan</td>
      <td>Low-rated</td>
      <td>38.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Hongkong</td>
      <td>High-rated</td>
      <td>14.0</td>
    </tr>
    <tr>
      <th>57</th>
      <td>Hongkong</td>
      <td>Low-rated</td>
      <td>19.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Germany</td>
      <td>High-rated</td>
      <td>13.0</td>
    </tr>
    <tr>
      <th>58</th>
      <td>Germany</td>
      <td>Low-rated</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>India</td>
      <td>High-rated</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>59</th>
      <td>India</td>
      <td>Low-rated</td>
      <td>13.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>cezhrepublic</td>
      <td>High-rated</td>
      <td>11.0</td>
    </tr>
    <tr>
      <th>60</th>
      <td>cezhrepublic</td>
      <td>Low-rated</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Hungary</td>
      <td>High-rated</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>65</th>
      <td>Hungary</td>
      <td>Low-rated</td>
      <td>7.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
rating_compare_country
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>country</th>
      <th>variable</th>
      <th>value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>United States</td>
      <td>High-rated</td>
      <td>156.0</td>
    </tr>
    <tr>
      <th>53</th>
      <td>United States</td>
      <td>Low-rated</td>
      <td>171.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>United Kingdom</td>
      <td>High-rated</td>
      <td>53.0</td>
    </tr>
    <tr>
      <th>54</th>
      <td>United Kingdom</td>
      <td>Low-rated</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Canada</td>
      <td>High-rated</td>
      <td>24.0</td>
    </tr>
    <tr>
      <th>55</th>
      <td>Canada</td>
      <td>Low-rated</td>
      <td>25.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Japan</td>
      <td>High-rated</td>
      <td>20.0</td>
    </tr>
    <tr>
      <th>56</th>
      <td>Japan</td>
      <td>Low-rated</td>
      <td>38.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Hongkong</td>
      <td>High-rated</td>
      <td>14.0</td>
    </tr>
    <tr>
      <th>57</th>
      <td>Hongkong</td>
      <td>Low-rated</td>
      <td>19.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Germany</td>
      <td>High-rated</td>
      <td>13.0</td>
    </tr>
    <tr>
      <th>58</th>
      <td>Germany</td>
      <td>Low-rated</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>India</td>
      <td>High-rated</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>59</th>
      <td>India</td>
      <td>Low-rated</td>
      <td>13.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>cezhrepublic</td>
      <td>High-rated</td>
      <td>11.0</td>
    </tr>
    <tr>
      <th>60</th>
      <td>cezhrepublic</td>
      <td>Low-rated</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Hungary</td>
      <td>High-rated</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>65</th>
      <td>Hungary</td>
      <td>Low-rated</td>
      <td>7.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
#plotting the data into sunburst using plotly
fig = px.sunburst(rating_compare_country, path=['country', 'variable'], values='value', color='country',
                  title='Analysis of Netflix ratings by country', height = 700, width =900)
fig.show()
```


<div>                            <div id="b44c3471-2420-4228-ba2e-b6c19e85a119" class="plotly-graph-div" style="height:700px; width:900px;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("b44c3471-2420-4228-ba2e-b6c19e85a119")) {                    Plotly.newPlot(                        "b44c3471-2420-4228-ba2e-b6c19e85a119",                        [{"branchvalues": "total", "customdata": [["India"], ["Japan"], ["Hongkong"], ["Germany"], ["cezhrepublic"], ["Canada"], ["United States"], ["cezhrepublic"], ["Hungary"], ["India"], ["United Kingdom"], ["United States"], ["Hungary"], ["Hongkong"], ["Germany"], ["Canada"], ["Japan"], ["United Kingdom"], ["Canada"], ["Germany"], ["Hongkong"], ["Hungary"], ["India"], ["Japan"], ["United Kingdom"], ["United States"], ["cezhrepublic"]], "domain": {"x": [0.0, 1.0], "y": [0.0, 1.0]}, "hovertemplate": "labels=%{label}<br>value=%{value}<br>parent=%{parent}<br>id=%{id}<br>country=%{customdata[0]}<extra></extra>", "ids": ["India/High-rated", "Japan/High-rated", "Hongkong/Low-rated", "Germany/Low-rated", "cezhrepublic/High-rated", "Canada/Low-rated", "United States/Low-rated", "cezhrepublic/Low-rated", "Hungary/Low-rated", "India/Low-rated", "United Kingdom/High-rated", "United States/High-rated", "Hungary/High-rated", "Hongkong/High-rated", "Germany/High-rated", "Canada/High-rated", "Japan/Low-rated", "United Kingdom/Low-rated", "Canada", "Germany", "Hongkong", "Hungary", "India", "Japan", "United Kingdom", "United States", "cezhrepublic"], "labels": ["High-rated", "High-rated", "Low-rated", "Low-rated", "High-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "Low-rated", "Low-rated", "Canada", "Germany", "Hongkong", "Hungary", "India", "Japan", "United Kingdom", "United States", "cezhrepublic"], "marker": {"colors": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#FFA15A", "#B6E880", "#636efa", "#FF97FF", "#FF6692", "#B6E880", "#00cc96", "#ab63fa", "#19d3f3", "#EF553B", "#FF97FF", "#19d3f3", "#ab63fa", "#00cc96", "#B6E880", "#636efa", "#EF553B", "#FF97FF", "#FF6692", "#FFA15A"]}, "name": "", "parents": ["India", "Japan", "Hongkong", "Germany", "cezhrepublic", "Canada", "United States", "cezhrepublic", "Hungary", "India", "United Kingdom", "United States", "Hungary", "Hongkong", "Germany", "Canada", "Japan", "United Kingdom", "", "", "", "", "", "", "", "", ""], "type": "sunburst", "values": [12.0, 20.0, 19.0, 10.0, 11.0, 25.0, 171.0, 12.0, 7.0, 13.0, 53.0, 156.0, 7.0, 14.0, 13.0, 24.0, 38.0, 12.0, 49.0, 23.0, 33.0, 14.0, 25.0, 58.0, 65.0, 327.0, 23.0]}],                        {"height": 700, "legend": {"tracegroupgap": 0}, "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Analysis of Netflix ratings by country"}, "width": 900},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('b44c3471-2420-4228-ba2e-b6c19e85a119');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>


## Popular Genres in these countries


```python
# getting a glance at types of genres we have in our dataframe
rating_analysis_expand.listed_in.to_list()

rating_analysis_expand.columns.values
```




    array(['netflixid', 'type', 'title', 'country', 'rating', 'duration',
           'listed_in', 'description', 'rating_num', 'rating_standard'],
          dtype=object)




```python
# in our datafraem we noticed that we had many genres in each row so separating it to process and analyze it.
#so using the function to separate the values by genre and making them individual rows
def get_each_genre(x):
    id_list =[]
    genre_df=pd.DataFrame()    #creaing new dataframe
    x['listed_in'] = x['listed_in'].astype(str)   #converting ito string format
    for i in range(len(x)):       #using for loop
        nid = x.iloc[i,0]  #accesing specific value
        typ = x.iloc[i,1]      #accesing specific value
        titl=x.iloc[i,2]         #accesing specific value
        country = x.iloc[i,3]        #accesing specific value
        rating_typ = x.iloc[i,4]#accesing specific value
        dura = x.iloc[i,5]          #accesing specific value
        value = x.iloc[i,6]         #accesing specific value
        desc = x.iloc[i,7]          #accesing specific value
        rate = x.iloc[i,8]          #accesing specific value
        rate_std = x.iloc[i,9]       #accesing specific value
        if ',' in value:        #checking for the comma in the value to split it accordingly
            splitted= value.split(',')  #splotting th value
            id_list.append(nid)
            if len(splitted)==2:    #making a new series for more than two generes in each row
                listOfSeries = [pd.Series([nid, typ, titl, country,rating_typ, dura,splitted[0].strip(),desc,rate,rate_std], index=x.columns ) ,
                        pd.Series([nid, typ, titl, country,rating_typ, dura,splitted[1].strip(),desc,rate,rate_std], index=x.columns )]
            elif len(splitted) ==3:   #making a new series for more than two generes in each row
                listOfSeries = [pd.Series([nid, typ, titl, country,rating_typ, dura,splitted[0].strip(),desc,rate,rate_std], index=x.columns ) ,
                        pd.Series([nid, typ, titl, country,rating_typ, dura,splitted[1].strip(),desc,rate,rate_std], index=x.columns ),
                        pd.Series([nid, typ, titl, country,rating_typ, dura,splitted[2].strip(),desc,rate,rate_std], index=x.columns )]
            

            genre_df = genre_df.append(listOfSeries , ignore_index=True)  #appending the dataframe with new rows

    #print(len(id_list))
    #print(len(country_df))
    #print(country_df)

    
   
    
    countries_genre_index = x.set_index('netflixid')  #setting the index
    #countries_genre_index
    id_list_final = set(id_list)     #removing duplicate items in the list by making it set type
    
    for each in id_list_final:
        countries_genre_index = countries_genre_index.drop(each, axis = 0)  #dropping the rows that have been repeated in another dataframe
        
    
    countries_genre_index  =   countries_genre_index.reset_index()  #resetting index 
    countries_genre_index = countries_genre_index.append(genre_df, ignore_index =True) #appending the new dataframe
    return countries_genre_index #returning the cleaned dataframe 

```


```python
rating_analysis_genre = get_each_genre(rating_analysis_expand)  #calling the function to process the genre columns
rating_analysis_genre
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>type</th>
      <th>title</th>
      <th>country</th>
      <th>rating</th>
      <th>duration</th>
      <th>listed_in</th>
      <th>description</th>
      <th>rating_num</th>
      <th>rating_standard</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>70234439</td>
      <td>TV Show</td>
      <td>Transformers Prime</td>
      <td>United States</td>
      <td>TV-Y7-FV</td>
      <td>1 Season</td>
      <td>Kids' TV</td>
      <td>With the help of three human allies, the Autob...</td>
      <td>7.8</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80182115</td>
      <td>Movie</td>
      <td>Long Shot</td>
      <td>United States</td>
      <td>TV-14</td>
      <td>40 min</td>
      <td>Documentaries</td>
      <td>When Juan Catalan is arrested for a murder he ...</td>
      <td>7.4</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>2</th>
      <td>81001809</td>
      <td>Movie</td>
      <td>Lessons from a School Shooting: Notes from Dun...</td>
      <td>United States</td>
      <td>TV-PG</td>
      <td>24 min</td>
      <td>Documentaries</td>
      <td>Two priests – one from Dunblane, Scotland, the...</td>
      <td>5.8</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>3</th>
      <td>80005444</td>
      <td>Movie</td>
      <td>Print the Legend</td>
      <td>United States</td>
      <td>TV-14</td>
      <td>100 min</td>
      <td>Documentaries</td>
      <td>This award-winning, original documentary chron...</td>
      <td>7.1</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>4</th>
      <td>80097321</td>
      <td>Movie</td>
      <td>Audrie &amp; Daisy</td>
      <td>United States</td>
      <td>TV-14</td>
      <td>99 min</td>
      <td>Documentaries</td>
      <td>In this wrenching documentary, two teens are s...</td>
      <td>7.2</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1439</th>
      <td>70184127</td>
      <td>TV Show</td>
      <td>Big Bad Beetleborgs</td>
      <td>Japan</td>
      <td>TV-Y7-FV</td>
      <td>2 Seasons</td>
      <td>TV Comedies</td>
      <td>When three teens free a spirit that offers to ...</td>
      <td>6.3</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>1440</th>
      <td>70180088</td>
      <td>TV Show</td>
      <td>The Garfield Show</td>
      <td>France</td>
      <td>TV-Y7</td>
      <td>3 Seasons</td>
      <td>Kids' TV</td>
      <td>Lazy, lasagna-loving fat cat Garfield lives li...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>1441</th>
      <td>70180088</td>
      <td>TV Show</td>
      <td>The Garfield Show</td>
      <td>France</td>
      <td>TV-Y7</td>
      <td>3 Seasons</td>
      <td>TV Comedies</td>
      <td>Lazy, lasagna-loving fat cat Garfield lives li...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>1442</th>
      <td>70180088</td>
      <td>TV Show</td>
      <td>The Garfield Show</td>
      <td>United States</td>
      <td>TV-Y7</td>
      <td>3 Seasons</td>
      <td>Kids' TV</td>
      <td>Lazy, lasagna-loving fat cat Garfield lives li...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>1443</th>
      <td>70180088</td>
      <td>TV Show</td>
      <td>The Garfield Show</td>
      <td>United States</td>
      <td>TV-Y7</td>
      <td>3 Seasons</td>
      <td>TV Comedies</td>
      <td>Lazy, lasagna-loving fat cat Garfield lives li...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
  </tbody>
</table>
<p>1444 rows × 10 columns</p>
</div>


rating_analysis_genre.listed_in.value_counts()
rating_analysis_genre_Get = rating_analysis_genre.loc[rating_analysis_genre.rating_num == 0]
rating_analysis_genre_Get

```python
# there are too many genres so processing them to major genres accordingly by replace functionality
rating_analysis_genre['listed_in'] = rating_analysis_genre['listed_in'].replace(['Movie','Classic Movies',
                                'Kid\'s TV', 'Teens TV','Teen TV Shows','Kids\' TV',
                                'Stand-Up Comedy','TV Comedies','Stand-Up Comedy & Talk Shows',
                                'TV Dramas','Docuseries','TV Action & Adventure','Crime TV Shows',
                                'Children & Family Movies', 'Faith & Spirituality',
                                'Independent Movies','LGBTQ Movies',
                                'Thrillers','Horror','TV Horror','TV Thrillers',
                                'TV Sci-Fi & Fantasy','Romantic Moives','Romantic TV Shows',
                                'TV Mysteries','British TV Shows','Classic & Cult TV','Korean TV Shows','Reality TV',
                        'Anime Features'],
                        ['International Movies','International Movies',
                        'Kid\'s and Teen','Kid\'s and Teen','Kid\'s and Teen', 'Kid\'s and Teen',
                        'Comedies','Comedies','Comedies',
                         'Dramas','Documentaries','Action & Adventure','Crime',
                        'Family Movies','Family Movies',
                        'Independent Movies and LGBTQ Movies','Independent Movies and LGBTQ Movies',
                        'Thrillers & Horror','Thrillers & Horror','Thrillers & Horror','Thrillers & Horror',
                        'Sci-Fi & Fantasy','Romantic','Romantic',
                        'Other Shows','Other Shows','Other Shows','Other Shows','Other Shows',
                        'Anime Series'])


```


```python
#also replacing movie type to Movie type to make the data similar and comparable
rating_analysis_genre['type'] = rating_analysis_genre['type'].replace('movie','Movie')
```


```python

```


```python
#using treemap to analyze the quality content of netflix in each country by genre
fig = px.treemap(rating_analysis_genre, path=['country','listed_in','rating_standard'], 
                 title ='Content analysis of each country by genre',
                  color='rating_num', hover_data=['rating_num'], 
                  color_continuous_scale='RdBu')
fig.show()
```


<div>                            <div id="d9de7d85-1792-468a-8bc4-d7444e2cbb51" class="plotly-graph-div" style="height:525px; width:100%;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("d9de7d85-1792-468a-8bc4-d7444e2cbb51")) {                    Plotly.newPlot(                        "d9de7d85-1792-468a-8bc4-d7444e2cbb51",                        [{"branchvalues": "total", "customdata": [[8.3, 8.3], [7.5, 7.5], [8.8, 8.8], [7.8999999999999995, 7.8999999999999995], [7.75, 7.75], [8.8, 8.8], [8.8, 8.8], [8.16, 8.16], [8.108695652173912, 8.108695652173912], [8.185714285714287, 8.185714285714287], [8.2, 8.2], [7.400000000000001, 7.400000000000001], [8.1, 8.1], [7.1, 7.1], [7.6, 7.6], [7.8, 7.8], [7.699999999999999, 7.699999999999999], [8.0, 8.0], [7.1, 7.1], [8.0, 8.0], [7.3, 7.3], [7.8125, 7.8125], [7.65967741935484, 7.65967741935484], [7.324999999999999, 7.324999999999999], [8.0, 8.0], [8.266666666666667, 8.266666666666667], [8.466666666666667, 8.466666666666667], [8.45, 8.45], [8.0, 8.0], [8.1, 8.1], [8.285714285714286, 8.285714285714286], [8.321052631578945, 8.321052631578945], [7.550000000000001, 7.550000000000001], [8.2, 8.2], [8.2, 8.2], [8.0, 8.0], [7.640000000000001, 7.640000000000001], [8.0, 8.0], [8.1, 8.1], [7.2, 7.2], [7.3, 7.3], [7.3, 7.3], [7.6, 7.6], [8.4, 8.4], [7.949999999999999, 7.949999999999999], [7.696296296296295, 7.696296296296295], [7.733333333333334, 7.733333333333334], [7.5, 7.5], [7.9, 7.9], [7.5, 7.5], [8.8, 8.8], [7.65, 7.65], [7.45, 7.45], [7.5, 7.5], [7.5, 7.5], [7.9, 7.9], [7.266666666666666, 7.266666666666666], [7.9, 7.9], [7.5, 7.5], [7.800000000000001, 7.800000000000001], [8.0, 8.0], [7.1, 7.1], [7.4, 7.4], [7.9, 7.9], [7.983333333333334, 7.983333333333334], [8.047619047619047, 8.047619047619047], [7.2, 7.2], [7.4, 7.4], [7.0, 7.0], [7.125, 7.125], [7.55, 7.55], [7.7, 7.7], [8.2, 8.2], [7.5, 7.5], [7.6, 7.6], [7.75, 7.75], [7.2, 7.2], [8.1, 8.1], [7.45, 7.45], [7.3, 7.3], [7.5, 7.5], [7.388888888888889, 7.388888888888889], [7.3, 7.3], [7.300000000000001, 7.300000000000001], [7.6, 7.6], [7.1, 7.1], [7.4, 7.4], [7.3, 7.3], [8.4, 8.4], [8.049999999999999, 8.049999999999999], [8.0, 8.0], [7.4, 7.4], [7.7, 7.7], [7.0, 7.0], [8.3, 8.3], [8.1, 8.1], [8.185714285714287, 8.185714285714287], [8.149999999999999, 8.149999999999999], [8.25, 8.25], [7.95, 7.95], [8.185714285714285, 8.185714285714285], [8.6, 8.6], [7.2, 7.2], [7.4625, 7.4625], [7.2, 7.2], [7.525, 7.525], [8.6, 8.6], [7.35, 7.35], [7.7, 7.7], [7.2, 7.2], [7.6, 7.6], [7.5, 7.5], [7.6, 7.6], [8.0, 8.0], [7.75, 7.75], [7.1, 7.1], [8.4, 8.4], [7.3, 7.3], [7.442857142857143, 7.442857142857143], [7.875, 7.875], [8.115000000000002, 8.115000000000002], [8.000000000000002, 8.000000000000002], [8.4, 8.4], [7.95, 7.95], [8.1, 8.1], [7.8, 7.8], [7.6, 7.6], [8.2, 8.2], [8.8, 8.8], [8.1, 8.1], [8.024999999999999, 8.024999999999999], [8.05, 8.05], [8.3, 8.3], [8.149999999999999, 8.149999999999999], [8.033333333333333, 8.033333333333333], [7.6, 7.6], [8.1, 8.1], [7.3, 7.3], [7.3, 7.3], [8.2, 8.2], [7.566666666666666, 7.566666666666666], [7.6, 7.6], [7.2, 7.2], [7.3, 7.3], [8.8, 8.8], [7.978571428571429, 7.978571428571429], [8.355555555555556, 8.355555555555556], [8.225, 8.225], [8.225, 8.225], [7.8, 7.8], [8.7, 8.7], [8.157142857142857, 8.157142857142857], [7.635714285714286, 7.635714285714286], [8.1, 8.1], [7.800000000000001, 7.800000000000001], [7.545454545454546, 7.545454545454546], [7.8, 7.8], [7.5, 7.5], [7.7, 7.7], [8.34, 8.34], [8.2, 8.2], [8.8, 8.8], [7.75, 7.75], [8.05, 8.05], [8.55, 8.55], [7.15, 7.15], [7.436363636363635, 7.436363636363635], [7.4, 7.4], [7.0, 7.0], [5.8, 5.8], [6.233333333333333, 6.233333333333333], [5.159999999999999, 5.159999999999999], [5.375, 5.375], [5.75, 5.75], [5.1, 5.1], [6.0, 6.0], [3.9, 3.9], [5.8, 5.8], [5.444444444444444, 5.444444444444444], [2.875, 2.875], [5.6, 5.6], [5.8999999999999995, 5.8999999999999995], [5.3, 5.3], [6.233333333333333, 6.233333333333333], [4.372727272727273, 4.372727272727273], [6.5, 6.5], [5.15, 5.15], [5.45, 5.45], [3.9333333333333336, 3.9333333333333336], [5.6, 5.6], [4.066666666666666, 4.066666666666666], [5.55, 5.55], [6.333333333333333, 6.333333333333333], [5.6, 5.6], [6.6, 6.6], [0.0, 0.0], [0.0, 0.0], [0.0, 0.0], [3.6, 3.6], [4.2, 4.2], [0.0, 0.0], [5.819999999999999, 5.819999999999999], [3.9, 3.9], [5.2, 5.2], [5.200000000000001, 5.200000000000001], [6.45, 6.45], [2.3, 2.3], [4.6, 4.6], [6.3, 6.3], [5.85, 5.85], [6.1, 6.1], [6.4, 6.4], [6.4, 6.4], [6.1, 6.1], [5.8, 5.8], [6.05, 6.05], [5.9, 5.9], [5.8, 5.8], [0.0, 0.0], [6.15, 6.15], [6.25, 6.25], [1.2666666666666666, 1.2666666666666666], [6.199999999999999, 6.199999999999999], [5.4, 5.4], [5.2, 5.2], [5.925, 5.925], [2.0, 2.0], [5.866666666666667, 5.866666666666667], [5.0, 5.0], [4.930000000000001, 4.930000000000001], [6.0, 6.0], [6.7, 6.7], [6.6, 6.6], [6.5, 6.5], [6.3, 6.3], [6.6, 6.6], [6.3, 6.3], [5.3, 5.3], [4.2, 4.2], [6.25, 6.25], [6.0, 6.0], [6.3, 6.3], [5.847619047619047, 5.847619047619047], [0.0, 0.0], [5.566666666666667, 5.566666666666667], [5.5, 5.5], [4.9, 4.9], [0.0, 0.0], [6.4, 6.4], [6.3, 6.3], [6.433333333333334, 6.433333333333334], [5.668421052631579, 5.668421052631579], [0.0, 0.0], [3.4, 3.4], [4.7, 4.7], [6.7, 6.7], [5.5, 5.5], [6.1, 6.1], [3.4, 3.4], [6.05, 6.05], [5.325, 5.325], [0.0, 0.0], [6.5, 6.5], [5.823809523809525, 5.823809523809525], [6.075, 6.075], [6.1, 6.1], [5.533333333333332, 5.533333333333332], [6.0200000000000005, 6.0200000000000005], [3.8833333333333333, 3.8833333333333333], [6.3, 6.3], [5.916666666666667, 5.916666666666667], [5.4, 5.4], [5.1571428571428575, 5.1571428571428575], [5.59, 5.59], [5.8, 5.8], [6.05, 6.05], [5.75, 5.75], [6.0, 6.0], [6.0, 6.0], [5.8, 5.8], [6.6, 6.6], [6.5, 6.5], [6.3, 6.3], [6.6, 6.6], [4.95, 4.95], [6.199999999999999, 6.199999999999999], [3.1, 3.1], [4.2, 4.2], [6.0, 6.0], [5.819999999999999, 5.819999999999999], [3.9, 3.9], [6.2, 6.2], [5.75, 5.75], [0.0, 0.0], [6.0, 6.0], [0.0, 0.0], [0.0, 0.0], [3.25, 3.25], [3.45, 3.45], [5.445454545454545, 5.445454545454545], [5.072727272727273, 5.072727272727273], [3.3, 3.3], [6.6, 6.6], [5.0, 5.0], [6.4, 6.4], [5.933333333333334, 5.933333333333334], [0.0, 0.0], [6.6, 6.6], [5.327659574468085, 5.327659574468085], [6.5, 6.5], [6.050000000000001, 6.050000000000001], [2.7, 2.7], [0.0, 0.0], [6.1, 6.1], [6.1, 6.1], [0.0, 0.0], [5.9, 5.9], [0.0, 0.0], [5.2, 5.2], [2.9, 2.9], [6.0, 6.0], [0.0, 0.0], [0.0, 0.0], [0.0, 0.0], [6.9, 6.9], [0.0, 0.0], [0.0, 0.0], [3.25, 3.25], [5.6, 5.6], [5.5, 5.5], [5.2, 5.2], [0.0, 0.0], [6.1, 6.1], [5.9, 5.9], [5.5, 5.5], [6.4, 6.4], [5.3, 5.3], [6.3, 6.3], [6.8, 6.8], [6.128571428571428, 6.128571428571428], [5.8, 5.8], [5.7, 5.7], [6.1, 6.1], [6.25, 6.25], [5.455555555555555, 5.455555555555555], [4.7, 4.7], [5.8, 5.8], [5.2, 5.2], [5.1, 5.1], [6.15, 6.15], [1.9, 1.9], [6.3, 6.3], [6.3, 6.3], [6.3, 6.3], [5.900000000000001, 5.900000000000001], [6.6, 6.6], [6.3, 6.3], [6.6, 6.6], [5.2, 5.2], [6.199999999999999, 6.199999999999999], [5.6, 5.6], [6.175000000000001, 6.175000000000001], [6.257142857142857, 6.257142857142857], [3.15, 3.15], [5.24, 5.24], [6.0736842105263165, 6.0736842105263165], [6.114285714285714, 6.114285714285714], [0.0, 0.0], [4.270833333333333, 4.270833333333333], [5.6, 5.6], [5.5, 5.5], [4.625, 4.625], [5.966666666666666, 5.966666666666666], [5.9, 5.9], [5.766666666666667, 5.766666666666667], [0.0, 0.0], [6.4, 6.4], [5.5, 5.5], [5.0, 5.0], [5.6, 5.6], [5.5, 5.5], [3.733333333333333, 3.733333333333333], [5.8, 5.8], [8.3, 8.3], [6.866666666666667, 6.866666666666667], [8.8, 8.8], [7.8999999999999995, 7.8999999999999995], [5.9, 5.9], [5.375, 5.375], [5.75, 5.75], [8.8, 8.8], [8.8, 8.8], [5.1, 5.1], [6.0, 6.0], [3.9, 3.9], [7.766666666666668, 7.766666666666668], [6.939024390243904, 6.939024390243904], [6.254545454545454, 6.254545454545454], [5.6, 5.6], [6.475, 6.475], [5.3, 5.3], [6.233333333333333, 6.233333333333333], [5.021428571428571, 5.021428571428571], [6.5, 6.5], [8.1, 8.1], [5.366666666666667, 5.366666666666667], [6.166666666666667, 6.166666666666667], [3.9333333333333336, 3.9333333333333336], [6.7, 6.7], [4.066666666666666, 4.066666666666666], [5.55, 5.55], [6.88, 6.88], [5.6, 5.6], [8.0, 8.0], [6.6, 6.6], [7.1, 7.1], [0.0, 0.0], [0.0, 0.0], [0.0, 0.0], [3.6, 3.6], [4.2, 4.2], [4.0, 4.0], [6.242857142857142, 6.242857142857142], [3.9, 3.9], [6.807692307692307, 6.807692307692307], [6.237414965986395, 6.237414965986395], [6.8875, 6.8875], [8.0, 8.0], [5.880000000000001, 5.880000000000001], [8.466666666666667, 8.466666666666667], [8.45, 8.45], [8.0, 8.0], [8.1, 8.1], [8.285714285714286, 8.285714285714286], [8.134999999999998, 8.134999999999998], [7.550000000000001, 7.550000000000001], [8.2, 8.2], [8.2, 8.2], [6.3, 6.3], [5.85, 5.85], [6.1, 6.1], [8.0, 8.0], [6.4, 6.4], [7.433333333333334, 7.433333333333334], [6.1, 6.1], [8.0, 8.0], [8.1, 8.1], [7.2, 7.2], [7.3, 7.3], [5.8, 5.8], [7.3, 7.3], [6.05, 6.05], [5.9, 5.9], [7.6, 7.6], [5.8, 5.8], [0.0, 0.0], [8.4, 8.4], [7.499999999999999, 7.499999999999999], [7.1581395348837225, 7.1581395348837225], [1.2666666666666666, 1.2666666666666666], [6.199999999999999, 6.199999999999999], [6.8, 6.8], [5.2, 5.2], [6.24, 6.24], [5.6875, 5.6875], [7.5, 7.5], [8.8, 8.8], [7.65, 7.65], [6.5, 6.5], [7.5, 7.5], [6.666666666666667, 6.666666666666667], [7.9, 7.9], [5.80625, 5.80625], [7.9, 7.9], [7.5, 7.5], [7.3500000000000005, 7.3500000000000005], [6.7, 6.7], [8.0, 8.0], [6.6, 6.6], [6.7, 6.7], [6.3, 6.3], [6.6, 6.6], [6.3, 6.3], [6.35, 6.35], [4.2, 4.2], [6.8, 6.8], [6.0, 6.0], [6.3, 6.3], [7.983333333333334, 7.983333333333334], [7.314285714285716, 7.314285714285716], [0.0, 0.0], [5.566666666666667, 5.566666666666667], [5.5, 5.5], [5.82, 5.82], [0.0, 0.0], [7.4, 7.4], [7.0, 7.0], [6.4, 6.4], [6.3, 6.3], [6.433333333333334, 6.433333333333334], [5.921739130434782, 5.921739130434782], [0.0, 0.0], [3.4, 3.4], [4.7, 4.7], [6.7, 6.7], [5.5, 5.5], [6.1, 6.1], [3.4, 3.4], [6.05, 6.05], [6.066666666666666, 6.066666666666666], [0.0, 0.0], [6.5, 6.5], [5.90909090909091, 5.90909090909091], [8.2, 8.2], [6.075, 6.075], [6.1, 6.1], [5.533333333333332, 5.533333333333332], [6.266666666666667, 6.266666666666667], [4.414285714285714, 4.414285714285714], [7.025, 7.025], [7.2, 7.2], [8.1, 8.1], [6.3, 6.3], [6.35, 6.35], [5.86, 5.86], [6.442105263157894, 6.442105263157894], [5.8, 5.8], [7.3, 7.3], [6.05, 6.05], [5.75, 5.75], [6.866666666666667, 6.866666666666667], [6.4, 6.4], [5.8, 5.8], [6.6, 6.6], [6.7, 6.7], [6.3, 6.3], [6.6, 6.6], [4.95, 4.95], [6.199999999999999, 6.199999999999999], [3.6375, 3.6375], [4.2, 4.2], [6.0, 6.0], [6.242857142857142, 6.242857142857142], [8.4, 8.4], [3.9, 3.9], [7.433333333333333, 7.433333333333333], [6.7142857142857135, 6.7142857142857135], [0.0, 0.0], [7.4, 7.4], [7.133333333333333, 7.133333333333333], [7.0, 7.0], [8.3, 8.3], [8.1, 8.1], [7.1625000000000005, 7.1625000000000005], [8.149999999999999, 8.149999999999999], [0.0, 0.0], [8.25, 8.25], [5.6, 5.6], [8.185714285714285, 8.185714285714285], [8.6, 8.6], [4.7, 4.7], [6.294736842105262, 6.294736842105262], [7.2, 7.2], [5.726666666666666, 5.726666666666666], [3.3, 3.3], [8.6, 8.6], [6.6, 6.6], [5.361538461538462, 5.361538461538462], [6.4, 6.4], [5.933333333333334, 5.933333333333334], [3.85, 3.85], [7.2, 7.2], [7.6, 7.6], [7.2, 7.2], [5.820000000000001, 5.820000000000001], [6.5, 6.5], [6.7, 6.7], [5.7299999999999995, 5.7299999999999995], [2.3666666666666667, 2.3666666666666667], [6.1, 6.1], [6.1, 6.1], [8.4, 8.4], [3.65, 3.65], [5.9, 5.9], [0.0, 0.0], [6.944444444444445, 6.944444444444445], [2.9, 2.9], [7.5, 7.5], [0.0, 0.0], [0.0, 0.0], [7.377272727272729, 7.377272727272729], [7.95217391304348, 7.95217391304348], [0.0, 0.0], [0.0, 0.0], [8.4, 8.4], [5.6, 5.6], [8.1, 8.1], [7.8, 7.8], [5.6, 5.6], [5.5, 5.5], [5.2, 5.2], [0.0, 0.0], [6.1, 6.1], [5.9, 5.9], [5.5, 5.5], [6.4, 6.4], [5.3, 5.3], [6.949999999999999, 6.949999999999999], [6.8, 6.8], [6.128571428571428, 6.128571428571428], [5.8, 5.8], [8.2, 8.2], [5.7, 5.7], [8.8, 8.8], [6.1, 6.1], [7.359999999999999, 7.359999999999999], [7.1, 7.1], [8.05, 8.05], [8.3, 8.3], [8.149999999999999, 8.149999999999999], [8.033333333333333, 8.033333333333333], [7.6, 7.6], [8.1, 8.1], [4.7, 4.7], [5.8, 5.8], [7.3, 7.3], [7.3, 7.3], [5.2, 5.2], [5.1, 5.1], [8.2, 8.2], [7.0, 7.0], [1.9, 1.9], [6.3, 6.3], [6.3, 6.3], [7.6, 7.6], [6.3, 6.3], [7.2, 7.2], [6.6000000000000005, 6.6000000000000005], [6.6, 6.6], [6.3, 6.3], [6.6, 6.6], [5.2, 5.2], [6.199999999999999, 6.199999999999999], [5.6, 5.6], [8.8, 8.8], [7.322727272727272, 7.322727272727272], [7.4375, 7.4375], [8.225, 8.225], [7.210000000000001, 7.210000000000001], [7.8, 7.8], [8.7, 8.7], [6.941666666666667, 6.941666666666667], [6.736363636363635, 6.736363636363635], [7.0307692307692315, 7.0307692307692315], [7.800000000000001, 7.800000000000001], [0.0, 0.0], [5.3, 5.3], [6.699999999999999, 6.699999999999999], [6.833333333333333, 6.833333333333333], [6.1625, 6.1625], [7.45, 7.45], [8.2, 8.2], [6.866666666666667, 6.866666666666667], [6.699999999999999, 6.699999999999999], [7.666666666666667, 7.666666666666667], [8.55, 8.55], [6.900000000000001, 6.900000000000001], [6.42608695652174, 6.42608695652174], [5.0, 5.0], [7.4, 7.4], [5.6, 5.6], [6.25, 6.25], [3.733333333333333, 3.733333333333333], [8.2, 8.2], [6.874074074074075, 6.874074074074075], [6.423333333333334, 6.423333333333334], [6.477777777777778, 6.477777777777778], [8.0, 8.0], [6.384210526315789, 6.384210526315789], [3.4, 3.4], [5.966666666666667, 5.966666666666667], [6.875, 6.875], [8.466666666666665, 8.466666666666665], [7.650000000000001, 7.650000000000001], [8.0, 8.0], [8.1, 8.1], [5.953488372093023, 5.953488372093023], [6.351515151515152, 6.351515151515152], [5.726086956521739, 5.726086956521739], [6.736363636363635, 6.736363636363635], [7.092857142857143, 7.092857142857143], [6.3112903225806445, 6.3112903225806445], [7.0200000000000005, 7.0200000000000005], [7.3, 7.3], [2.8666666666666663, 2.8666666666666663], [5.7148648648648654, 5.7148648648648654], [6.699999999999999, 6.699999999999999], [7.352173913043478, 7.352173913043478], [6.1625, 6.1625], [6.4, 6.4], [7.1, 7.1], [8.0, 8.0], [6.599999999999999, 6.599999999999999], [6.7, 6.7], [6.3, 6.3], [6.599999999999999, 6.599999999999999], [5.608333333333333, 5.608333333333333], [5.028571428571428, 5.028571428571428], [5.1, 5.1], [4.446153846153846, 4.446153846153846], [4.764285714285713, 4.764285714285713], [6.325, 6.325], [5.6800000000000015, 5.6800000000000015], [6.244444444444444, 6.244444444444444], [8.4, 8.4], [4.86, 4.86], [7.549999999999999, 7.549999999999999], [6.681318681318682, 6.681318681318682], [6.900000000000001, 6.900000000000001], [6.42608695652174, 6.42608695652174], [5.0, 5.0], [7.4, 7.4], [3.6916666666666664, 3.6916666666666664], [5.6, 5.6], [6.25, 6.25], [3.733333333333333, 3.733333333333333]], "domain": {"x": [0.0, 1.0], "y": [0.0, 1.0]}, "hovertemplate": "labels=%{label}<br>count=%{value}<br>parent=%{parent}<br>id=%{id}<br>rating_num=%{color}<extra></extra>", "ids": ["Canada/Action & Adventure/High-rated", "China/Action & Adventure/High-rated", "Colombia/Action & Adventure/High-rated", "Germany/Action & Adventure/High-rated", "Hong Kong/Action & Adventure/High-rated", "Mexico/Action & Adventure/High-rated", "New Zealand/Action & Adventure/High-rated", "United Kingdom/Action & Adventure/High-rated", "United States/Action & Adventure/High-rated", "Japan/Anime Series/High-rated", "Australia/Comedies/High-rated", "Canada/Comedies/High-rated", "Denmark/Comedies/High-rated", "France/Comedies/High-rated", "Germany/Comedies/High-rated", "India/Comedies/High-rated", "Mexico/Comedies/High-rated", "Norway/Comedies/High-rated", "Philippines/Comedies/High-rated", "Taiwan/Comedies/High-rated", "Turkey/Comedies/High-rated", "United Kingdom/Comedies/High-rated", "United States/Comedies/High-rated", "nan/Comedies/High-rated", "Australia/Crime/High-rated", "Canada/Crime/High-rated", "Colombia/Crime/High-rated", "Mexico/Crime/High-rated", "Norway/Crime/High-rated", "Spain/Crime/High-rated", "United Kingdom/Crime/High-rated", "United States/Crime/High-rated", "Canada/Cult Movies/High-rated", "India/Cult Movies/High-rated", "/Documentaries/High-rated", "Bermuda/Documentaries/High-rated", "Canada/Documentaries/High-rated", "Ecuador/Documentaries/High-rated", "Egypt/Documentaries/High-rated", "Germany/Documentaries/High-rated", "India/Documentaries/High-rated", "Israel/Documentaries/High-rated", "Netherlands/Documentaries/High-rated", "Ukraine/Documentaries/High-rated", "United Kingdom/Documentaries/High-rated", "United States/Documentaries/High-rated", "Australia/Dramas/High-rated", "Brazil/Dramas/High-rated", "Canada/Dramas/High-rated", "China/Dramas/High-rated", "Colombia/Dramas/High-rated", "Denmark/Dramas/High-rated", "France/Dramas/High-rated", "Germany/Dramas/High-rated", "Hong Kong/Dramas/High-rated", "Hungary/Dramas/High-rated", "India/Dramas/High-rated", "Ireland/Dramas/High-rated", "Japan/Dramas/High-rated", "Mexico/Dramas/High-rated", "Norway/Dramas/High-rated", "Philippines/Dramas/High-rated", "Spain/Dramas/High-rated", "Taiwan/Dramas/High-rated", "United Kingdom/Dramas/High-rated", "United States/Dramas/High-rated", "Canada/Family Movies/High-rated", "India/Family Movies/High-rated", "Ireland/Family Movies/High-rated", "United States/Family Movies/High-rated", "India/Independent Movies and LGBTQ Movies/High-rated", "United States/Independent Movies and LGBTQ Movies/High-rated", "/International Movies/High-rated", "Brazil/International Movies/High-rated", "Canada/International Movies/High-rated", "China/International Movies/High-rated", "Denmark/International Movies/High-rated", "Egypt/International Movies/High-rated", "France/International Movies/High-rated", "Germany/International Movies/High-rated", "Hong Kong/International Movies/High-rated", "India/International Movies/High-rated", "Israel/International Movies/High-rated", "Mexico/International Movies/High-rated", "Netherlands/International Movies/High-rated", "Philippines/International Movies/High-rated", "Spain/International Movies/High-rated", "Turkey/International Movies/High-rated", "Ukraine/International Movies/High-rated", "United Kingdom/International Movies/High-rated", "United States/International Movies/High-rated", "Australia/International TV Shows/High-rated", "Canada/International TV Shows/High-rated", "China/International TV Shows/High-rated", "Colombia/International TV Shows/High-rated", "Denmark/International TV Shows/High-rated", "Japan/International TV Shows/High-rated", "Mexico/International TV Shows/High-rated", "Spain/International TV Shows/High-rated", "Taiwan/International TV Shows/High-rated", "United Kingdom/International TV Shows/High-rated", "United States/International TV Shows/High-rated", "Australia/Kid's and Teen/High-rated", "Canada/Kid's and Teen/High-rated", "Denmark/Kid's and Teen/High-rated", "France/Kid's and Teen/High-rated", "Ireland/Kid's and Teen/High-rated", "Japan/Kid's and Teen/High-rated", "Russia/Kid's and Teen/High-rated", "Singapore/Kid's and Teen/High-rated", "Spain/Kid's and Teen/High-rated", "United Kingdom/Kid's and Teen/High-rated", "United States/Kid's and Teen/High-rated", "Canada/Movies/High-rated", "United States/Movies/High-rated", "nan/Movies/High-rated", "Canada/Music & Musicals/High-rated", "Germany/Music & Musicals/High-rated", "United States/Music & Musicals/High-rated", "Canada/Other Shows/High-rated", "United Kingdom/Other Shows/High-rated", "United States/Other Shows/High-rated", "Spain/Romantic/High-rated", "Taiwan/Romantic/High-rated", "United Kingdom/Romantic/High-rated", "United States/Romantic/High-rated", "Turkey/Romantic Movies/High-rated", "Germany/Sci-Fi & Fantasy/High-rated", "New Zealand/Sci-Fi & Fantasy/High-rated", "United Kingdom/Sci-Fi & Fantasy/High-rated", "United States/Sci-Fi & Fantasy/High-rated", "United States/Science & Nature TV/High-rated", "Colombia/Spanish-Language TV Shows/High-rated", "Mexico/Spanish-Language TV Shows/High-rated", "Spain/Spanish-Language TV Shows/High-rated", "United Kingdom/Spanish-Language TV Shows/High-rated", "United States/Spanish-Language TV Shows/High-rated", "Germany/Sports Movies/High-rated", "India/Sports Movies/High-rated", "United Kingdom/Sports Movies/High-rated", "United States/Sports Movies/High-rated", "Canada/Thrillers & Horror/High-rated", "Germany/Thrillers & Horror/High-rated", "India/Thrillers & Horror/High-rated", "United Kingdom/Thrillers & Horror/High-rated", "United States/Thrillers & Horror/High-rated", "Argentina/nan/High-rated", "Australia/nan/High-rated", "Belgium/nan/High-rated", "Brazil/nan/High-rated", "France/nan/High-rated", "Germany/nan/High-rated", "Hongkong/nan/High-rated", "Hungary/nan/High-rated", "India/nan/High-rated", "Japan/nan/High-rated", "Luthvania/nan/High-rated", "Mexico/nan/High-rated", "Netherland/nan/High-rated", "Russia/nan/High-rated", "Singapore/nan/High-rated", "South Korea/nan/High-rated", "Sweden/nan/High-rated", "United Kingdom/nan/High-rated", "United States/nan/High-rated", "ca/nan/High-rated", "cezhrepublic/nan/High-rated", "is/nan/High-rated", "sk/nan/High-rated", "Australia/Action & Adventure/Low-rated", "China/Action & Adventure/Low-rated", "Hong Kong/Action & Adventure/Low-rated", "India/Action & Adventure/Low-rated", "Japan/Action & Adventure/Low-rated", "South Africa/Action & Adventure/Low-rated", "Taiwan/Action & Adventure/Low-rated", "United Arab Emirates/Action & Adventure/Low-rated", "United Kingdom/Action & Adventure/Low-rated", "United States/Action & Adventure/Low-rated", "Japan/Anime Series/Low-rated", "Argentina/Comedies/Low-rated", "Australia/Comedies/Low-rated", "Belgium/Comedies/Low-rated", "Brazil/Comedies/Low-rated", "Canada/Comedies/Low-rated", "China/Comedies/Low-rated", "France/Comedies/Low-rated", "Germany/Comedies/Low-rated", "Hong Kong/Comedies/Low-rated", "India/Comedies/Low-rated", "Italy/Comedies/Low-rated", "Japan/Comedies/Low-rated", "Mexico/Comedies/Low-rated", "Netherlands/Comedies/Low-rated", "Pakistan/Comedies/Low-rated", "Russia/Comedies/Low-rated", "Singapore/Comedies/Low-rated", "South Korea/Comedies/Low-rated", "Spain/Comedies/Low-rated", "Sweden/Comedies/Low-rated", "Taiwan/Comedies/Low-rated", "Turkey/Comedies/Low-rated", "United Arab Emirates/Comedies/Low-rated", "United Kingdom/Comedies/Low-rated", "United States/Comedies/Low-rated", "nan/Comedies/Low-rated", "Canada/Crime/Low-rated", "United States/Crime/Low-rated", "Argentina/Documentaries/Low-rated", "Australia/Documentaries/Low-rated", "Belgium/Documentaries/Low-rated", "Brazil/Documentaries/Low-rated", "Canada/Documentaries/Low-rated", "China/Documentaries/Low-rated", "Ireland/Documentaries/Low-rated", "Italy/Documentaries/Low-rated", "Mexico/Documentaries/Low-rated", "New Zealand/Documentaries/Low-rated", "Spain/Documentaries/Low-rated", "United Kingdom/Documentaries/Low-rated", "United States/Documentaries/Low-rated", "nan/Documentaries/Low-rated", "Argentina/Dramas/Low-rated", "Australia/Dramas/Low-rated", "Belgium/Dramas/Low-rated", "Brazil/Dramas/Low-rated", "Canada/Dramas/Low-rated", "France/Dramas/Low-rated", "Hong Kong/Dramas/Low-rated", "India/Dramas/Low-rated", "Mexico/Dramas/Low-rated", "Netherlands/Dramas/Low-rated", "Pakistan/Dramas/Low-rated", "Philippines/Dramas/Low-rated", "Poland/Dramas/Low-rated", "Qatar/Dramas/Low-rated", "South Korea/Dramas/Low-rated", "Spain/Dramas/Low-rated", "Sweden/Dramas/Low-rated", "Taiwan/Dramas/Low-rated", "Turkey/Dramas/Low-rated", "United Arab Emirates/Dramas/Low-rated", "United States/Dramas/Low-rated", "nan/Dramas/Low-rated", "Australia/Family Movies/Low-rated", "Brazil/Family Movies/Low-rated", "Canada/Family Movies/Low-rated", "Germany/Family Movies/Low-rated", "New Zealand/Family Movies/Low-rated", "United Arab Emirates/Family Movies/Low-rated", "United Kingdom/Family Movies/Low-rated", "United States/Family Movies/Low-rated", "nan/Family Movies/Low-rated", "Bulgaria/Horror Movies/Low-rated", "Singapore/Horror Movies/Low-rated", "United Kingdom/Horror Movies/Low-rated", "United States/Horror Movies/Low-rated", "Argentina/Independent Movies and LGBTQ Movies/Low-rated", "Bulgaria/Independent Movies and LGBTQ Movies/Low-rated", "France/Independent Movies and LGBTQ Movies/Low-rated", "India/Independent Movies and LGBTQ Movies/Low-rated", "Spain/Independent Movies and LGBTQ Movies/Low-rated", "United Kingdom/Independent Movies and LGBTQ Movies/Low-rated", "United States/Independent Movies and LGBTQ Movies/Low-rated", "Argentina/International Movies/Low-rated", "Australia/International Movies/Low-rated", "Belgium/International Movies/Low-rated", "Brazil/International Movies/Low-rated", "Canada/International Movies/Low-rated", "China/International Movies/Low-rated", "France/International Movies/Low-rated", "Germany/International Movies/Low-rated", "Hong Kong/International Movies/Low-rated", "India/International Movies/Low-rated", "Ireland/International Movies/Low-rated", "Italy/International Movies/Low-rated", "Japan/International Movies/Low-rated", "Mexico/International Movies/Low-rated", "Netherlands/International Movies/Low-rated", "New Zealand/International Movies/Low-rated", "Pakistan/International Movies/Low-rated", "Philippines/International Movies/Low-rated", "Poland/International Movies/Low-rated", "Qatar/International Movies/Low-rated", "Singapore/International Movies/Low-rated", "South Korea/International Movies/Low-rated", "Spain/International Movies/Low-rated", "Sweden/International Movies/Low-rated", "Taiwan/International Movies/Low-rated", "Turkey/International Movies/Low-rated", "United Arab Emirates/International Movies/Low-rated", "United Kingdom/International Movies/Low-rated", "United States/International Movies/Low-rated", "nan/International Movies/Low-rated", "Canada/International TV Shows/Low-rated", "Japan/International TV Shows/Low-rated", "South Korea/International TV Shows/Low-rated", "Taiwan/International TV Shows/Low-rated", "Australia/Kid's and Teen/Low-rated", "Canada/Kid's and Teen/Low-rated", "France/Kid's and Teen/Low-rated", "Germany/Kid's and Teen/Low-rated", "Italy/Kid's and Teen/Low-rated", "Japan/Kid's and Teen/Low-rated", "Netherlands/Kid's and Teen/Low-rated", "New Zealand/Kid's and Teen/Low-rated", "Russia/Kid's and Teen/Low-rated", "United Kingdom/Kid's and Teen/Low-rated", "United States/Kid's and Teen/Low-rated", "nan/Kid's and Teen/Low-rated", "Canada/Movies/Low-rated", "United States/Movies/Low-rated", "nan/Movies/Low-rated", "Australia/Music & Musicals/Low-rated", "Belgium/Music & Musicals/Low-rated", "Germany/Music & Musicals/Low-rated", "India/Music & Musicals/Low-rated", "Spain/Music & Musicals/Low-rated", "United States/Music & Musicals/Low-rated", "nan/Music & Musicals/Low-rated", "Canada/Other Shows/Low-rated", "Russia/Other Shows/Low-rated", "South Korea/Other Shows/Low-rated", "United Kingdom/Other Shows/Low-rated", "United States/Other Shows/Low-rated", "Canada/Romantic/Low-rated", "South Korea/Romantic/Low-rated", "Taiwan/Romantic/Low-rated", "Argentina/Romantic Movies/Low-rated", "Australia/Romantic Movies/Low-rated", "Belgium/Romantic Movies/Low-rated", "Canada/Romantic Movies/Low-rated", "China/Romantic Movies/Low-rated", "France/Romantic Movies/Low-rated", "Germany/Romantic Movies/Low-rated", "Philippines/Romantic Movies/Low-rated", "Spain/Romantic Movies/Low-rated", "Turkey/Romantic Movies/Low-rated", "United Kingdom/Romantic Movies/Low-rated", "United States/Romantic Movies/Low-rated", "Australia/Sci-Fi & Fantasy/Low-rated", "Netherlands/Sci-Fi & Fantasy/Low-rated", "South Korea/Sci-Fi & Fantasy/Low-rated", "United Kingdom/Sci-Fi & Fantasy/Low-rated", "United States/Sci-Fi & Fantasy/Low-rated", "Australia/Sports Movies/Low-rated", "Canada/Sports Movies/Low-rated", "Spain/Sports Movies/Low-rated", "Turkey/Sports Movies/Low-rated", "United States/Sports Movies/Low-rated", "nan/Sports Movies/Low-rated", "Argentina/Thrillers & Horror/Low-rated", "Brazil/Thrillers & Horror/Low-rated", "France/Thrillers & Horror/Low-rated", "India/Thrillers & Horror/Low-rated", "Philippines/Thrillers & Horror/Low-rated", "Poland/Thrillers & Horror/Low-rated", "Qatar/Thrillers & Horror/Low-rated", "Singapore/Thrillers & Horror/Low-rated", "South Korea/Thrillers & Horror/Low-rated", "Spain/Thrillers & Horror/Low-rated", "United States/Thrillers & Horror/Low-rated", "Argentina/nan/Low-rated", "Belgium/nan/Low-rated", "Germany/nan/Low-rated", "Hongkong/nan/Low-rated", "Hungary/nan/Low-rated", "Italy/nan/Low-rated", "Japan/nan/Low-rated", "Luthvania/nan/Low-rated", "Mexico/nan/Low-rated", "Netherland/nan/Low-rated", "Russia/nan/Low-rated", "South Korea/nan/Low-rated", "Sweden/nan/Low-rated", "United Kingdom/nan/Low-rated", "ca/nan/Low-rated", "cezhrepublic/nan/Low-rated", "gr/nan/Low-rated", "pt/nan/Low-rated", "sk/nan/Low-rated", "th/nan/Low-rated", "Australia/Action & Adventure", "Canada/Action & Adventure", "China/Action & Adventure", "Colombia/Action & Adventure", "Germany/Action & Adventure", "Hong Kong/Action & Adventure", "India/Action & Adventure", "Japan/Action & Adventure", "Mexico/Action & Adventure", "New Zealand/Action & Adventure", "South Africa/Action & Adventure", "Taiwan/Action & Adventure", "United Arab Emirates/Action & Adventure", "United Kingdom/Action & Adventure", "United States/Action & Adventure", "Japan/Anime Series", "Argentina/Comedies", "Australia/Comedies", "Belgium/Comedies", "Brazil/Comedies", "Canada/Comedies", "China/Comedies", "Denmark/Comedies", "France/Comedies", "Germany/Comedies", "Hong Kong/Comedies", "India/Comedies", "Italy/Comedies", "Japan/Comedies", "Mexico/Comedies", "Netherlands/Comedies", "Norway/Comedies", "Pakistan/Comedies", "Philippines/Comedies", "Russia/Comedies", "Singapore/Comedies", "South Korea/Comedies", "Spain/Comedies", "Sweden/Comedies", "Taiwan/Comedies", "Turkey/Comedies", "United Arab Emirates/Comedies", "United Kingdom/Comedies", "United States/Comedies", "nan/Comedies", "Australia/Crime", "Canada/Crime", "Colombia/Crime", "Mexico/Crime", "Norway/Crime", "Spain/Crime", "United Kingdom/Crime", "United States/Crime", "Canada/Cult Movies", "India/Cult Movies", "/Documentaries", "Argentina/Documentaries", "Australia/Documentaries", "Belgium/Documentaries", "Bermuda/Documentaries", "Brazil/Documentaries", "Canada/Documentaries", "China/Documentaries", "Ecuador/Documentaries", "Egypt/Documentaries", "Germany/Documentaries", "India/Documentaries", "Ireland/Documentaries", "Israel/Documentaries", "Italy/Documentaries", "Mexico/Documentaries", "Netherlands/Documentaries", "New Zealand/Documentaries", "Spain/Documentaries", "Ukraine/Documentaries", "United Kingdom/Documentaries", "United States/Documentaries", "nan/Documentaries", "Argentina/Dramas", "Australia/Dramas", "Belgium/Dramas", "Brazil/Dramas", "Canada/Dramas", "China/Dramas", "Colombia/Dramas", "Denmark/Dramas", "France/Dramas", "Germany/Dramas", "Hong Kong/Dramas", "Hungary/Dramas", "India/Dramas", "Ireland/Dramas", "Japan/Dramas", "Mexico/Dramas", "Netherlands/Dramas", "Norway/Dramas", "Pakistan/Dramas", "Philippines/Dramas", "Poland/Dramas", "Qatar/Dramas", "South Korea/Dramas", "Spain/Dramas", "Sweden/Dramas", "Taiwan/Dramas", "Turkey/Dramas", "United Arab Emirates/Dramas", "United Kingdom/Dramas", "United States/Dramas", "nan/Dramas", "Australia/Family Movies", "Brazil/Family Movies", "Canada/Family Movies", "Germany/Family Movies", "India/Family Movies", "Ireland/Family Movies", "New Zealand/Family Movies", "United Arab Emirates/Family Movies", "United Kingdom/Family Movies", "United States/Family Movies", "nan/Family Movies", "Bulgaria/Horror Movies", "Singapore/Horror Movies", "United Kingdom/Horror Movies", "United States/Horror Movies", "Argentina/Independent Movies and LGBTQ Movies", "Bulgaria/Independent Movies and LGBTQ Movies", "France/Independent Movies and LGBTQ Movies", "India/Independent Movies and LGBTQ Movies", "Spain/Independent Movies and LGBTQ Movies", "United Kingdom/Independent Movies and LGBTQ Movies", "United States/Independent Movies and LGBTQ Movies", "/International Movies", "Argentina/International Movies", "Australia/International Movies", "Belgium/International Movies", "Brazil/International Movies", "Canada/International Movies", "China/International Movies", "Denmark/International Movies", "Egypt/International Movies", "France/International Movies", "Germany/International Movies", "Hong Kong/International Movies", "India/International Movies", "Ireland/International Movies", "Israel/International Movies", "Italy/International Movies", "Japan/International Movies", "Mexico/International Movies", "Netherlands/International Movies", "New Zealand/International Movies", "Pakistan/International Movies", "Philippines/International Movies", "Poland/International Movies", "Qatar/International Movies", "Singapore/International Movies", "South Korea/International Movies", "Spain/International Movies", "Sweden/International Movies", "Taiwan/International Movies", "Turkey/International Movies", "Ukraine/International Movies", "United Arab Emirates/International Movies", "United Kingdom/International Movies", "United States/International Movies", "nan/International Movies", "Australia/International TV Shows", "Canada/International TV Shows", "China/International TV Shows", "Colombia/International TV Shows", "Denmark/International TV Shows", "Japan/International TV Shows", "Mexico/International TV Shows", "South Korea/International TV Shows", "Spain/International TV Shows", "Taiwan/International TV Shows", "United Kingdom/International TV Shows", "United States/International TV Shows", "Australia/Kid's and Teen", "Canada/Kid's and Teen", "Denmark/Kid's and Teen", "France/Kid's and Teen", "Germany/Kid's and Teen", "Ireland/Kid's and Teen", "Italy/Kid's and Teen", "Japan/Kid's and Teen", "Netherlands/Kid's and Teen", "New Zealand/Kid's and Teen", "Russia/Kid's and Teen", "Singapore/Kid's and Teen", "Spain/Kid's and Teen", "United Kingdom/Kid's and Teen", "United States/Kid's and Teen", "nan/Kid's and Teen", "Canada/Movies", "United States/Movies", "nan/Movies", "Australia/Music & Musicals", "Belgium/Music & Musicals", "Canada/Music & Musicals", "Germany/Music & Musicals", "India/Music & Musicals", "Spain/Music & Musicals", "United States/Music & Musicals", "nan/Music & Musicals", "Canada/Other Shows", "Russia/Other Shows", "South Korea/Other Shows", "United Kingdom/Other Shows", "United States/Other Shows", "Canada/Romantic", "South Korea/Romantic", "Spain/Romantic", "Taiwan/Romantic", "United Kingdom/Romantic", "United States/Romantic", "Argentina/Romantic Movies", "Australia/Romantic Movies", "Belgium/Romantic Movies", "Canada/Romantic Movies", "China/Romantic Movies", "France/Romantic Movies", "Germany/Romantic Movies", "Philippines/Romantic Movies", "Spain/Romantic Movies", "Turkey/Romantic Movies", "United Kingdom/Romantic Movies", "United States/Romantic Movies", "Australia/Sci-Fi & Fantasy", "Germany/Sci-Fi & Fantasy", "Netherlands/Sci-Fi & Fantasy", "New Zealand/Sci-Fi & Fantasy", "South Korea/Sci-Fi & Fantasy", "United Kingdom/Sci-Fi & Fantasy", "United States/Sci-Fi & Fantasy", "United States/Science & Nature TV", "Colombia/Spanish-Language TV Shows", "Mexico/Spanish-Language TV Shows", "Spain/Spanish-Language TV Shows", "United Kingdom/Spanish-Language TV Shows", "United States/Spanish-Language TV Shows", "Australia/Sports Movies", "Canada/Sports Movies", "Germany/Sports Movies", "India/Sports Movies", "Spain/Sports Movies", "Turkey/Sports Movies", "United Kingdom/Sports Movies", "United States/Sports Movies", "nan/Sports Movies", "Argentina/Thrillers & Horror", "Brazil/Thrillers & Horror", "Canada/Thrillers & Horror", "France/Thrillers & Horror", "Germany/Thrillers & Horror", "India/Thrillers & Horror", "Philippines/Thrillers & Horror", "Poland/Thrillers & Horror", "Qatar/Thrillers & Horror", "Singapore/Thrillers & Horror", "South Korea/Thrillers & Horror", "Spain/Thrillers & Horror", "United Kingdom/Thrillers & Horror", "United States/Thrillers & Horror", "Argentina/nan", "Australia/nan", "Belgium/nan", "Brazil/nan", "France/nan", "Germany/nan", "Hongkong/nan", "Hungary/nan", "India/nan", "Italy/nan", "Japan/nan", "Luthvania/nan", "Mexico/nan", "Netherland/nan", "Russia/nan", "Singapore/nan", "South Korea/nan", "Sweden/nan", "United Kingdom/nan", "United States/nan", "ca/nan", "cezhrepublic/nan", "gr/nan", "is/nan", "pt/nan", "sk/nan", "th/nan", "", "Argentina", "Australia", "Belgium", "Bermuda", "Brazil", "Bulgaria", "Canada", "China", "Colombia", "Denmark", "Ecuador", "Egypt", "France", "Germany", "Hong Kong", "Hongkong", "Hungary", "India", "Ireland", "Israel", "Italy", "Japan", "Luthvania", "Mexico", "Netherland", "Netherlands", "New Zealand", "Norway", "Pakistan", "Philippines", "Poland", "Qatar", "Russia", "Singapore", "South Africa", "South Korea", "Spain", "Sweden", "Taiwan", "Turkey", "Ukraine", "United Arab Emirates", "United Kingdom", "United States", "ca", "cezhrepublic", "gr", "is", "nan", "pt", "sk", "th"], "labels": ["High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "High-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Low-rated", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Action & Adventure", "Anime Series", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Comedies", "Crime", "Crime", "Crime", "Crime", "Crime", "Crime", "Crime", "Crime", "Cult Movies", "Cult Movies", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Documentaries", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Dramas", "Family Movies", "Family Movies", "Family Movies", "Family Movies", "Family Movies", "Family Movies", "Family Movies", "Family Movies", "Family Movies", "Family Movies", "Family Movies", "Horror Movies", "Horror Movies", "Horror Movies", "Horror Movies", "Independent Movies and LGBTQ Movies", "Independent Movies and LGBTQ Movies", "Independent Movies and LGBTQ Movies", "Independent Movies and LGBTQ Movies", "Independent Movies and LGBTQ Movies", "Independent Movies and LGBTQ Movies", "Independent Movies and LGBTQ Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International Movies", "International TV Shows", "International TV Shows", "International TV Shows", "International TV Shows", "International TV Shows", "International TV Shows", "International TV Shows", "International TV Shows", "International TV Shows", "International TV Shows", "International TV Shows", "International TV Shows", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Kid's and Teen", "Movies", "Movies", "Movies", "Music & Musicals", "Music & Musicals", "Music & Musicals", "Music & Musicals", "Music & Musicals", "Music & Musicals", "Music & Musicals", "Music & Musicals", "Other Shows", "Other Shows", "Other Shows", "Other Shows", "Other Shows", "Romantic", "Romantic", "Romantic", "Romantic", "Romantic", "Romantic", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Romantic Movies", "Sci-Fi & Fantasy", "Sci-Fi & Fantasy", "Sci-Fi & Fantasy", "Sci-Fi & Fantasy", "Sci-Fi & Fantasy", "Sci-Fi & Fantasy", "Sci-Fi & Fantasy", "Science & Nature TV", "Spanish-Language TV Shows", "Spanish-Language TV Shows", "Spanish-Language TV Shows", "Spanish-Language TV Shows", "Spanish-Language TV Shows", "Sports Movies", "Sports Movies", "Sports Movies", "Sports Movies", "Sports Movies", "Sports Movies", "Sports Movies", "Sports Movies", "Sports Movies", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "Thrillers & Horror", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "nan", "", "Argentina", "Australia", "Belgium", "Bermuda", "Brazil", "Bulgaria", "Canada", "China", "Colombia", "Denmark", "Ecuador", "Egypt", "France", "Germany", "Hong Kong", "Hongkong", "Hungary", "India", "Ireland", "Israel", "Italy", "Japan", "Luthvania", "Mexico", "Netherland", "Netherlands", "New Zealand", "Norway", "Pakistan", "Philippines", "Poland", "Qatar", "Russia", "Singapore", "South Africa", "South Korea", "Spain", "Sweden", "Taiwan", "Turkey", "Ukraine", "United Arab Emirates", "United Kingdom", "United States", "ca", "cezhrepublic", "gr", "is", "nan", "pt", "sk", "th"], "marker": {"coloraxis": "coloraxis", "colors": [8.3, 7.5, 8.8, 7.8999999999999995, 7.75, 8.8, 8.8, 8.16, 8.108695652173912, 8.185714285714287, 8.2, 7.400000000000001, 8.1, 7.1, 7.6, 7.8, 7.699999999999999, 8.0, 7.1, 8.0, 7.3, 7.8125, 7.65967741935484, 7.324999999999999, 8.0, 8.266666666666667, 8.466666666666667, 8.45, 8.0, 8.1, 8.285714285714286, 8.321052631578945, 7.550000000000001, 8.2, 8.2, 8.0, 7.640000000000001, 8.0, 8.1, 7.2, 7.3, 7.3, 7.6, 8.4, 7.949999999999999, 7.696296296296295, 7.733333333333334, 7.5, 7.9, 7.5, 8.8, 7.65, 7.45, 7.5, 7.5, 7.9, 7.266666666666666, 7.9, 7.5, 7.800000000000001, 8.0, 7.1, 7.4, 7.9, 7.983333333333334, 8.047619047619047, 7.2, 7.4, 7.0, 7.125, 7.55, 7.7, 8.2, 7.5, 7.6, 7.75, 7.2, 8.1, 7.45, 7.3, 7.5, 7.388888888888889, 7.3, 7.300000000000001, 7.6, 7.1, 7.4, 7.3, 8.4, 8.049999999999999, 8.0, 7.4, 7.7, 7.0, 8.3, 8.1, 8.185714285714287, 8.149999999999999, 8.25, 7.95, 8.185714285714285, 8.6, 7.2, 7.4625, 7.2, 7.525, 8.6, 7.35, 7.7, 7.2, 7.6, 7.5, 7.6, 8.0, 7.75, 7.1, 8.4, 7.3, 7.442857142857143, 7.875, 8.115000000000002, 8.000000000000002, 8.4, 7.95, 8.1, 7.8, 7.6, 8.2, 8.8, 8.1, 8.024999999999999, 8.05, 8.3, 8.149999999999999, 8.033333333333333, 7.6, 8.1, 7.3, 7.3, 8.2, 7.566666666666666, 7.6, 7.2, 7.3, 8.8, 7.978571428571429, 8.355555555555556, 8.225, 8.225, 7.8, 8.7, 8.157142857142857, 7.635714285714286, 8.1, 7.800000000000001, 7.545454545454546, 7.8, 7.5, 7.7, 8.34, 8.2, 8.8, 7.75, 8.05, 8.55, 7.15, 7.436363636363635, 7.4, 7.0, 5.8, 6.233333333333333, 5.159999999999999, 5.375, 5.75, 5.1, 6.0, 3.9, 5.8, 5.444444444444444, 2.875, 5.6, 5.8999999999999995, 5.3, 6.233333333333333, 4.372727272727273, 6.5, 5.15, 5.45, 3.9333333333333336, 5.6, 4.066666666666666, 5.55, 6.333333333333333, 5.6, 6.6, 0.0, 0.0, 0.0, 3.6, 4.2, 0.0, 5.819999999999999, 3.9, 5.2, 5.200000000000001, 6.45, 2.3, 4.6, 6.3, 5.85, 6.1, 6.4, 6.4, 6.1, 5.8, 6.05, 5.9, 5.8, 0.0, 6.15, 6.25, 1.2666666666666666, 6.199999999999999, 5.4, 5.2, 5.925, 2.0, 5.866666666666667, 5.0, 4.930000000000001, 6.0, 6.7, 6.6, 6.5, 6.3, 6.6, 6.3, 5.3, 4.2, 6.25, 6.0, 6.3, 5.847619047619047, 0.0, 5.566666666666667, 5.5, 4.9, 0.0, 6.4, 6.3, 6.433333333333334, 5.668421052631579, 0.0, 3.4, 4.7, 6.7, 5.5, 6.1, 3.4, 6.05, 5.325, 0.0, 6.5, 5.823809523809525, 6.075, 6.1, 5.533333333333332, 6.0200000000000005, 3.8833333333333333, 6.3, 5.916666666666667, 5.4, 5.1571428571428575, 5.59, 5.8, 6.05, 5.75, 6.0, 6.0, 5.8, 6.6, 6.5, 6.3, 6.6, 4.95, 6.199999999999999, 3.1, 4.2, 6.0, 5.819999999999999, 3.9, 6.2, 5.75, 0.0, 6.0, 0.0, 0.0, 3.25, 3.45, 5.445454545454545, 5.072727272727273, 3.3, 6.6, 5.0, 6.4, 5.933333333333334, 0.0, 6.6, 5.327659574468085, 6.5, 6.050000000000001, 2.7, 0.0, 6.1, 6.1, 0.0, 5.9, 0.0, 5.2, 2.9, 6.0, 0.0, 0.0, 0.0, 6.9, 0.0, 0.0, 3.25, 5.6, 5.5, 5.2, 0.0, 6.1, 5.9, 5.5, 6.4, 5.3, 6.3, 6.8, 6.128571428571428, 5.8, 5.7, 6.1, 6.25, 5.455555555555555, 4.7, 5.8, 5.2, 5.1, 6.15, 1.9, 6.3, 6.3, 6.3, 5.900000000000001, 6.6, 6.3, 6.6, 5.2, 6.199999999999999, 5.6, 6.175000000000001, 6.257142857142857, 3.15, 5.24, 6.0736842105263165, 6.114285714285714, 0.0, 4.270833333333333, 5.6, 5.5, 4.625, 5.966666666666666, 5.9, 5.766666666666667, 0.0, 6.4, 5.5, 5.0, 5.6, 5.5, 3.733333333333333, 5.8, 8.3, 6.866666666666667, 8.8, 7.8999999999999995, 5.9, 5.375, 5.75, 8.8, 8.8, 5.1, 6.0, 3.9, 7.766666666666668, 6.939024390243904, 6.254545454545454, 5.6, 6.475, 5.3, 6.233333333333333, 5.021428571428571, 6.5, 8.1, 5.366666666666667, 6.166666666666667, 3.9333333333333336, 6.7, 4.066666666666666, 5.55, 6.88, 5.6, 8.0, 6.6, 7.1, 0.0, 0.0, 0.0, 3.6, 4.2, 4.0, 6.242857142857142, 3.9, 6.807692307692307, 6.237414965986395, 6.8875, 8.0, 5.880000000000001, 8.466666666666667, 8.45, 8.0, 8.1, 8.285714285714286, 8.134999999999998, 7.550000000000001, 8.2, 8.2, 6.3, 5.85, 6.1, 8.0, 6.4, 7.433333333333334, 6.1, 8.0, 8.1, 7.2, 7.3, 5.8, 7.3, 6.05, 5.9, 7.6, 5.8, 0.0, 8.4, 7.499999999999999, 7.1581395348837225, 1.2666666666666666, 6.199999999999999, 6.8, 5.2, 6.24, 5.6875, 7.5, 8.8, 7.65, 6.5, 7.5, 6.666666666666667, 7.9, 5.80625, 7.9, 7.5, 7.3500000000000005, 6.7, 8.0, 6.6, 6.7, 6.3, 6.6, 6.3, 6.35, 4.2, 6.8, 6.0, 6.3, 7.983333333333334, 7.314285714285716, 0.0, 5.566666666666667, 5.5, 5.82, 0.0, 7.4, 7.0, 6.4, 6.3, 6.433333333333334, 5.921739130434782, 0.0, 3.4, 4.7, 6.7, 5.5, 6.1, 3.4, 6.05, 6.066666666666666, 0.0, 6.5, 5.90909090909091, 8.2, 6.075, 6.1, 5.533333333333332, 6.266666666666667, 4.414285714285714, 7.025, 7.2, 8.1, 6.3, 6.35, 5.86, 6.442105263157894, 5.8, 7.3, 6.05, 5.75, 6.866666666666667, 6.4, 5.8, 6.6, 6.7, 6.3, 6.6, 4.95, 6.199999999999999, 3.6375, 4.2, 6.0, 6.242857142857142, 8.4, 3.9, 7.433333333333333, 6.7142857142857135, 0.0, 7.4, 7.133333333333333, 7.0, 8.3, 8.1, 7.1625000000000005, 8.149999999999999, 0.0, 8.25, 5.6, 8.185714285714285, 8.6, 4.7, 6.294736842105262, 7.2, 5.726666666666666, 3.3, 8.6, 6.6, 5.361538461538462, 6.4, 5.933333333333334, 3.85, 7.2, 7.6, 7.2, 5.820000000000001, 6.5, 6.7, 5.7299999999999995, 2.3666666666666667, 6.1, 6.1, 8.4, 3.65, 5.9, 0.0, 6.944444444444445, 2.9, 7.5, 0.0, 0.0, 7.377272727272729, 7.95217391304348, 0.0, 0.0, 8.4, 5.6, 8.1, 7.8, 5.6, 5.5, 5.2, 0.0, 6.1, 5.9, 5.5, 6.4, 5.3, 6.949999999999999, 6.8, 6.128571428571428, 5.8, 8.2, 5.7, 8.8, 6.1, 7.359999999999999, 7.1, 8.05, 8.3, 8.149999999999999, 8.033333333333333, 7.6, 8.1, 4.7, 5.8, 7.3, 7.3, 5.2, 5.1, 8.2, 7.0, 1.9, 6.3, 6.3, 7.6, 6.3, 7.2, 6.6000000000000005, 6.6, 6.3, 6.6, 5.2, 6.199999999999999, 5.6, 8.8, 7.322727272727272, 7.4375, 8.225, 7.210000000000001, 7.8, 8.7, 6.941666666666667, 6.736363636363635, 7.0307692307692315, 7.800000000000001, 0.0, 5.3, 6.699999999999999, 6.833333333333333, 6.1625, 7.45, 8.2, 6.866666666666667, 6.699999999999999, 7.666666666666667, 8.55, 6.900000000000001, 6.42608695652174, 5.0, 7.4, 5.6, 6.25, 3.733333333333333, 8.2, 6.874074074074075, 6.423333333333334, 6.477777777777778, 8.0, 6.384210526315789, 3.4, 5.966666666666667, 6.875, 8.466666666666665, 7.650000000000001, 8.0, 8.1, 5.953488372093023, 6.351515151515152, 5.726086956521739, 6.736363636363635, 7.092857142857143, 6.3112903225806445, 7.0200000000000005, 7.3, 2.8666666666666663, 5.7148648648648654, 6.699999999999999, 7.352173913043478, 6.1625, 6.4, 7.1, 8.0, 6.599999999999999, 6.7, 6.3, 6.599999999999999, 5.608333333333333, 5.028571428571428, 5.1, 4.446153846153846, 4.764285714285713, 6.325, 5.6800000000000015, 6.244444444444444, 8.4, 4.86, 7.549999999999999, 6.681318681318682, 6.900000000000001, 6.42608695652174, 5.0, 7.4, 3.6916666666666664, 5.6, 6.25, 3.733333333333333]}, "name": "", "parents": ["Canada/Action & Adventure", "China/Action & Adventure", "Colombia/Action & Adventure", "Germany/Action & Adventure", "Hong Kong/Action & Adventure", "Mexico/Action & Adventure", "New Zealand/Action & Adventure", "United Kingdom/Action & Adventure", "United States/Action & Adventure", "Japan/Anime Series", "Australia/Comedies", "Canada/Comedies", "Denmark/Comedies", "France/Comedies", "Germany/Comedies", "India/Comedies", "Mexico/Comedies", "Norway/Comedies", "Philippines/Comedies", "Taiwan/Comedies", "Turkey/Comedies", "United Kingdom/Comedies", "United States/Comedies", "nan/Comedies", "Australia/Crime", "Canada/Crime", "Colombia/Crime", "Mexico/Crime", "Norway/Crime", "Spain/Crime", "United Kingdom/Crime", "United States/Crime", "Canada/Cult Movies", "India/Cult Movies", "/Documentaries", "Bermuda/Documentaries", "Canada/Documentaries", "Ecuador/Documentaries", "Egypt/Documentaries", "Germany/Documentaries", "India/Documentaries", "Israel/Documentaries", "Netherlands/Documentaries", "Ukraine/Documentaries", "United Kingdom/Documentaries", "United States/Documentaries", "Australia/Dramas", "Brazil/Dramas", "Canada/Dramas", "China/Dramas", "Colombia/Dramas", "Denmark/Dramas", "France/Dramas", "Germany/Dramas", "Hong Kong/Dramas", "Hungary/Dramas", "India/Dramas", "Ireland/Dramas", "Japan/Dramas", "Mexico/Dramas", "Norway/Dramas", "Philippines/Dramas", "Spain/Dramas", "Taiwan/Dramas", "United Kingdom/Dramas", "United States/Dramas", "Canada/Family Movies", "India/Family Movies", "Ireland/Family Movies", "United States/Family Movies", "India/Independent Movies and LGBTQ Movies", "United States/Independent Movies and LGBTQ Movies", "/International Movies", "Brazil/International Movies", "Canada/International Movies", "China/International Movies", "Denmark/International Movies", "Egypt/International Movies", "France/International Movies", "Germany/International Movies", "Hong Kong/International Movies", "India/International Movies", "Israel/International Movies", "Mexico/International Movies", "Netherlands/International Movies", "Philippines/International Movies", "Spain/International Movies", "Turkey/International Movies", "Ukraine/International Movies", "United Kingdom/International Movies", "United States/International Movies", "Australia/International TV Shows", "Canada/International TV Shows", "China/International TV Shows", "Colombia/International TV Shows", "Denmark/International TV Shows", "Japan/International TV Shows", "Mexico/International TV Shows", "Spain/International TV Shows", "Taiwan/International TV Shows", "United Kingdom/International TV Shows", "United States/International TV Shows", "Australia/Kid's and Teen", "Canada/Kid's and Teen", "Denmark/Kid's and Teen", "France/Kid's and Teen", "Ireland/Kid's and Teen", "Japan/Kid's and Teen", "Russia/Kid's and Teen", "Singapore/Kid's and Teen", "Spain/Kid's and Teen", "United Kingdom/Kid's and Teen", "United States/Kid's and Teen", "Canada/Movies", "United States/Movies", "nan/Movies", "Canada/Music & Musicals", "Germany/Music & Musicals", "United States/Music & Musicals", "Canada/Other Shows", "United Kingdom/Other Shows", "United States/Other Shows", "Spain/Romantic", "Taiwan/Romantic", "United Kingdom/Romantic", "United States/Romantic", "Turkey/Romantic Movies", "Germany/Sci-Fi & Fantasy", "New Zealand/Sci-Fi & Fantasy", "United Kingdom/Sci-Fi & Fantasy", "United States/Sci-Fi & Fantasy", "United States/Science & Nature TV", "Colombia/Spanish-Language TV Shows", "Mexico/Spanish-Language TV Shows", "Spain/Spanish-Language TV Shows", "United Kingdom/Spanish-Language TV Shows", "United States/Spanish-Language TV Shows", "Germany/Sports Movies", "India/Sports Movies", "United Kingdom/Sports Movies", "United States/Sports Movies", "Canada/Thrillers & Horror", "Germany/Thrillers & Horror", "India/Thrillers & Horror", "United Kingdom/Thrillers & Horror", "United States/Thrillers & Horror", "Argentina/nan", "Australia/nan", "Belgium/nan", "Brazil/nan", "France/nan", "Germany/nan", "Hongkong/nan", "Hungary/nan", "India/nan", "Japan/nan", "Luthvania/nan", "Mexico/nan", "Netherland/nan", "Russia/nan", "Singapore/nan", "South Korea/nan", "Sweden/nan", "United Kingdom/nan", "United States/nan", "ca/nan", "cezhrepublic/nan", "is/nan", "sk/nan", "Australia/Action & Adventure", "China/Action & Adventure", "Hong Kong/Action & Adventure", "India/Action & Adventure", "Japan/Action & Adventure", "South Africa/Action & Adventure", "Taiwan/Action & Adventure", "United Arab Emirates/Action & Adventure", "United Kingdom/Action & Adventure", "United States/Action & Adventure", "Japan/Anime Series", "Argentina/Comedies", "Australia/Comedies", "Belgium/Comedies", "Brazil/Comedies", "Canada/Comedies", "China/Comedies", "France/Comedies", "Germany/Comedies", "Hong Kong/Comedies", "India/Comedies", "Italy/Comedies", "Japan/Comedies", "Mexico/Comedies", "Netherlands/Comedies", "Pakistan/Comedies", "Russia/Comedies", "Singapore/Comedies", "South Korea/Comedies", "Spain/Comedies", "Sweden/Comedies", "Taiwan/Comedies", "Turkey/Comedies", "United Arab Emirates/Comedies", "United Kingdom/Comedies", "United States/Comedies", "nan/Comedies", "Canada/Crime", "United States/Crime", "Argentina/Documentaries", "Australia/Documentaries", "Belgium/Documentaries", "Brazil/Documentaries", "Canada/Documentaries", "China/Documentaries", "Ireland/Documentaries", "Italy/Documentaries", "Mexico/Documentaries", "New Zealand/Documentaries", "Spain/Documentaries", "United Kingdom/Documentaries", "United States/Documentaries", "nan/Documentaries", "Argentina/Dramas", "Australia/Dramas", "Belgium/Dramas", "Brazil/Dramas", "Canada/Dramas", "France/Dramas", "Hong Kong/Dramas", "India/Dramas", "Mexico/Dramas", "Netherlands/Dramas", "Pakistan/Dramas", "Philippines/Dramas", "Poland/Dramas", "Qatar/Dramas", "South Korea/Dramas", "Spain/Dramas", "Sweden/Dramas", "Taiwan/Dramas", "Turkey/Dramas", "United Arab Emirates/Dramas", "United States/Dramas", "nan/Dramas", "Australia/Family Movies", "Brazil/Family Movies", "Canada/Family Movies", "Germany/Family Movies", "New Zealand/Family Movies", "United Arab Emirates/Family Movies", "United Kingdom/Family Movies", "United States/Family Movies", "nan/Family Movies", "Bulgaria/Horror Movies", "Singapore/Horror Movies", "United Kingdom/Horror Movies", "United States/Horror Movies", "Argentina/Independent Movies and LGBTQ Movies", "Bulgaria/Independent Movies and LGBTQ Movies", "France/Independent Movies and LGBTQ Movies", "India/Independent Movies and LGBTQ Movies", "Spain/Independent Movies and LGBTQ Movies", "United Kingdom/Independent Movies and LGBTQ Movies", "United States/Independent Movies and LGBTQ Movies", "Argentina/International Movies", "Australia/International Movies", "Belgium/International Movies", "Brazil/International Movies", "Canada/International Movies", "China/International Movies", "France/International Movies", "Germany/International Movies", "Hong Kong/International Movies", "India/International Movies", "Ireland/International Movies", "Italy/International Movies", "Japan/International Movies", "Mexico/International Movies", "Netherlands/International Movies", "New Zealand/International Movies", "Pakistan/International Movies", "Philippines/International Movies", "Poland/International Movies", "Qatar/International Movies", "Singapore/International Movies", "South Korea/International Movies", "Spain/International Movies", "Sweden/International Movies", "Taiwan/International Movies", "Turkey/International Movies", "United Arab Emirates/International Movies", "United Kingdom/International Movies", "United States/International Movies", "nan/International Movies", "Canada/International TV Shows", "Japan/International TV Shows", "South Korea/International TV Shows", "Taiwan/International TV Shows", "Australia/Kid's and Teen", "Canada/Kid's and Teen", "France/Kid's and Teen", "Germany/Kid's and Teen", "Italy/Kid's and Teen", "Japan/Kid's and Teen", "Netherlands/Kid's and Teen", "New Zealand/Kid's and Teen", "Russia/Kid's and Teen", "United Kingdom/Kid's and Teen", "United States/Kid's and Teen", "nan/Kid's and Teen", "Canada/Movies", "United States/Movies", "nan/Movies", "Australia/Music & Musicals", "Belgium/Music & Musicals", "Germany/Music & Musicals", "India/Music & Musicals", "Spain/Music & Musicals", "United States/Music & Musicals", "nan/Music & Musicals", "Canada/Other Shows", "Russia/Other Shows", "South Korea/Other Shows", "United Kingdom/Other Shows", "United States/Other Shows", "Canada/Romantic", "South Korea/Romantic", "Taiwan/Romantic", "Argentina/Romantic Movies", "Australia/Romantic Movies", "Belgium/Romantic Movies", "Canada/Romantic Movies", "China/Romantic Movies", "France/Romantic Movies", "Germany/Romantic Movies", "Philippines/Romantic Movies", "Spain/Romantic Movies", "Turkey/Romantic Movies", "United Kingdom/Romantic Movies", "United States/Romantic Movies", "Australia/Sci-Fi & Fantasy", "Netherlands/Sci-Fi & Fantasy", "South Korea/Sci-Fi & Fantasy", "United Kingdom/Sci-Fi & Fantasy", "United States/Sci-Fi & Fantasy", "Australia/Sports Movies", "Canada/Sports Movies", "Spain/Sports Movies", "Turkey/Sports Movies", "United States/Sports Movies", "nan/Sports Movies", "Argentina/Thrillers & Horror", "Brazil/Thrillers & Horror", "France/Thrillers & Horror", "India/Thrillers & Horror", "Philippines/Thrillers & Horror", "Poland/Thrillers & Horror", "Qatar/Thrillers & Horror", "Singapore/Thrillers & Horror", "South Korea/Thrillers & Horror", "Spain/Thrillers & Horror", "United States/Thrillers & Horror", "Argentina/nan", "Belgium/nan", "Germany/nan", "Hongkong/nan", "Hungary/nan", "Italy/nan", "Japan/nan", "Luthvania/nan", "Mexico/nan", "Netherland/nan", "Russia/nan", "South Korea/nan", "Sweden/nan", "United Kingdom/nan", "ca/nan", "cezhrepublic/nan", "gr/nan", "pt/nan", "sk/nan", "th/nan", "Australia", "Canada", "China", "Colombia", "Germany", "Hong Kong", "India", "Japan", "Mexico", "New Zealand", "South Africa", "Taiwan", "United Arab Emirates", "United Kingdom", "United States", "Japan", "Argentina", "Australia", "Belgium", "Brazil", "Canada", "China", "Denmark", "France", "Germany", "Hong Kong", "India", "Italy", "Japan", "Mexico", "Netherlands", "Norway", "Pakistan", "Philippines", "Russia", "Singapore", "South Korea", "Spain", "Sweden", "Taiwan", "Turkey", "United Arab Emirates", "United Kingdom", "United States", "nan", "Australia", "Canada", "Colombia", "Mexico", "Norway", "Spain", "United Kingdom", "United States", "Canada", "India", "", "Argentina", "Australia", "Belgium", "Bermuda", "Brazil", "Canada", "China", "Ecuador", "Egypt", "Germany", "India", "Ireland", "Israel", "Italy", "Mexico", "Netherlands", "New Zealand", "Spain", "Ukraine", "United Kingdom", "United States", "nan", "Argentina", "Australia", "Belgium", "Brazil", "Canada", "China", "Colombia", "Denmark", "France", "Germany", "Hong Kong", "Hungary", "India", "Ireland", "Japan", "Mexico", "Netherlands", "Norway", "Pakistan", "Philippines", "Poland", "Qatar", "South Korea", "Spain", "Sweden", "Taiwan", "Turkey", "United Arab Emirates", "United Kingdom", "United States", "nan", "Australia", "Brazil", "Canada", "Germany", "India", "Ireland", "New Zealand", "United Arab Emirates", "United Kingdom", "United States", "nan", "Bulgaria", "Singapore", "United Kingdom", "United States", "Argentina", "Bulgaria", "France", "India", "Spain", "United Kingdom", "United States", "", "Argentina", "Australia", "Belgium", "Brazil", "Canada", "China", "Denmark", "Egypt", "France", "Germany", "Hong Kong", "India", "Ireland", "Israel", "Italy", "Japan", "Mexico", "Netherlands", "New Zealand", "Pakistan", "Philippines", "Poland", "Qatar", "Singapore", "South Korea", "Spain", "Sweden", "Taiwan", "Turkey", "Ukraine", "United Arab Emirates", "United Kingdom", "United States", "nan", "Australia", "Canada", "China", "Colombia", "Denmark", "Japan", "Mexico", "South Korea", "Spain", "Taiwan", "United Kingdom", "United States", "Australia", "Canada", "Denmark", "France", "Germany", "Ireland", "Italy", "Japan", "Netherlands", "New Zealand", "Russia", "Singapore", "Spain", "United Kingdom", "United States", "nan", "Canada", "United States", "nan", "Australia", "Belgium", "Canada", "Germany", "India", "Spain", "United States", "nan", "Canada", "Russia", "South Korea", "United Kingdom", "United States", "Canada", "South Korea", "Spain", "Taiwan", "United Kingdom", "United States", "Argentina", "Australia", "Belgium", "Canada", "China", "France", "Germany", "Philippines", "Spain", "Turkey", "United Kingdom", "United States", "Australia", "Germany", "Netherlands", "New Zealand", "South Korea", "United Kingdom", "United States", "United States", "Colombia", "Mexico", "Spain", "United Kingdom", "United States", "Australia", "Canada", "Germany", "India", "Spain", "Turkey", "United Kingdom", "United States", "nan", "Argentina", "Brazil", "Canada", "France", "Germany", "India", "Philippines", "Poland", "Qatar", "Singapore", "South Korea", "Spain", "United Kingdom", "United States", "Argentina", "Australia", "Belgium", "Brazil", "France", "Germany", "Hongkong", "Hungary", "India", "Italy", "Japan", "Luthvania", "Mexico", "Netherland", "Russia", "Singapore", "South Korea", "Sweden", "United Kingdom", "United States", "ca", "cezhrepublic", "gr", "is", "pt", "sk", "th", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", ""], "type": "treemap", "values": [1, 3, 1, 2, 2, 1, 2, 5, 23, 7, 1, 3, 1, 1, 1, 2, 2, 1, 1, 1, 2, 8, 62, 4, 2, 3, 3, 2, 1, 1, 7, 19, 2, 1, 1, 1, 5, 1, 1, 1, 1, 1, 1, 1, 6, 27, 3, 1, 5, 2, 1, 2, 2, 4, 2, 1, 6, 1, 1, 3, 1, 1, 1, 1, 6, 42, 2, 1, 1, 4, 2, 1, 1, 1, 1, 2, 1, 1, 2, 1, 3, 9, 1, 2, 1, 1, 1, 2, 1, 6, 3, 1, 2, 1, 2, 1, 7, 2, 2, 2, 14, 2, 1, 8, 1, 4, 1, 2, 1, 1, 1, 2, 13, 1, 6, 1, 1, 1, 7, 4, 20, 22, 1, 2, 1, 4, 1, 1, 2, 3, 16, 2, 2, 2, 3, 1, 1, 1, 1, 1, 3, 2, 1, 3, 1, 14, 9, 4, 8, 2, 1, 7, 14, 6, 2, 11, 1, 2, 4, 5, 1, 1, 8, 20, 2, 2, 11, 1, 1, 1, 3, 5, 4, 2, 1, 1, 1, 1, 18, 4, 1, 3, 1, 3, 11, 1, 8, 2, 3, 2, 3, 2, 3, 1, 1, 1, 1, 1, 3, 1, 1, 5, 1, 5, 85, 4, 2, 1, 1, 2, 1, 1, 1, 1, 1, 2, 1, 1, 2, 2, 16, 3, 2, 2, 1, 4, 3, 3, 1, 10, 1, 1, 1, 2, 1, 1, 1, 1, 1, 2, 1, 1, 21, 1, 3, 1, 3, 1, 1, 1, 3, 19, 1, 1, 1, 1, 8, 1, 1, 2, 4, 1, 1, 21, 4, 1, 3, 5, 6, 2, 6, 1, 7, 10, 1, 2, 2, 1, 3, 1, 1, 2, 1, 1, 2, 2, 7, 1, 1, 5, 1, 3, 4, 2, 1, 1, 1, 2, 2, 11, 11, 2, 1, 11, 2, 3, 1, 1, 47, 2, 2, 4, 2, 1, 1, 1, 1, 1, 2, 2, 1, 1, 1, 2, 1, 1, 1, 2, 1, 1, 1, 1, 1, 2, 1, 1, 1, 1, 1, 7, 1, 1, 1, 2, 9, 1, 1, 1, 1, 2, 2, 1, 1, 1, 3, 1, 1, 1, 1, 2, 1, 8, 7, 2, 5, 19, 7, 7, 24, 1, 1, 4, 3, 2, 9, 1, 1, 12, 1, 1, 1, 3, 1, 1, 6, 1, 2, 7, 4, 2, 1, 2, 1, 1, 1, 6, 41, 11, 1, 4, 1, 3, 14, 1, 1, 9, 3, 3, 4, 3, 2, 5, 1, 1, 1, 1, 1, 1, 1, 3, 1, 2, 7, 1, 13, 147, 8, 2, 5, 3, 2, 1, 1, 7, 20, 2, 1, 1, 1, 2, 1, 1, 1, 6, 1, 1, 1, 1, 1, 1, 1, 2, 1, 1, 1, 2, 1, 8, 43, 3, 2, 5, 1, 5, 8, 2, 1, 2, 5, 4, 3, 1, 16, 1, 1, 4, 1, 1, 1, 3, 1, 1, 1, 2, 1, 3, 1, 1, 6, 63, 1, 3, 1, 5, 1, 1, 1, 1, 1, 3, 23, 1, 1, 1, 1, 8, 1, 1, 2, 6, 1, 1, 22, 1, 4, 1, 3, 6, 7, 4, 1, 1, 8, 2, 10, 19, 1, 1, 2, 2, 3, 4, 1, 1, 3, 1, 1, 2, 2, 8, 1, 1, 7, 1, 1, 9, 7, 2, 1, 3, 1, 2, 1, 8, 2, 1, 2, 4, 14, 2, 3, 19, 1, 15, 2, 1, 1, 13, 2, 3, 2, 1, 1, 3, 60, 2, 3, 10, 3, 1, 1, 1, 2, 1, 1, 9, 2, 5, 1, 1, 22, 23, 1, 1, 1, 4, 1, 4, 1, 1, 1, 1, 1, 2, 1, 1, 1, 2, 1, 7, 1, 1, 1, 2, 1, 5, 25, 2, 2, 2, 3, 1, 1, 1, 1, 1, 1, 1, 1, 1, 5, 2, 1, 1, 2, 1, 1, 6, 1, 1, 1, 1, 2, 1, 1, 22, 16, 4, 10, 2, 1, 12, 33, 13, 2, 7, 35, 2, 3, 8, 8, 1, 3, 17, 21, 2, 3, 23, 1, 1, 1, 2, 3, 2, 27, 30, 18, 1, 19, 2, 84, 16, 9, 6, 1, 2, 43, 33, 23, 33, 14, 62, 5, 2, 15, 74, 2, 23, 8, 10, 10, 3, 3, 9, 3, 3, 12, 7, 1, 13, 28, 20, 15, 18, 2, 5, 124, 546, 3, 23, 1, 1, 24, 1, 2, 3]}],                        {"coloraxis": {"colorbar": {"title": {"text": "rating_num"}}, "colorscale": [[0.0, "rgb(103,0,31)"], [0.1, "rgb(178,24,43)"], [0.2, "rgb(214,96,77)"], [0.3, "rgb(244,165,130)"], [0.4, "rgb(253,219,199)"], [0.5, "rgb(247,247,247)"], [0.6, "rgb(209,229,240)"], [0.7, "rgb(146,197,222)"], [0.8, "rgb(67,147,195)"], [0.9, "rgb(33,102,172)"], [1.0, "rgb(5,48,97)"]]}, "legend": {"tracegroupgap": 0}, "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Content analysis of each country by genre"}},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('d9de7d85-1792-468a-8bc4-d7444e2cbb51');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>


## Duration analysis


```python
#making a nes dataframe by selecting specific columns
duration_analysis = rating_analysis_genre.loc[:,['netflixid','type','duration','rating_standard','rating_num']]
# duration_analysis        #printing duration analysis
```


```python
#getting specific rows where we find the movie because we are anlyzing the length of movie
movie_analysis = duration_analysis.loc[(duration_analysis['type'] =='Movie')]
 
#checking for the duplicates and drop the duplicated items in the dataframe
movie_analysis_edited = movie_analysis.drop_duplicates(subset=['netflixid'])

#splitting the duration column to actual duration and to units of duration measurrement(mins)
movie_analysis_edited[['duration_in_mins','duration_units']] = movie_analysis_edited.duration.str.split(" ",expand=True,)

#droping nan values
movie_analysis_edited = movie_analysis_edited.dropna()
#but all the values in duration column was not in same format so it wasnot easily splitted

#dataframe of high-rated movies with their duration
high_movie_analysis_edited = movie_analysis_edited[movie_analysis_edited.rating_standard == 'High-rated']

```


```python
#duration column had different formatted values so used regular expression to ge the float numbers of out it.
s= movie_analysis_edited.duration.to_list()  #making a list
lis=[]
to_sum=[]
for each in s:
    counter = 0
    for each in re.findall(r'\d+',each):   #finding all the values using regular expression
        if counter == 0:  #setting the condition
            x =float(each)    #converting it to float
            if x ==1: 
                x = 60
            elif x ==2:
                x =120
            sume = x   #assigning the value
            #print(f"x is{x}")
            #print(f"sume is {sume}")
            
        else:
            y = float(each)   #converting to float
            #print(y)
            sume=sume+y
            #print(f"sume is {sume}")
        counter = counter +1
        #print(counter)
    lis.append(sume)  #appendig the list

movie_analysis_edited['duration_in_min'] = lis  #making a new column with the appended list to get the float numbers that represnet the duration

#movie_analysis_edited   #prints the dataframe

```


```python
#plotting the histogram of distribution of movies with both high-standard and low-standard to analyze their distribution pattern
fig = px.histogram(movie_analysis_edited, x="duration_in_min", color="rating_standard", 
                   nbins=18,title='Distribution of duration of movies by rating standard', marginal="box") # can be `box`, `violin`)
                   
fig.show()
```


<div>                            <div id="1b4afc19-ca86-4061-9902-024129b7ea0e" class="plotly-graph-div" style="height:525px; width:100%;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("1b4afc19-ca86-4061-9902-024129b7ea0e")) {                    Plotly.newPlot(                        "1b4afc19-ca86-4061-9902-024129b7ea0e",                        [{"alignmentgroup": "True", "bingroup": "x", "hovertemplate": "rating_standard=High-rated<br>duration_in_min=%{x}<br>count=%{y}<extra></extra>", "legendgroup": "High-rated", "marker": {"color": "#636efa"}, "name": "High-rated", "nbinsx": 18, "offsetgroup": "High-rated", "orientation": "v", "showlegend": true, "type": "histogram", "x": [40.0, 100.0, 99.0, 84.0, 90.0, 57.0, 101.0, 90.0, 64.0, 64.0, 50.0, 59.0, 72.0, 89.0, 67.0, 90.0, 114.0, 64.0, 65.0, 75.0, 62.0, 95.0, 80.0, 61.0, 60.0, 74.0, 66.0, 65.0, 63.0, 61.0, 79.0, 58.0, 46.0, 74.0, 70.0, 71.0, 87.0, 74.0, 78.0, 65.0, 71.0, 122.0, 46.0, 59.0, 76.0, 84.0, 81.0, 29.0, 88.0, 26.0, 48.0, 68.0, 77.0, 66.0, 62.0, 72.0, 77.0, 70.0, 74.0, 59.0, 35.0, 66.0, 54.0, 107.0, 30.0, 142.0, 112.0, 94.0, 101.0, 82.0, 137.0, 97.0, 136.0, 138.0, 95.0, 126.0, 133.0, 104.0, 84.0, 160.0, 105.0, 40.0, 58.0, 95.0, 103.0, 101.0, 47.0, 60.0, 103.0, 53.0, 143.0, 92.0, 80.0, 105.0, 120.0, 102.0, 107.0, 55.0, 130.0, 62.0, 27.0, 100.0, 99.0, 127.0, 158.0, 108.0, 104.0, 99.0, 132.0, 100.0, 103.0, 105.0, 107.0, 108.0, 146.0, 137.0, 148.0, 201.0, 179.0, 110.0, 113.0, 128.0], "xaxis": "x", "yaxis": "y"}, {"alignmentgroup": "True", "hovertemplate": "rating_standard=High-rated<br>duration_in_min=%{x}<extra></extra>", "legendgroup": "High-rated", "marker": {"color": "#636efa"}, "name": "High-rated", "notched": true, "offsetgroup": "High-rated", "showlegend": false, "type": "box", "x": [40.0, 100.0, 99.0, 84.0, 90.0, 57.0, 101.0, 90.0, 64.0, 64.0, 50.0, 59.0, 72.0, 89.0, 67.0, 90.0, 114.0, 64.0, 65.0, 75.0, 62.0, 95.0, 80.0, 61.0, 60.0, 74.0, 66.0, 65.0, 63.0, 61.0, 79.0, 58.0, 46.0, 74.0, 70.0, 71.0, 87.0, 74.0, 78.0, 65.0, 71.0, 122.0, 46.0, 59.0, 76.0, 84.0, 81.0, 29.0, 88.0, 26.0, 48.0, 68.0, 77.0, 66.0, 62.0, 72.0, 77.0, 70.0, 74.0, 59.0, 35.0, 66.0, 54.0, 107.0, 30.0, 142.0, 112.0, 94.0, 101.0, 82.0, 137.0, 97.0, 136.0, 138.0, 95.0, 126.0, 133.0, 104.0, 84.0, 160.0, 105.0, 40.0, 58.0, 95.0, 103.0, 101.0, 47.0, 60.0, 103.0, 53.0, 143.0, 92.0, 80.0, 105.0, 120.0, 102.0, 107.0, 55.0, 130.0, 62.0, 27.0, 100.0, 99.0, 127.0, 158.0, 108.0, 104.0, 99.0, 132.0, 100.0, 103.0, 105.0, 107.0, 108.0, 146.0, 137.0, 148.0, 201.0, 179.0, 110.0, 113.0, 128.0], "xaxis": "x2", "yaxis": "y2"}, {"alignmentgroup": "True", "bingroup": "x", "hovertemplate": "rating_standard=Low-rated<br>duration_in_min=%{x}<br>count=%{y}<extra></extra>", "legendgroup": "Low-rated", "marker": {"color": "#EF553B"}, "name": "Low-rated", "nbinsx": 18, "offsetgroup": "Low-rated", "orientation": "v", "showlegend": true, "type": "histogram", "x": [24.0, 63.0, 64.0, 60.0, 71.0, 68.0, 64.0, 63.0, 71.0, 81.0, 61.0, 62.0, 66.0, 22.0, 44.0, 67.0, 92.0, 113.0, 83.0, 58.0, 78.0, 64.0, 53.0, 57.0, 58.0, 58.0, 82.0, 65.0, 89.0, 81.0, 66.0, 62.0, 66.0, 86.0, 72.0, 75.0, 92.0, 130.0, 22.0, 102.0, 61.0, 93.0, 72.0, 60.0, 116.0, 78.0, 24.0, 24.0, 23.0, 24.0, 24.0, 68.0, 67.0, 83.0, 65.0, 22.0, 63.0, 60.0, 60.0, 60.0, 47.0, 70.0, 83.0, 54.0, 90.0, 75.0, 97.0, 62.0, 79.0, 76.0, 54.0, 84.0, 61.0, 96.0, 59.0, 99.0, 84.0, 112.0, 109.0, 86.0, 81.0, 80.0, 126.0, 75.0, 112.0, 109.0, 90.0, 95.0, 111.0, 88.0, 85.0, 105.0, 86.0, 90.0, 91.0, 86.0, 89.0, 119.0, 147.0, 104.0, 122.0, 125.0, 154.0, 146.0, 101.0, 147.0, 135.0, 47.0, 105.0, 97.0, 82.0, 91.0, 91.0, 129.0, 104.0, 126.0, 69.0, 106.0, 118.0, 98.0, 93.0, 89.0, 116.0, 103.0, 74.0, 69.0, 91.0, 77.0, 117.0, 99.0, 101.0, 98.0, 101.0, 104.0, 90.0, 75.0, 92.0, 24.0, 102.0, 96.0, 133.0, 85.0, 105.0, 104.0, 106.0, 78.0, 113.0, 95.0, 91.0, 75.0, 98.0, 85.0, 78.0, 86.0, 136.0, 104.0, 65.0, 91.0, 97.0, 24.0, 65.0, 123.0, 97.0, 104.0, 71.0, 94.0, 179.0, 38.0, 74.0, 89.0, 57.0, 82.0, 102.0, 80.0, 124.0, 78.0, 82.0, 105.0, 93.0, 77.0, 120.0, 81.0, 72.0, 26.0, 99.0, 100.0, 196.0, 90.0, 104.0, 92.0, 85.0, 94.0, 105.0, 96.0, 91.0, 110.0, 95.0, 141.0, 107.0, 110.0, 88.0, 66.0, 115.0, 87.0, 103.0, 96.0, 115.0, 96.0, 104.0, 101.0, 97.0, 92.0, 91.0, 103.0, 130.0, 106.0, 97.0, 89.0, 87.0, 81.0, 96.0], "xaxis": "x", "yaxis": "y"}, {"alignmentgroup": "True", "hovertemplate": "rating_standard=Low-rated<br>duration_in_min=%{x}<extra></extra>", "legendgroup": "Low-rated", "marker": {"color": "#EF553B"}, "name": "Low-rated", "notched": true, "offsetgroup": "Low-rated", "showlegend": false, "type": "box", "x": [24.0, 63.0, 64.0, 60.0, 71.0, 68.0, 64.0, 63.0, 71.0, 81.0, 61.0, 62.0, 66.0, 22.0, 44.0, 67.0, 92.0, 113.0, 83.0, 58.0, 78.0, 64.0, 53.0, 57.0, 58.0, 58.0, 82.0, 65.0, 89.0, 81.0, 66.0, 62.0, 66.0, 86.0, 72.0, 75.0, 92.0, 130.0, 22.0, 102.0, 61.0, 93.0, 72.0, 60.0, 116.0, 78.0, 24.0, 24.0, 23.0, 24.0, 24.0, 68.0, 67.0, 83.0, 65.0, 22.0, 63.0, 60.0, 60.0, 60.0, 47.0, 70.0, 83.0, 54.0, 90.0, 75.0, 97.0, 62.0, 79.0, 76.0, 54.0, 84.0, 61.0, 96.0, 59.0, 99.0, 84.0, 112.0, 109.0, 86.0, 81.0, 80.0, 126.0, 75.0, 112.0, 109.0, 90.0, 95.0, 111.0, 88.0, 85.0, 105.0, 86.0, 90.0, 91.0, 86.0, 89.0, 119.0, 147.0, 104.0, 122.0, 125.0, 154.0, 146.0, 101.0, 147.0, 135.0, 47.0, 105.0, 97.0, 82.0, 91.0, 91.0, 129.0, 104.0, 126.0, 69.0, 106.0, 118.0, 98.0, 93.0, 89.0, 116.0, 103.0, 74.0, 69.0, 91.0, 77.0, 117.0, 99.0, 101.0, 98.0, 101.0, 104.0, 90.0, 75.0, 92.0, 24.0, 102.0, 96.0, 133.0, 85.0, 105.0, 104.0, 106.0, 78.0, 113.0, 95.0, 91.0, 75.0, 98.0, 85.0, 78.0, 86.0, 136.0, 104.0, 65.0, 91.0, 97.0, 24.0, 65.0, 123.0, 97.0, 104.0, 71.0, 94.0, 179.0, 38.0, 74.0, 89.0, 57.0, 82.0, 102.0, 80.0, 124.0, 78.0, 82.0, 105.0, 93.0, 77.0, 120.0, 81.0, 72.0, 26.0, 99.0, 100.0, 196.0, 90.0, 104.0, 92.0, 85.0, 94.0, 105.0, 96.0, 91.0, 110.0, 95.0, 141.0, 107.0, 110.0, 88.0, 66.0, 115.0, 87.0, 103.0, 96.0, 115.0, 96.0, 104.0, 101.0, 97.0, 92.0, 91.0, 103.0, 130.0, 106.0, 97.0, 89.0, 87.0, 81.0, 96.0], "xaxis": "x2", "yaxis": "y2"}],                        {"barmode": "relative", "legend": {"title": {"text": "rating_standard"}, "tracegroupgap": 0}, "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Distribution of duration of movies by rating standard"}, "xaxis": {"anchor": "y", "domain": [0.0, 1.0], "title": {"text": "duration_in_min"}}, "xaxis2": {"anchor": "y2", "domain": [0.0, 1.0], "matches": "x", "showgrid": true, "showticklabels": false}, "yaxis": {"anchor": "x", "domain": [0.0, 0.7326], "title": {"text": "count"}}, "yaxis2": {"anchor": "x2", "domain": [0.7426, 1.0], "matches": "y2", "showgrid": false, "showline": false, "showticklabels": false, "ticks": ""}},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('1b4afc19-ca86-4061-9902-024129b7ea0e');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>



```python
#plotting histogram to analyze the distribution of duration of high-rated movies
fig = px.histogram(high_movie_analysis_edited, x="duration_in_mins", 
                   title='Distribution of duration of high-rated movies', marginal="box",nbins=18)
fig.show()
```


<div>                            <div id="3e8b689e-7ce5-4d83-899e-55b60a1f44ef" class="plotly-graph-div" style="height:525px; width:100%;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("3e8b689e-7ce5-4d83-899e-55b60a1f44ef")) {                    Plotly.newPlot(                        "3e8b689e-7ce5-4d83-899e-55b60a1f44ef",                        [{"alignmentgroup": "True", "bingroup": "x", "hovertemplate": "duration_in_mins=%{x}<br>count=%{y}<extra></extra>", "legendgroup": "", "marker": {"color": "#636efa"}, "name": "", "nbinsx": 18, "offsetgroup": "", "orientation": "v", "showlegend": false, "type": "histogram", "x": ["40", "100", "99", "84", "90", "57", "101", "90", "64", "64", "50", "59", "72", "89", "67", "90", "114", "64", "65", "75", "62", "95", "80", "61", "60", "74", "66", "65", "63", "61", "79", "58", "46", "74", "70", "71", "87", "74", "78", "65", "71", "122", "46", "59", "76", "84", "81", "29", "88", "26", "48", "68", "77", "66", "62", "72", "77", "70", "74", "59", "35", "66", "54", "107", "30", "142", "112", "94", "101", "82", "137", "97", "136", "138", "95", "126", "133", "104", "84", "160", "105", "40", "58", "95", "103", "101", "47", "60", "103", "53", "143", "92", "80", "105", "120", "102", "107", "55", "130", "62", "27", "100", "99", "127", "158", "108", "104", "99", "132", "100", "103", "105", "107", "108", "146", "137", "148", "201", "179", "110", "113", "128"], "xaxis": "x", "yaxis": "y"}, {"alignmentgroup": "True", "hovertemplate": "duration_in_mins=%{x}<extra></extra>", "legendgroup": "", "marker": {"color": "#636efa"}, "name": "", "notched": true, "offsetgroup": "", "showlegend": false, "type": "box", "x": ["40", "100", "99", "84", "90", "57", "101", "90", "64", "64", "50", "59", "72", "89", "67", "90", "114", "64", "65", "75", "62", "95", "80", "61", "60", "74", "66", "65", "63", "61", "79", "58", "46", "74", "70", "71", "87", "74", "78", "65", "71", "122", "46", "59", "76", "84", "81", "29", "88", "26", "48", "68", "77", "66", "62", "72", "77", "70", "74", "59", "35", "66", "54", "107", "30", "142", "112", "94", "101", "82", "137", "97", "136", "138", "95", "126", "133", "104", "84", "160", "105", "40", "58", "95", "103", "101", "47", "60", "103", "53", "143", "92", "80", "105", "120", "102", "107", "55", "130", "62", "27", "100", "99", "127", "158", "108", "104", "99", "132", "100", "103", "105", "107", "108", "146", "137", "148", "201", "179", "110", "113", "128"], "xaxis": "x2", "yaxis": "y2"}],                        {"barmode": "relative", "legend": {"tracegroupgap": 0}, "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Distribution of duration of high-rated movies"}, "xaxis": {"anchor": "y", "domain": [0.0, 1.0], "title": {"text": "duration_in_mins"}}, "xaxis2": {"anchor": "y2", "domain": [0.0, 1.0], "matches": "x", "showgrid": true, "showticklabels": false}, "yaxis": {"anchor": "x", "domain": [0.0, 0.8316], "title": {"text": "count"}}, "yaxis2": {"anchor": "x2", "domain": [0.8416, 1.0], "matches": "y2", "showgrid": false, "showline": false, "showticklabels": false, "ticks": ""}},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('3e8b689e-7ce5-4d83-899e-55b60a1f44ef');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>


## Finding co-relation between duration and rating


```python
#analyzing the realation of duration and rating
# to see if increase or decrease in length of movie would impact the rating
fig = px.scatter(movie_analysis_edited, x="duration_in_min", y="rating_num", color="rating_standard",
                 title = 'Analysis of co-relation between rating and duration',
                  hover_data=['type'])
fig.show()
```


<div>                            <div id="95383646-a71b-44c2-b459-48d290ba93e4" class="plotly-graph-div" style="height:525px; width:100%;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("95383646-a71b-44c2-b459-48d290ba93e4")) {                    Plotly.newPlot(                        "95383646-a71b-44c2-b459-48d290ba93e4",                        [{"customdata": [["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"]], "hovertemplate": "rating_standard=High-rated<br>duration_in_min=%{x}<br>rating_num=%{y}<br>type=%{customdata[0]}<extra></extra>", "legendgroup": "High-rated", "marker": {"color": "#636efa", "symbol": "circle"}, "mode": "markers", "name": "High-rated", "orientation": "v", "showlegend": true, "type": "scatter", "x": [40.0, 100.0, 99.0, 84.0, 90.0, 57.0, 101.0, 90.0, 64.0, 64.0, 50.0, 59.0, 72.0, 89.0, 67.0, 90.0, 114.0, 64.0, 65.0, 75.0, 62.0, 95.0, 80.0, 61.0, 60.0, 74.0, 66.0, 65.0, 63.0, 61.0, 79.0, 58.0, 46.0, 74.0, 70.0, 71.0, 87.0, 74.0, 78.0, 65.0, 71.0, 122.0, 46.0, 59.0, 76.0, 84.0, 81.0, 29.0, 88.0, 26.0, 48.0, 68.0, 77.0, 66.0, 62.0, 72.0, 77.0, 70.0, 74.0, 59.0, 35.0, 66.0, 54.0, 107.0, 30.0, 142.0, 112.0, 94.0, 101.0, 82.0, 137.0, 97.0, 136.0, 138.0, 95.0, 126.0, 133.0, 104.0, 84.0, 160.0, 105.0, 40.0, 58.0, 95.0, 103.0, 101.0, 47.0, 60.0, 103.0, 53.0, 143.0, 92.0, 80.0, 105.0, 120.0, 102.0, 107.0, 55.0, 130.0, 62.0, 27.0, 100.0, 99.0, 127.0, 158.0, 108.0, 104.0, 99.0, 132.0, 100.0, 103.0, 105.0, 107.0, 108.0, 146.0, 137.0, 148.0, 201.0, 179.0, 110.0, 113.0, 128.0], "xaxis": "x", "y": [7.4, 7.1, 7.2, 8.5, 8.3, 7.3, 8.2, 7.2, 7.5, 7.4, 7.1, 7.8, 7.1, 7.4, 7.6, 7.5, 8.2, 7.2, 7.5, 7.0, 7.9, 7.4, 7.3, 7.2, 7.5, 7.1, 7.1, 7.9, 7.1, 7.5, 7.9, 7.3, 8.0, 7.8, 8.2, 7.3, 7.7, 7.5, 7.3, 7.1, 7.6, 8.3, 7.0, 7.2, 7.6, 7.3, 8.4, 7.8, 7.4, 7.1, 7.7, 7.0, 8.1, 7.8, 7.3, 8.0, 7.8, 7.6, 7.6, 7.6, 7.4, 7.1, 7.0, 7.2, 7.0, 8.1, 7.6, 8.0, 7.0, 7.2, 7.7, 7.4, 8.7, 7.2, 7.7, 7.1, 7.1, 7.2, 7.4, 8.2, 7.0, 7.3, 7.5, 7.2, 7.6, 7.0, 7.9, 8.4, 7.6, 7.4, 7.2, 7.4, 8.0, 7.3, 7.1, 7.3, 8.4, 7.3, 7.1, 7.4, 7.0, 7.4, 8.2, 7.4, 7.0, 7.0, 7.8, 8.4, 8.2, 8.2, 7.4, 8.1, 8.0, 7.5, 7.5, 7.3, 8.8, 8.9, 8.7, 7.6, 7.2, 7.6], "yaxis": "y"}, {"customdata": [["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"], ["Movie"]], "hovertemplate": "rating_standard=Low-rated<br>duration_in_min=%{x}<br>rating_num=%{y}<br>type=%{customdata[0]}<extra></extra>", "legendgroup": "Low-rated", "marker": {"color": "#EF553B", "symbol": "circle"}, "mode": "markers", "name": "Low-rated", "orientation": "v", "showlegend": true, "type": "scatter", "x": [24.0, 63.0, 64.0, 60.0, 71.0, 68.0, 64.0, 63.0, 71.0, 81.0, 61.0, 62.0, 66.0, 22.0, 44.0, 67.0, 92.0, 113.0, 83.0, 58.0, 78.0, 64.0, 53.0, 57.0, 58.0, 58.0, 82.0, 65.0, 89.0, 81.0, 66.0, 62.0, 66.0, 86.0, 72.0, 75.0, 92.0, 130.0, 22.0, 102.0, 61.0, 93.0, 72.0, 60.0, 116.0, 78.0, 24.0, 24.0, 23.0, 24.0, 24.0, 68.0, 67.0, 83.0, 65.0, 22.0, 63.0, 60.0, 60.0, 60.0, 47.0, 70.0, 83.0, 54.0, 90.0, 75.0, 97.0, 62.0, 79.0, 76.0, 54.0, 84.0, 61.0, 96.0, 59.0, 99.0, 84.0, 112.0, 109.0, 86.0, 81.0, 80.0, 126.0, 75.0, 112.0, 109.0, 90.0, 95.0, 111.0, 88.0, 85.0, 105.0, 86.0, 90.0, 91.0, 86.0, 89.0, 119.0, 147.0, 104.0, 122.0, 125.0, 154.0, 146.0, 101.0, 147.0, 135.0, 47.0, 105.0, 97.0, 82.0, 91.0, 91.0, 129.0, 104.0, 126.0, 69.0, 106.0, 118.0, 98.0, 93.0, 89.0, 116.0, 103.0, 74.0, 69.0, 91.0, 77.0, 117.0, 99.0, 101.0, 98.0, 101.0, 104.0, 90.0, 75.0, 92.0, 24.0, 102.0, 96.0, 133.0, 85.0, 105.0, 104.0, 106.0, 78.0, 113.0, 95.0, 91.0, 75.0, 98.0, 85.0, 78.0, 86.0, 136.0, 104.0, 65.0, 91.0, 97.0, 24.0, 65.0, 123.0, 97.0, 104.0, 71.0, 94.0, 179.0, 38.0, 74.0, 89.0, 57.0, 82.0, 102.0, 80.0, 124.0, 78.0, 82.0, 105.0, 93.0, 77.0, 120.0, 81.0, 72.0, 26.0, 99.0, 100.0, 196.0, 90.0, 104.0, 92.0, 85.0, 94.0, 105.0, 96.0, 91.0, 110.0, 95.0, 141.0, 107.0, 110.0, 88.0, 66.0, 115.0, 87.0, 103.0, 96.0, 115.0, 96.0, 104.0, 101.0, 97.0, 92.0, 91.0, 103.0, 130.0, 106.0, 97.0, 89.0, 87.0, 81.0, 96.0], "xaxis": "x", "y": [5.8, 6.5, 5.7, 5.9, 0.0, 6.3, 5.8, 6.5, 5.9, 6.9, 6.1, 6.7, 6.1, 0.0, 4.1, 6.5, 4.2, 5.8, 6.1, 6.5, 6.8, 6.0, 5.5, 2.9, 0.0, 6.6, 6.4, 6.7, 6.2, 5.9, 6.7, 0.0, 6.3, 5.3, 0.0, 6.8, 6.3, 0.0, 6.5, 6.8, 0.0, 6.9, 6.8, 0.0, 6.7, 6.6, 0.0, 4.2, 0.0, 5.8, 5.9, 6.6, 6.5, 4.7, 6.5, 6.6, 6.5, 0.0, 0.0, 0.0, 4.7, 0.0, 6.7, 0.0, 4.0, 5.6, 6.0, 6.1, 6.7, 4.4, 6.8, 6.5, 0.0, 5.9, 6.4, 6.2, 5.5, 6.4, 5.1, 5.9, 6.1, 5.6, 5.6, 6.5, 5.9, 3.3, 6.1, 5.7, 6.7, 5.6, 5.9, 5.4, 6.0, 5.8, 6.6, 6.8, 0.0, 6.9, 6.6, 6.3, 6.9, 6.5, 6.0, 4.9, 5.4, 5.7, 6.3, 4.9, 6.1, 6.9, 6.0, 5.6, 6.6, 6.8, 5.6, 6.0, 6.4, 6.5, 6.6, 5.8, 0.0, 5.9, 3.9, 6.4, 3.7, 0.0, 4.2, 3.8, 6.4, 5.1, 5.6, 6.0, 6.1, 6.3, 6.0, 5.2, 6.2, 5.3, 6.1, 5.8, 5.5, 5.6, 0.0, 5.3, 5.1, 6.3, 5.0, 4.7, 5.0, 6.4, 4.8, 6.0, 5.6, 6.0, 6.6, 5.1, 0.0, 0.0, 6.1, 0.0, 5.8, 6.2, 6.9, 5.9, 5.2, 6.1, 5.0, 4.9, 0.0, 5.6, 5.5, 5.2, 5.8, 6.4, 6.6, 4.7, 5.2, 5.7, 5.4, 6.1, 4.8, 6.5, 6.5, 6.8, 5.0, 4.5, 5.7, 6.6, 6.6, 5.3, 4.7, 0.0, 0.0, 5.9, 3.4, 6.2, 5.2, 5.9, 0.0, 6.5, 5.8, 6.3, 6.6, 6.3, 5.3, 5.8, 6.6, 6.7, 6.8, 6.1, 6.3, 5.1, 5.6, 6.3, 6.5, 5.8, 5.5, 6.1, 6.1, 5.2, 6.3], "yaxis": "y"}],                        {"legend": {"title": {"text": "rating_standard"}, "tracegroupgap": 0}, "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Analysis of co-relation between rating and duration"}, "xaxis": {"anchor": "y", "domain": [0.0, 1.0], "title": {"text": "duration_in_min"}}, "yaxis": {"anchor": "x", "domain": [0.0, 1.0], "title": {"text": "rating_num"}}},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('95383646-a71b-44c2-b459-48d290ba93e4');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>



```python
#finding co-relation to see if the duration variable and rating variable are co-related
from scipy.stats import pearsonr 
  
# Convert dataframe into series 
list1 = movie_analysis_edited['duration_in_min'] 
list2 = movie_analysis_edited['rating_num'] 
  
# Apply the pearsonr() 
corr, _ = pearsonr(list1, list2) 
print('Pearsons correlation: %.3f' % corr)

correlation = list1.corr(list2)
correlation
```

    Pearsons correlation: 0.180





    0.18002051843301892



## Rating class popularity


```python
# n_data_filter.head(1)   #taking  a glance at the dataframe

#accessing specifc columns 
data_rating_class= n_data_filter.loc[:,['netflixid','rating','country']]
data_rating_class.head(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>rating</th>
      <th>country</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>81145628</td>
      <td>TV-PG</td>
      <td>United States, India, South Korea, China</td>
    </tr>
  </tbody>
</table>
</div>




```python
# lets see which type of rating movie or TV show the netflix has the most
rating_value_counts = data_rating_class.rating.value_counts()
rating_value_counts
```




    TV-MA       2027
    TV-14       1698
    TV-PG        701
    R            508
    PG-13        286
    NR           218
    PG           184
    TV-Y7        169
    TV-G         149
    TV-Y         143
    TV-Y7-FV      95
    G             37
    UR             7
    NC-17          2
    Name: rating, dtype: int64



aliceblue, antiquewhite, aqua, aquamarine, azure,
            beige, bisque, black, blanchedalmond, blue,
            blueviolet, brown, burlywood, cadetblue,
            chartreuse, chocolate, coral, cornflowerblue,
            cornsilk, crimson, cyan, darkblue, darkcyan,
            darkgoldenrod, darkgray, darkgrey, darkgreen,
            darkkhaki, darkmagenta, darkolivegreen, darkorange,
            darkorchid, darkred, darksalmon, darkseagreen,
            darkslateblue, darkslategray, darkslategrey,
            darkturquoise, darkviolet, deeppink, deepskyblue,
            dimgray, dimgrey, dodgerblue, firebrick,
            floralwhite, forestgreen, fuchsia, gainsboro,
            ghostwhite, gold, goldenrod, gray, grey, green,
            greenyellow, honeydew, hotpink, indianred, indigo,
            ivory, khaki, lavender, lavenderblush, lawngreen,
            lemonchiffon, lightblue, lightcoral, lightcyan,
            lightgoldenrodyellow, lightgray, lightgrey,
            lightgreen, lightpink, lightsalmon, lightseagreen,
            lightskyblue, lightslategray, lightslategrey,
            lightsteelblue, lightyellow, lime, limegreen,
            linen, magenta, maroon, mediumaquamarine,
            mediumblue, mediumorchid, mediumpurple,
            mediumseagreen, mediumslateblue, mediumspringgreen,
            mediumturquoise, mediumvioletred, midnightblue,
            mintcream, mistyrose, moccasin, navajowhite, navy,
            oldlace, olive, olivedrab, orange, orangered,
            orchid, palegoldenrod, palegreen, paleturquoise,
            palevioletred, papayawhip, peachpuff, peru, pink,
            plum, powderblue, purple, red, rosybrown,
            royalblue, rebeccapurple, saddlebrown, salmon,
            sandybrown, seagreen, seashell, sienna, silver,
            skyblue, slateblue, slategray, slategrey, snow,
            springgreen, steelblue, tan, teal, thistle, tomato,
            turquoise, violet, wheat, white, whitesmoke,
            yellow, yellowgreen


```python
#setting colors
color = ['salmon', 'firebrick', 'aqua', 'mediumorchid', 'orangered',
           'limegreen', 'gold', 'tomato', 'magenta', 'blue',
            'blueviolet', 'brown', 'burlywood', 'cadetblue',
            'chartreuse']
#using bar plotly
data = [go.Bar(x=['TV-MA','TV-14','TV-PG','R','PG-13','NR','PG','TV-Y7','TV-G','TV-Y','TV-Y7-F7','G','UR','NC-17'],

#setting y to be value count of each rating type
y=[data_rating_class.loc[data_rating_class['rating']=='TV-MA'].shape[0],  
   data_rating_class.loc[data_rating_class['rating']=='TV-14'].shape[0],
   data_rating_class.loc[data_rating_class['rating']=='TV-PG'].shape[0],
    data_rating_class.loc[data_rating_class['rating']=='R'].shape[0],
    data_rating_class.loc[data_rating_class['rating']=='PG-13'].shape[0],
    data_rating_class.loc[data_rating_class['rating']=='NR'].shape[0],
    data_rating_class.loc[data_rating_class['rating']=='PG'].shape[0],
               data_rating_class.loc[data_rating_class['rating']=='TV-Y7'].shape[0],
               data_rating_class.loc[data_rating_class['rating']=='TV-G'].shape[0],
               data_rating_class.loc[data_rating_class['rating']=='TV-Y'].shape[0],
               data_rating_class.loc[data_rating_class['rating']=='TV-Y7-F7'].shape[0],
               data_rating_class.loc[data_rating_class['rating']=='G'].shape[0],
               data_rating_class.loc[data_rating_class['rating']=='UR'].shape[0],
               data_rating_class.loc[data_rating_class['rating']=='NC-17'].shape[0]],
   marker=dict(color=color) 
    
)]
#create the layout of the chart by defining titles for chart, x-axis and y-axis
layout = go.Layout(title='Netflix content rating analysis',
            xaxis=dict(title='Type of ratings'),
            yaxis=dict(title='Total no. of ratings'),
            height =500,
            width = 700)

#embedding data and layout into charts figure using Figure function
fig = go.Figure(data=data, layout=layout)
#Use plot function of plotly to visualize the data
fig.show()
```


<div>                            <div id="06613e7e-cfb5-4df6-af7c-816a55ffe6e8" class="plotly-graph-div" style="height:500px; width:700px;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("06613e7e-cfb5-4df6-af7c-816a55ffe6e8")) {                    Plotly.newPlot(                        "06613e7e-cfb5-4df6-af7c-816a55ffe6e8",                        [{"marker": {"color": ["salmon", "firebrick", "aqua", "mediumorchid", "orangered", "limegreen", "gold", "tomato", "magenta", "blue", "blueviolet", "brown", "burlywood", "cadetblue", "chartreuse"]}, "type": "bar", "x": ["TV-MA", "TV-14", "TV-PG", "R", "PG-13", "NR", "PG", "TV-Y7", "TV-G", "TV-Y", "TV-Y7-F7", "G", "UR", "NC-17"], "y": [2027, 1698, 701, 508, 286, 218, 184, 169, 149, 143, 0, 37, 7, 2]}],                        {"height": 500, "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Netflix content rating analysis"}, "width": 700, "xaxis": {"title": {"text": "Type of ratings"}}, "yaxis": {"title": {"text": "Total no. of ratings"}}},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('06613e7e-cfb5-4df6-af7c-816a55ffe6e8');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>



```python
rating_analysis_expand.head(2)  #printing two rows of data frame to see what the data frame looks like
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>type</th>
      <th>title</th>
      <th>country</th>
      <th>rating</th>
      <th>duration</th>
      <th>listed_in</th>
      <th>description</th>
      <th>rating_num</th>
      <th>rating_standard</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>70234439</td>
      <td>TV Show</td>
      <td>Transformers Prime</td>
      <td>United States</td>
      <td>TV-Y7-FV</td>
      <td>1 Season</td>
      <td>Kids' TV</td>
      <td>With the help of three human allies, the Autob...</td>
      <td>7.8</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80045922</td>
      <td>Movie</td>
      <td>6 Years</td>
      <td>United States</td>
      <td>NR</td>
      <td>80 min</td>
      <td>Dramas, Independent Movies, Romantic Movies</td>
      <td>As a volatile young couple who have been toget...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
  </tbody>
</table>
</div>




```python
#making a copy of dataframe
rating_analysis_by_country = rating_analysis_expand.copy()

#filling empty values with not available for ease of analysis
rating_analysis_by_country=rating_analysis_by_country.fillna('N/A')

#checking if the dataframe now has null values
rating_analysis_by_country.isnull().sum()
```




    netflixid          0
    type               0
    title              0
    country            0
    rating             0
    duration           0
    listed_in          0
    description        0
    rating_num         0
    rating_standard    0
    dtype: int64




```python
#plotting sunbrust plotly to see the type of rating type by the country
fig = px.sunburst(rating_analysis_by_country, path=['country', 'rating'],  color='country',
                  title='Analysis of Netflix ratings by country', height = 650, width =900)
fig.show()
```


<div>                            <div id="2adb1b1a-be2d-42bf-ba19-96ed6a35dbcb" class="plotly-graph-div" style="height:650px; width:900px;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("2adb1b1a-be2d-42bf-ba19-96ed6a35dbcb")) {                    Plotly.newPlot(                        "2adb1b1a-be2d-42bf-ba19-96ed6a35dbcb",                        [{"branchvalues": "total", "customdata": [["Mexico"], ["Singapore"], ["France"], ["Ecuador"], ["Denmark"], ["Netherlands"], ["India"], ["Japan"], ["United Kingdom"], ["Germany"], ["Ireland"], ["Italy"], ["Germany"], ["Mexico"], ["Japan"], ["Hungary"], ["Spain"], ["United States"], ["France"], ["France"], ["Ireland"], ["Canada"], ["Japan"], ["United States"], ["nan"], ["United States"], ["United Kingdom"], ["Israel"], ["France"], ["Norway"], ["Pakistan"], ["Taiwan"], ["Spain"], ["Poland"], ["Germany"], ["Italy"], ["Sweden"], ["United States"], ["Colombia"], ["Sweden"], ["Netherlands"], ["China"], ["Hong Kong"], ["Egypt"], ["nan"], ["Denmark"], ["United States"], ["Egypt"], ["Colombia"], ["Spain"], ["Netherlands"], ["Brazil"], ["United States"], ["cezhrepublic"], ["gr"], ["Ukraine"], ["France"], ["Germany"], ["Ireland"], ["Hong Kong"], ["Canada"], ["Singapore"], ["United States"], [""], ["United Arab Emirates"], ["South Africa"], ["New Zealand"], ["Australia"], ["United Kingdom"], ["Australia"], ["nan"], ["is"], ["United States"], ["United Arab Emirates"], ["Spain"], ["United Kingdom"], ["Japan"], ["Israel"], ["nan"], ["Mexico"], ["Australia"], ["Hong Kong"], ["Spain"], ["Russia"], ["Canada"], ["nan"], ["United States"], ["Bermuda"], ["United Kingdom"], ["Argentina"], ["Denmark"], ["Philippines"], ["Poland"], ["Russia"], ["Singapore"], ["South Korea"], ["Taiwan"], ["Turkey"], ["Ukraine"], ["United Arab Emirates"], ["United Kingdom"], ["United States"], ["ca"], ["cezhrepublic"], ["gr"], ["is"], ["nan"], ["pt"], ["New Zealand"], ["Netherlands"], ["Netherland"], ["Japan"], ["Japan"], ["New Zealand"], ["Brazil"], ["France"], ["Argentina"], ["Australia"], ["Bermuda"], ["Brazil"], ["Germany"], ["Bulgaria"], ["China"], ["Ecuador"], ["France"], ["Hong Kong"], ["Hongkong"], ["Hungary"], ["India"], ["Italy"], ["Canada"], ["Belgium"], ["Hungary"], ["United Kingdom"], ["Canada"], ["China"], ["France"], ["Hong Kong"], ["Mexico"], ["Netherlands"], ["Spain"], ["United States"], ["Brazil"], ["Australia"], ["United Kingdom"], ["United States"], ["Australia"], ["Canada"], ["Germany"], ["New Zealand"], ["South Africa"], ["Bulgaria"], ["Brazil"], ["Canada"], ["Australia"], ["th"], ["Australia"], ["Belgium"], ["Brazil"], ["France"], ["Germany"], ["Hongkong"], ["India"], ["Italy"], ["Argentina"], ["Luthvania"], ["Netherland"], ["Russia"], ["Singapore"], ["South Korea"], ["United Kingdom"], ["ca"], ["pt"], ["sk"], ["Mexico"], ["Argentina"], ["th"], ["Belgium"], ["Canada"], ["France"], ["Australia"], ["Ireland"], ["Russia"], [""], ["Singapore"], ["Argentina"], ["Australia"], ["Belgium"], ["Brazil"], ["Canada"], ["China"], ["sk"], ["India"], ["New Zealand"], ["Norway"], ["nan"], ["Philippines"], ["South Korea"], ["Turkey"], ["Canada"], ["United Kingdom"], ["China"], ["Colombia"], ["France"], ["Germany"], ["Hong Kong"], ["India"], ["Ireland"], ["Italy"], ["Japan"], ["Mexico"], ["Netherlands"], ["Pakistan"], ["Philippines"], ["Taiwan"], ["Sweden"], ["Qatar"], ["India"], ["Belgium"], ["Denmark"], ["Luthvania"], ["Germany"], ["South Korea"], ["Canada"], ["Qatar"], ["United States"]], "domain": {"x": [0.0, 1.0], "y": [0.0, 1.0]}, "hovertemplate": "labels=%{label}<br>count=%{value}<br>parent=%{parent}<br>id=%{id}<br>country=%{customdata[0]}<extra></extra>", "ids": ["Mexico", "Singapore/R", "France/TV-Y7-FV", "Ecuador/TV-Y7", "Denmark", "Netherlands/TV-Y7-FV", "India/TV-G", "Japan/N/A", "United Kingdom/R", "Germany/TV-Y", "Ireland/TV-Y", "Italy/TV-Y", "Germany", "Mexico/R", "Japan/TV-Y", "Hungary/N/A", "Spain/TV-MA", "United States/TV-14", "France/TV-Y7", "France/TV-Y", "Ireland/TV-MA", "Canada/TV-Y7-FV", "Japan/TV-Y7", "United States/TV-G", "nan/TV-G", "United States/R", "United Kingdom/NR", "Israel", "France/TV-PG", "Norway", "Pakistan", "Taiwan/TV-14", "Spain/TV-14", "Poland/TV-14", "Germany/R", "Italy/TV-MA", "Sweden", "United States/PG-13", "Colombia", "Sweden/N/A", "Netherlands/TV-MA", "China/R", "Hong Kong/TV-MA", "Egypt/TV-MA", "nan/TV-MA", "Denmark/TV-MA", "United States/N/A", "Egypt", "Colombia/TV-MA", "Spain", "Netherlands/TV-Y", "Brazil/TV-14", "United States/TV-Y7", "cezhrepublic/N/A", "gr/N/A", "Ukraine/NR", "France/TV-MA", "Germany/TV-PG", "Ireland", "Hong Kong/R", "Canada/TV-Y7", "Singapore/TV-Y7-FV", "United States/TV-Y7-FV", "", "United Arab Emirates/TV-14", "South Africa", "New Zealand/PG", "Australia/TV-PG", "United Kingdom/TV-14", "Australia/TV-G", "nan/N/A", "is/N/A", "United States/TV-PG", "United Arab Emirates/TV-PG", "Spain/TV-PG", "United Kingdom/TV-PG", "Japan/TV-PG", "Israel/TV-PG", "nan/TV-PG", "Mexico/TV-MA", "Australia/TV-Y7", "Hong Kong/TV-PG", "Spain/TV-Y", "Russia/TV-Y", "Canada/TV-Y", "nan/TV-Y", "United States/TV-Y", "Bermuda/TV-Y7", "United Kingdom/TV-Y", "Argentina/N/A", "Denmark/TV-Y7-FV", "Philippines", "Poland", "Russia", "Singapore", "South Korea", "Taiwan", "Turkey", "Ukraine", "United Arab Emirates", "United Kingdom", "United States", "ca", "cezhrepublic", "gr", "is", "nan", "pt", "New Zealand", "Netherlands", "Netherland", "Japan", "Japan/TV-Y7-FV", "New Zealand/TV-Y7-FV", "Brazil/UR", "France/UR", "Argentina", "Australia", "Bermuda", "Brazil", "Germany/TV-Y7", "Bulgaria", "China", "Ecuador", "France", "Hong Kong", "Hongkong", "Hungary", "India", "Italy", "Canada", "Belgium", "Hungary/TV-MA", "United Kingdom/PG-13", "Canada/NR", "China/NR", "France/NR", "Hong Kong/NR", "Mexico/NR", "Netherlands/NR", "Spain/NR", "United States/NR", "Brazil/NR", "Australia/PG", "United Kingdom/PG", "United States/PG", "Australia/PG-13", "Canada/PG-13", "Germany/PG-13", "New Zealand/PG-13", "South Africa/PG-13", "Bulgaria/R", "Brazil/PG", "Canada/R", "Australia/NR", "th/N/A", "Australia/N/A", "Belgium/N/A", "Brazil/N/A", "France/N/A", "Germany/N/A", "Hongkong/N/A", "India/N/A", "Italy/N/A", "Argentina/NR", "Luthvania/N/A", "Netherland/N/A", "Russia/N/A", "Singapore/N/A", "South Korea/N/A", "United Kingdom/N/A", "ca/N/A", "pt/N/A", "sk/N/A", "Mexico/N/A", "Argentina/TV-14", "th", "Belgium/TV-14", "Canada/TV-G", "France/TV-G", "Australia/TV-14", "Ireland/TV-G", "Russia/TV-G", "/TV-MA", "Singapore/TV-MA", "Argentina/TV-MA", "Australia/TV-MA", "Belgium/TV-MA", "Brazil/TV-MA", "Canada/TV-MA", "China/TV-MA", "sk", "India/TV-MA", "New Zealand/TV-MA", "Norway/TV-MA", "nan/TV-14", "Philippines/TV-MA", "South Korea/TV-MA", "Turkey/TV-14", "Canada/TV-14", "United Kingdom/TV-MA", "China/TV-14", "Colombia/TV-14", "France/TV-14", "Germany/TV-14", "Hong Kong/TV-14", "India/TV-14", "Ireland/TV-14", "Italy/TV-14", "Japan/TV-14", "Mexico/TV-14", "Netherlands/TV-14", "Pakistan/TV-14", "Philippines/TV-14", "Taiwan/TV-MA", "Sweden/TV-MA", "Qatar/TV-MA", "India/TV-PG", "Belgium/NR", "Denmark/NR", "Luthvania", "Germany/NR", "South Korea/TV-14", "Canada/TV-PG", "Qatar", "United States/TV-MA"], "labels": ["Mexico", "R", "TV-Y7-FV", "TV-Y7", "Denmark", "TV-Y7-FV", "TV-G", "N/A", "R", "TV-Y", "TV-Y", "TV-Y", "Germany", "R", "TV-Y", "N/A", "TV-MA", "TV-14", "TV-Y7", "TV-Y", "TV-MA", "TV-Y7-FV", "TV-Y7", "TV-G", "TV-G", "R", "NR", "Israel", "TV-PG", "Norway", "Pakistan", "TV-14", "TV-14", "TV-14", "R", "TV-MA", "Sweden", "PG-13", "Colombia", "N/A", "TV-MA", "R", "TV-MA", "TV-MA", "TV-MA", "TV-MA", "N/A", "Egypt", "TV-MA", "Spain", "TV-Y", "TV-14", "TV-Y7", "N/A", "N/A", "NR", "TV-MA", "TV-PG", "Ireland", "R", "TV-Y7", "TV-Y7-FV", "TV-Y7-FV", "", "TV-14", "South Africa", "PG", "TV-PG", "TV-14", "TV-G", "N/A", "N/A", "TV-PG", "TV-PG", "TV-PG", "TV-PG", "TV-PG", "TV-PG", "TV-PG", "TV-MA", "TV-Y7", "TV-PG", "TV-Y", "TV-Y", "TV-Y", "TV-Y", "TV-Y", "TV-Y7", "TV-Y", "N/A", "TV-Y7-FV", "Philippines", "Poland", "Russia", "Singapore", "South Korea", "Taiwan", "Turkey", "Ukraine", "United Arab Emirates", "United Kingdom", "United States", "ca", "cezhrepublic", "gr", "is", "nan", "pt", "New Zealand", "Netherlands", "Netherland", "Japan", "TV-Y7-FV", "TV-Y7-FV", "UR", "UR", "Argentina", "Australia", "Bermuda", "Brazil", "TV-Y7", "Bulgaria", "China", "Ecuador", "France", "Hong Kong", "Hongkong", "Hungary", "India", "Italy", "Canada", "Belgium", "TV-MA", "PG-13", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "PG", "PG", "PG", "PG-13", "PG-13", "PG-13", "PG-13", "PG-13", "R", "PG", "R", "NR", "N/A", "N/A", "N/A", "N/A", "N/A", "N/A", "N/A", "N/A", "N/A", "NR", "N/A", "N/A", "N/A", "N/A", "N/A", "N/A", "N/A", "N/A", "N/A", "N/A", "TV-14", "th", "TV-14", "TV-G", "TV-G", "TV-14", "TV-G", "TV-G", "TV-MA", "TV-MA", "TV-MA", "TV-MA", "TV-MA", "TV-MA", "TV-MA", "TV-MA", "sk", "TV-MA", "TV-MA", "TV-MA", "TV-14", "TV-MA", "TV-MA", "TV-14", "TV-14", "TV-MA", "TV-14", "TV-14", "TV-14", "TV-14", "TV-14", "TV-14", "TV-14", "TV-14", "TV-14", "TV-14", "TV-14", "TV-14", "TV-14", "TV-MA", "TV-MA", "TV-MA", "TV-PG", "NR", "NR", "Luthvania", "NR", "TV-14", "TV-PG", "Qatar", "TV-MA"], "marker": {"colors": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52", "#636efa", "#EF553B", "#FECB52", "#636efa", "#B6E880", "#00cc96", "#ab63fa", "#FFA15A", "#00cc96", "#00cc96", "#636efa", "#19d3f3", "#B6E880", "#FFA15A", "#FF6692", "#FFA15A", "#FF97FF", "#B6E880", "#00cc96", "#FF97FF", "#FECB52", "#636efa", "#ab63fa", "#EF553B", "#FECB52", "#EF553B", "#00cc96", "#FFA15A", "#ab63fa", "#00cc96", "#19d3f3", "#FFA15A", "#19d3f3", "#FF6692", "#FF6692", "#FFA15A", "#FFA15A", "#FF6692", "#ab63fa", "#ab63fa", "#19d3f3", "#B6E880", "#FFA15A", "#FF97FF", "#FECB52", "#636efa", "#00cc96", "#FECB52", "#636efa", "#19d3f3", "#19d3f3", "#EF553B", "#FFA15A", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF97FF", "#19d3f3", "#FF6692", "#FF6692", "#FFA15A", "#00cc96", "#ab63fa", "#FF97FF", "#B6E880", "#B6E880", "#FF6692", "#636efa", "#19d3f3", "#19d3f3", "#ab63fa", "#B6E880", "#19d3f3", "#FF6692", "#FFA15A", "#FF97FF", "#FF97FF", "#FECB52", "#FFA15A", "#636efa", "#EF553B", "#B6E880", "#EF553B", "#EF553B", "#636efa", "#00cc96", "#636efa", "#00cc96", "#FF97FF", "#FFA15A", "#ab63fa", "#FF97FF", "#FECB52", "#FF6692", "#FF6692", "#FFA15A", "#FFA15A", "#19d3f3", "#19d3f3", "#B6E880", "#B6E880", "#FFA15A", "#B6E880", "#00cc96", "#FECB52", "#19d3f3", "#FF97FF", "#B6E880", "#FECB52", "#FF6692", "#FFA15A", "#ab63fa", "#00cc96", "#19d3f3", "#B6E880", "#00cc96", "#FF6692", "#EF553B", "#19d3f3", "#FF97FF", "#00cc96", "#FF97FF", "#19d3f3", "#FFA15A", "#00cc96", "#19d3f3", "#636efa", "#19d3f3", "#ab63fa", "#FFA15A", "#B6E880", "#19d3f3", "#FF97FF", "#FFA15A", "#19d3f3", "#19d3f3", "#FECB52", "#FFA15A", "#ab63fa", "#FF6692", "#B6E880", "#19d3f3", "#19d3f3", "#FECB52", "#19d3f3", "#FF97FF", "#B6E880", "#00cc96", "#FECB52", "#B6E880", "#FF6692", "#EF553B", "#FECB52", "#636efa", "#19d3f3", "#B6E880", "#EF553B", "#EF553B", "#FF97FF", "#ab63fa", "#FFA15A", "#EF553B", "#636efa", "#FECB52", "#FECB52", "#FF97FF", "#19d3f3", "#00cc96", "#19d3f3", "#636efa", "#B6E880", "#EF553B", "#EF553B", "#FECB52", "#19d3f3", "#FF97FF", "#B6E880", "#19d3f3", "#FFA15A", "#EF553B", "#FF6692", "#FFA15A", "#FF97FF", "#FF6692", "#636efa", "#EF553B", "#00cc96", "#19d3f3", "#FF97FF", "#FFA15A", "#ab63fa", "#00cc96", "#FECB52", "#19d3f3", "#FF6692", "#636efa", "#EF553B", "#B6E880", "#636efa", "#19d3f3", "#FECB52", "#636efa", "#636efa", "#00cc96", "#00cc96", "#FF6692", "#FF97FF", "#FFA15A", "#636efa", "#FECB52", "#EF553B", "#19d3f3", "#00cc96", "#FFA15A"]}, "name": "", "parents": ["", "Singapore", "France", "Ecuador", "", "Netherlands", "India", "Japan", "United Kingdom", "Germany", "Ireland", "Italy", "", "Mexico", "Japan", "Hungary", "Spain", "United States", "France", "France", "Ireland", "Canada", "Japan", "United States", "nan", "United States", "United Kingdom", "", "France", "", "", "Taiwan", "Spain", "Poland", "Germany", "Italy", "", "United States", "", "Sweden", "Netherlands", "China", "Hong Kong", "Egypt", "nan", "Denmark", "United States", "", "Colombia", "", "Netherlands", "Brazil", "United States", "cezhrepublic", "gr", "Ukraine", "France", "Germany", "", "Hong Kong", "Canada", "Singapore", "United States", "", "United Arab Emirates", "", "New Zealand", "Australia", "United Kingdom", "Australia", "nan", "is", "United States", "United Arab Emirates", "Spain", "United Kingdom", "Japan", "Israel", "nan", "Mexico", "Australia", "Hong Kong", "Spain", "Russia", "Canada", "nan", "United States", "Bermuda", "United Kingdom", "Argentina", "Denmark", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "", "Japan", "New Zealand", "Brazil", "France", "", "", "", "", "Germany", "", "", "", "", "", "", "", "", "", "", "", "Hungary", "United Kingdom", "Canada", "China", "France", "Hong Kong", "Mexico", "Netherlands", "Spain", "United States", "Brazil", "Australia", "United Kingdom", "United States", "Australia", "Canada", "Germany", "New Zealand", "South Africa", "Bulgaria", "Brazil", "Canada", "Australia", "th", "Australia", "Belgium", "Brazil", "France", "Germany", "Hongkong", "India", "Italy", "Argentina", "Luthvania", "Netherland", "Russia", "Singapore", "South Korea", "United Kingdom", "ca", "pt", "sk", "Mexico", "Argentina", "", "Belgium", "Canada", "France", "Australia", "Ireland", "Russia", "", "Singapore", "Argentina", "Australia", "Belgium", "Brazil", "Canada", "China", "", "India", "New Zealand", "Norway", "nan", "Philippines", "South Korea", "Turkey", "Canada", "United Kingdom", "China", "Colombia", "France", "Germany", "Hong Kong", "India", "Ireland", "Italy", "Japan", "Mexico", "Netherlands", "Pakistan", "Philippines", "Taiwan", "Sweden", "Qatar", "India", "Belgium", "Denmark", "", "Germany", "South Korea", "Canada", "", "United States"], "type": "sunburst", "values": [13, 1, 9, 1, 3, 1, 1, 35, 2, 1, 1, 1, 23, 1, 1, 13, 4, 56, 1, 2, 1, 3, 2, 7, 1, 20, 2, 1, 1, 1, 1, 4, 4, 1, 2, 3, 18, 16, 3, 17, 1, 2, 2, 1, 8, 1, 5, 1, 2, 11, 1, 2, 12, 23, 1, 1, 5, 1, 4, 2, 7, 1, 36, 1, 1, 1, 1, 2, 11, 1, 2, 1, 31, 1, 1, 3, 2, 1, 3, 6, 1, 2, 1, 1, 7, 1, 11, 1, 3, 16, 1, 3, 1, 10, 5, 7, 5, 7, 1, 2, 65, 327, 3, 23, 1, 1, 17, 1, 7, 6, 8, 58, 10, 3, 1, 1, 20, 18, 1, 10, 1, 1, 7, 1, 26, 10, 33, 14, 25, 13, 49, 13, 1, 4, 5, 1, 1, 2, 2, 2, 1, 24, 1, 2, 3, 7, 3, 1, 3, 2, 1, 1, 1, 2, 1, 3, 4, 10, 2, 1, 12, 33, 2, 7, 1, 2, 8, 8, 1, 3, 21, 3, 1, 2, 3, 2, 3, 1, 4, 2, 2, 1, 1, 1, 2, 1, 2, 1, 3, 6, 2, 2, 12, 1, 1, 2, 1, 3, 7, 10, 16, 2, 1, 3, 1, 2, 6, 1, 2, 8, 1, 1, 1, 2, 1, 1, 1, 4, 1, 1, 2, 2, 1, 4, 1, 102]}],                        {"height": 650, "legend": {"tracegroupgap": 0}, "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Analysis of Netflix ratings by country"}, "width": 900},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('2adb1b1a-be2d-42bf-ba19-96ed6a35dbcb');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>


#### now that we have analyzed the rating type, since we also have data of title, cast, directors lets analyze these pieces of incormation and see if we can come up with some insights

## High-rated titles


```python
# coming up with some popular words among all titles for high-rated movie/shows
country_high_rating.head(1)
#country_high_rating[country_high_rating.duplicated(['netflixid'])]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>type</th>
      <th>title</th>
      <th>country</th>
      <th>rating</th>
      <th>duration</th>
      <th>listed_in</th>
      <th>description</th>
      <th>rating_num</th>
      <th>rating_standard</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>70234439</td>
      <td>TV Show</td>
      <td>Transformers Prime</td>
      <td>United States</td>
      <td>TV-Y7-FV</td>
      <td>1 Season</td>
      <td>Kids' TV</td>
      <td>With the help of three human allies, the Autob...</td>
      <td>7.8</td>
      <td>High-rated</td>
    </tr>
  </tbody>
</table>
</div>




```python

#opening image in numpy array format to shape word cloud in this saved image
#to do that we need to check the intensity of pixels, which acn be done by opening image in numpy format
TV_mask = np.array(Image.open("TV.jpg")) 
#TV_mask
```


```python
#mask has to be in 255 pixels to use it in word cloud 
# our mask is in correct form so, let's create text for wordcloud
text = " ".join(country_high_rating['title'])

#creating a word cloud image
wc = WordCloud(background_color='black',max_words =500, mask = TV_mask, 
               contour_width =3, contour_color = 'red')

#generate a wordcloud
wc.generate(text)

#show
plt.figure(figsize=[20,10])
plt.title("Wordcloud for popoular words in titles", fontsize =30)
plt.imshow(wc)
plt.axis('off')
plt.show()
```


![png](output_45_0.png)


## High-rated directors


```python
# Similarly some popular directors from high rated movies/shows

#accessing specific columns
rated_directorANDactor = copy_count_rated.loc[:,['director','cast','rating_standard','title']]

#accessing specific rows
high_rated_directorANDactor = rated_directorANDactor.loc[rated_directorANDactor.rating_standard == 'High-rated']

#dropping nan values
high_rated_director = high_rated_directorANDactor.director.dropna()
#high_rated_director
```


```python
# our mask is in correct form so, let's create text for wordcloud
text = " ".join(high_rated_director)

#creating a word cloud image with maximum words of 200 
wc = WordCloud(background_color='black',max_words =200, mask = TV_mask, 
               contour_width =3, contour_color = 'red')

#generate a wordcloud
wc.generate(text)

#show
plt.figure(figsize=[25,8])
plt.title("Popular directors", fontsize =25)
plt.imshow(wc)
plt.axis('off')
plt.show()
```


![png](output_48_0.png)

Most common 4 director names with High rated movies are:
    1. Shannon Hartman
    2. Jay Karas
    3. Lilly Wachowski, Lana Wachowski
    4. Mike Clattenburg
   

```python
#having some information related with director Shannon Hartman
high_rated_directorANDactor[high_rated_directorANDactor['director'].str.match('^Shannon Hartman*')== True][:2]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>director</th>
      <th>cast</th>
      <th>rating_standard</th>
      <th>title</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>60</th>
      <td>Shannon Hartman</td>
      <td>Kevin Hart</td>
      <td>High-rated</td>
      <td>Kevin Hart: Seriously Funny</td>
    </tr>
    <tr>
      <th>78</th>
      <td>Shannon Hartman, Michelle Caputo</td>
      <td>Donald Glover</td>
      <td>High-rated</td>
      <td>Donald Glover: Weirdo</td>
    </tr>
  </tbody>
</table>
</div>



## most probably do not use the visualization for description wordcloud so its in nbc convert
# our mask is in correct form so, let's create text for wordcloud
text = " ".join(country_high_rating['description'])

#creating a word cloud image
wc = WordCloud(background_color='black',max_words =1000, mask = TV_mask, 
               contour_width =3, contour_color = 'red')

#generate a wordcloud
wc.generate(text)

#show
plt.figure(figsize=[20,10])
plt.imshow(wc)
plt.axis('off')
plt.show()rated_directorANDactor

```python

```

###  Pattern for content description

I would also like to analyze if there is any specific pattern in description of movie/show. Can we tell which genre will that movie/show belong by looking at the descritption? If yes, are there any commonalities we can find in that gerne's?

## genre nlp try


```python
rating_analysis_genre
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>type</th>
      <th>title</th>
      <th>country</th>
      <th>rating</th>
      <th>duration</th>
      <th>listed_in</th>
      <th>description</th>
      <th>rating_num</th>
      <th>rating_standard</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>70234439</td>
      <td>TV Show</td>
      <td>Transformers Prime</td>
      <td>United States</td>
      <td>TV-Y7-FV</td>
      <td>1 Season</td>
      <td>Kid's and Teen</td>
      <td>With the help of three human allies, the Autob...</td>
      <td>7.8</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80182115</td>
      <td>Movie</td>
      <td>Long Shot</td>
      <td>United States</td>
      <td>TV-14</td>
      <td>40 min</td>
      <td>Documentaries</td>
      <td>When Juan Catalan is arrested for a murder he ...</td>
      <td>7.4</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>2</th>
      <td>81001809</td>
      <td>Movie</td>
      <td>Lessons from a School Shooting: Notes from Dun...</td>
      <td>United States</td>
      <td>TV-PG</td>
      <td>24 min</td>
      <td>Documentaries</td>
      <td>Two priests – one from Dunblane, Scotland, the...</td>
      <td>5.8</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>3</th>
      <td>80005444</td>
      <td>Movie</td>
      <td>Print the Legend</td>
      <td>United States</td>
      <td>TV-14</td>
      <td>100 min</td>
      <td>Documentaries</td>
      <td>This award-winning, original documentary chron...</td>
      <td>7.1</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>4</th>
      <td>80097321</td>
      <td>Movie</td>
      <td>Audrie &amp; Daisy</td>
      <td>United States</td>
      <td>TV-14</td>
      <td>99 min</td>
      <td>Documentaries</td>
      <td>In this wrenching documentary, two teens are s...</td>
      <td>7.2</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1439</th>
      <td>70184127</td>
      <td>TV Show</td>
      <td>Big Bad Beetleborgs</td>
      <td>Japan</td>
      <td>TV-Y7-FV</td>
      <td>2 Seasons</td>
      <td>Comedies</td>
      <td>When three teens free a spirit that offers to ...</td>
      <td>6.3</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>1440</th>
      <td>70180088</td>
      <td>TV Show</td>
      <td>The Garfield Show</td>
      <td>France</td>
      <td>TV-Y7</td>
      <td>3 Seasons</td>
      <td>Kid's and Teen</td>
      <td>Lazy, lasagna-loving fat cat Garfield lives li...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>1441</th>
      <td>70180088</td>
      <td>TV Show</td>
      <td>The Garfield Show</td>
      <td>France</td>
      <td>TV-Y7</td>
      <td>3 Seasons</td>
      <td>Comedies</td>
      <td>Lazy, lasagna-loving fat cat Garfield lives li...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>1442</th>
      <td>70180088</td>
      <td>TV Show</td>
      <td>The Garfield Show</td>
      <td>United States</td>
      <td>TV-Y7</td>
      <td>3 Seasons</td>
      <td>Kid's and Teen</td>
      <td>Lazy, lasagna-loving fat cat Garfield lives li...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
    <tr>
      <th>1443</th>
      <td>70180088</td>
      <td>TV Show</td>
      <td>The Garfield Show</td>
      <td>United States</td>
      <td>TV-Y7</td>
      <td>3 Seasons</td>
      <td>Comedies</td>
      <td>Lazy, lasagna-loving fat cat Garfield lives li...</td>
      <td>5.6</td>
      <td>Low-rated</td>
    </tr>
  </tbody>
</table>
<p>1444 rows × 10 columns</p>
</div>




```python
#getting speciifc columns needed for analysis
rating_analysis_genre_edit =rating_analysis_genre.loc[:,['netflixid','listed_in','description','rating_standard']]

#looking for duplicates and keeping the first records if there are any duplicates
analysis_genre = rating_analysis_genre_edit.drop_duplicates(subset='netflixid',keep= 'first')
#print(analysis_genre.shape) #will print the shape of data frame
#analysis_genre

#analysis_genre.listed_in.to_list()    prints out the list of genres
```


```python
#setting listed_in column as index
genre_pattern = analysis_genre.set_index('listed_in')

#getting popular genre descriptions like comedies, Action and adventures, Horror movies and Romantic
comedies_pattern = genre_pattern.loc[['Comedies']]
Action_Adventures_pattern =  genre_pattern.loc[['Action & Adventure']]
Horror_pattern = genre_pattern.loc[['Horror Movies']]
Romantic_pattern = genre_pattern.loc[['Romantic']]
```


```python
# defining a function to get popular words from thd description of that specific genre 
#nltk.download('stopwords')
from nltk.corpus import stopwords

def get_pattern(x):
    text = " ".join(x['description'])  #joining all the values of Description COLUMN as a text
    
    # using word_tokenize() for splitting strings into tokens (nominally words). 
    #It splits tokens based on white space and punctuation. For example, commas and periods are taken as separate tokens.
    textwords = word_tokenize(text)       
    
    #setting stopwords 
    stop_words = set(stopwords.words("english"))
    stop_words.update(['series','finds'])  #updating stopwords because as these words might not have specifc meaning
    exclud_punc=[]  #making a new list
    finl_words=[]  #making a new list
    for w in textwords:        #using a for loop in tokenized text
        if w.isalpha():        # checking whether a character is an alphabet or not
            exclud_punc.append(w.lower())    #making sure that all the strings are lower case and appeding to the new list and 
    for word in exclud_punc:                 # using for loop in the appended list
        if word not in stop_words:          #checking if the words are contained in stop_words
            finl_words.append(word)         #appedning the filtered words, which are not in stop words

    return finl_words       #returning the appended list

```


```python
comedy_word_list = get_pattern(comedies_pattern)    #calling a function to get popular words for comedy genre
action_Adv_list = get_pattern(Action_Adventures_pattern) #calling a function to get popular words for action and adventure genre
horror_list =get_pattern(Horror_pattern)  #calling a function to get popular words for horror genre
romantic_list = get_pattern(Romantic_pattern) #calling a fucntion to get popular words for romantic genre
```
I don't need this

fdist_comedy= FreqDist(comedy_word_list)
fdist_act_Adv= FreqDist(action_Adv_list)
fdist_horror = FreqDist(horror_list)

print(fdist_horror.most_common(20))

```python
#w1 = WordCloud(max_font_size=50, max_words=150, colormap="Oranges_r").generate(horror_list_wc)
#wordcloud2 = WordCloud().generate(action_Adv_wc)

#making a list of the lists
list_words = [horror_list,action_Adv_list, comedy_word_list, romantic_list]

#making a list for the tile
title=['horror genre','action and adventure genre','comedy genre','romantic genre']
j =0   #setting the counter
for i in list_words:   #using for loop in the lists
    text = " ".join(i)   #joining all the words from the list and making it like whole bag of words  
    w1 = WordCloud(max_font_size=50, max_words=150, colormap="Oranges_r").generate(text)  #generating wordcloud
    plt.figure(figsize = (10, 8))
    plt.imshow(w1)
    plt.title(f"Popoular words for {title[j]}", fontsize=20)  #setting title
#plt.imshow(wordcloud2)
    plt.axis("off")
    plt.show() #plotting
    j= j+1  #increasing counter
```


![png](output_63_0.png)



![png](output_63_1.png)



![png](output_63_2.png)



![png](output_63_3.png)



```python

```


```python

```

## Pattern for sentiments of title

I have seen some people who are only tempted to see the movie which have positive sentiments. Like my aunt only watches the movie which gives her positive influence. She reads the description of movie and if the movie description has word like violence (negative vibes), she will ignore that. So lets analyze the sentiment of the description of title.


```python
#getting specific columns from the dataframe
copy_count_rated_country
synopsis_analysis = copy_count_rated_country.loc[:,['description', 'rating_num','rating_standard','rating']]
synopsis_analysis = synopsis_analysis.set_index(['description'])  #setting index
synopsis_analysis = synopsis_analysis.reset_index()  #resetting index
synopsis_analysis.head(2) 
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>description</th>
      <th>rating_num</th>
      <th>rating_standard</th>
      <th>rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>With the help of three human allies, the Autob...</td>
      <td>7.8</td>
      <td>High-rated</td>
      <td>TV-Y7-FV</td>
    </tr>
    <tr>
      <th>1</th>
      <td>As a volatile young couple who have been toget...</td>
      <td>5.6</td>
      <td>Low-rated</td>
      <td>NR</td>
    </tr>
  </tbody>
</table>
</div>




```python
#making a new list
value_list =[]  
sentiment_list=[]

#using for loop to iterate
for each in range(len(synopsis_analysis)):
    try:
        text = synopsis_analysis['description'][each]  #getting specific value of description column 
        analysis = TextBlob(text)   #using python library to process the textual data.
        value = analysis.sentiment.polarity  #analyzing the sentiment of text
        value_list.append(value)
        if value > 0:                  #setting the condition if the sentiment is greater than 0 to be positive
            sentiment = 'positive'
        elif value == 0:           #setting the condition if the sentiment is 0 to be neutral
            sentiment ='neutral'
        else:                        #setting the condition if the sentiment is lesser than 0 to be negative
            sentiment ='negative'
        sentiment_list.append(sentiment)  #appending sentiment values i.e. either positive, neutral or negative to the list
    except:
        continue

#print(value_list)  #prints the list
#print(len(sentiment_list))
```


```python
# making the list into the column of dataframe
synopsis_analysis['sentiment'] = sentiment_list

#dropping nan values of the dataframe
sentiment_analysis = synopsis_analysis.dropna()


# calculating counts of sentiment movies/show 
count_sentiments = sentiment_analysis.sentiment.value_counts()

```


```python
#making a function to calculate the percent of sentiment values(i.e. either positive/neutral/negative)
def get_sentiment_count(df):
    y_count = df.sentiment.value_counts().reset_index()  #counting the values and restting the index
    y_count =y_count.rename(columns={'index': "sentiment_value","sentiment":"counts"})  #renaming the columns
    total = sum(y_count['counts'])  #calcualting the sum 
    y_count['percent'] = y_count['counts'].apply(lambda x: (x/total)*100 )  #applying the percent function using lambda
    return y_count #returning the dataframe

high_count = get_sentiment_count(sentiment_analysis)

```


```python
#plotting the percentage of sentiment for high-rated movies
fig = go.Figure(data=[go.Pie(labels=high_count['sentiment_value'], values=high_count['percent'], hole=.3)])

fig.update_layout(
    title_text="Synopsis sentiment of high-rated movies",
    # Add annotations in the center of the donut pies.
    annotations=[dict(text='sentiments', x=0.50, y=0.5, font_size=14, showarrow=False)])

fig.show()

#this is good news for people like my aunt, as she prefers to watch the movie that has positive sentiments. 
```


<div>                            <div id="7d931206-c603-4299-9053-280695275c13" class="plotly-graph-div" style="height:525px; width:100%;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("7d931206-c603-4299-9053-280695275c13")) {                    Plotly.newPlot(                        "7d931206-c603-4299-9053-280695275c13",                        [{"hole": 0.3, "labels": ["positive", "negative", "neutral"], "type": "pie", "values": [52.95238095238095, 30.857142857142854, 16.19047619047619]}],                        {"annotations": [{"font": {"size": 14}, "showarrow": false, "text": "sentiments", "x": 0.5, "y": 0.5}], "template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Synopsis sentiment of high-rated movies"}},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('7d931206-c603-4299-9053-280695275c13');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>



```python
#GETTING sentiment data for high-rated
high_rated = sentiment_analysis[sentiment_analysis.rating_standard == 'High-rated']

#getting sentiment data for low-rated
low_rated = sentiment_analysis[sentiment_analysis.rating_standard == 'Low-rated']

#dataframe with high positive sentiments among high-rated movies
only_high_pos = high_rated[high_rated['sentiment'] == 'positive']

#dataframe with high negative sentiments among high-rated movies
only_high_neg = high_rated[high_rated['sentiment'] == 'negative']

```


```python
#finding popular words to look for high-rated movie/shows with positive sentiments
high_pos_words = get_pattern(only_high_pos)    #calling a previous function

#finding popular words to look for high-rated movie/shows with negative sentiments
high_neg_words = get_pattern(only_high_neg)#calling a previous function
```


```python
#plotting word cloud that shows the popoular words to look to find high-rated positive sentiment movie/show
text = " ".join(high_pos_words)  #joining all the the words

stopwords = set(STOPWORDS)  #setting stopwords
stopwords.update(["series",'show'])  #updating stopwords with series and show as these words might not be that significant
#creating a word cloud image
wc = WordCloud(stopwords =stopwords, background_color='white',max_words =1000)
#generate a wordcloud
wc.generate(text)

#show
plt.figure(figsize=[15,7])
plt.title("Positive words to find high-rated movies with positive-sentiment", fontsize = 30)

plt.imshow(wc)
plt.axis('off')
plt.show()
```


![png](output_74_0.png)


## Recommendation according to title, type, cast, director, listed_in 

#### Using countvectorizer and cosine similarity to provide some recommendations according to title, type, cast, director and genre.
Countvectorizer is used to transform a given text into a vector on the basis of the frequency (count) of each word that occurs in the entire text. And ‘cosine_similarity’ is used to find the similarity. Using cossine similarity means to calculate the cosine of the angle between two vectors. It does not mean finding straight line distance between two points 


```python
#getting specific columns from the dataframe
new_df_recommend = n_data_filter.loc[:,['type','title','director','cast','listed_in']]
new_df =new_df_recommend.copy()  #making a copy of the dataframe
new_df = new_df.fillna('') #filling na values 
#new_df
```


```python
#defining a function to clean data according to the need
def clean_data(x):
#Check if string exists. If not, return empty string
    if isinstance(x, str): 
        return str.lower(x.replace(" ", "")) #making string lowercase and replacing whitespace
    else:
        return ''
```


```python
# using for loop and calling the function to clean the data
columns = ['type','title','director','cast','listed_in']
for col in columns:
    new_df[col] = new_df[col].apply(clean_data)
```


```python
#defining function that comines all the columns together
def combine_cols(x):
    return ''.join(x['type']) + ' ' + ''.join(x['title']) + ' ' + x['director'] + ' ' + ''.join(x['cast'])+' ' + '' .join(x['listed_in'])

#applying the defined functions
new_df['combined_cols'] = new_df.apply(combine_cols , axis=1)
# new_df['combined_cols']
```


```python
#making another recommend function  using countvectorizer 
def recommend_func(x,user_title,new_df_recommend):
    
    #calling countvectorizer and using stop_words functionality to remove the unwanted words
    count_convert_vector = CountVectorizer(stop_words='english')
    
    #Convert a collection of text documents to a matrix of counts
    count_convert_vector_matrix = count_convert_vector.fit_transform(x['combined_cols'])

    # Compute the Cosine Similarity matrix based on the matrix of counts
    from sklearn.metrics.pairwise import cosine_similarity

    #calling a cosine_similarity function and passing the counts 
    similarity_metric = cosine_similarity(count_convert_vector_matrix, count_convert_vector_matrix)

    # Reset index of your main DataFrame and construct reverse mapping as before
    try:
        x = x.reset_index()
        index_col = pd.Series(x.index, index=x['title'])
    except:
        index_col = pd.Series(x.index, index=x['title'])
    
    
    ################      recommendations_title_by_genre(user_title, similarity_metric)
    user_title =user_title.replace(' ','').lower()

    # Get the index of the movie that matches the title
    index_val = index_col[user_title]
    
    print("The 5 shows related to your title are:\n")


    # Get the pairwsie similarity scores of all movies with that movie
    similarity_scores = enumerate(similarity_metric[index_val])


    # Sort the movies based on the similarity scores
    #using the sort function to filter the scores and arrange them in descending order
    similarity_scores = sorted(similarity_scores, key=lambda a: a[1], reverse=True)
    
    # Get the scores of the 5 most similar movies
    similarity_scores = similarity_scores[1:6]
    
    
   
    # Get the movie indices
    movie_index_val=[]
    #usig for loop to get the scores and appending it to new list 
    for similar in similarity_scores:
        value = similar[0]
        movie_index_val.append(value)
    

    # Return the top 5 most similar movies
    my_list = new_df_recommend['title'].iloc[movie_index_val]
    for my in my_list:  #using for loop to print one by one
        print(my)

```


```python
#defining another function to get the title that the user chose
def get_df_title_genre(new_df,user_genre, user_title):
    #replacing the whitespaces because our all the titles and other features are combined and removed whitespaces for processing
    user_genre = user_genre.replace(' ','').lower()
    #getting data frame with specific genre from listed_in columns
    x = new_df[new_df.listed_in == user_genre]
    
    #calling the function and passing the dataframe, title and genre to the function
    recommend_func(x,user_title,new_df_recommend)

def get_df_title(new_df,user_title): #defining the function that will get the title 
    x = new_df.copy()  #making the new dataframe
    recommend_func(x,user_title,new_df_recommend)#calling the function and passing the title name, data frame 
    
```


```python
def choose_genre(user_genre): #defining the function to let the user choose genre
    
    # getting the specific genre according to user choice
    movie_names =new_df_recommend[new_df_recommend['listed_in']== user_genre]
    print(user_genre) #printing the user genre choice
    name_list = movie_names['title'].to_list() #getting the title list of titles from the genre chose
    print(name_list[0:3]) #printing three title names based on the genre chose
```


```python
#defining the menu function 
def menu():
    while True:
        #getting the input from users
        inp = input("How would you like to get the recommendations? \n"
                        "      Enter 'T' if you would like to get recommendation just by title:\n"
                        "      Enter 'G' if you would like to get recommendation with genre and title:\n"
                        "      Enter 'N' for no recommendations and to quit:\n").upper()

        if inp == 'T': #setting the condition
            user_input=input("Enter the title name to get some recommendation: ")  #asking the input
            
            print(f"Your title is:{user_input} ") #printing the title or the input that the user entered
            print()  #leaving one line space
            print("The 5 shows related to your title are: \n") #print prompt
            get_df_title(new_df,user_input) #calling the function that passes the user title and dataframe

        elif inp =='G':  #setting another condition
            print("Genre options:\n"  #printing the prompt
                  "    (Enter) 'A'for 'Documentaries'\n"
                  "    (Enter) 'B' for 'Stand-Up Comedy'\n"
                  "    (Enter) 'C' for 'Dramas, Independent Movies, International Movies'\n"
                  '    (Enter) "D" for "Kids\' TV "\n'
                  "    (Enter) 'E' for 'Dramas, International Movies, Romantic Movies'\n"
                  "    (Enter) 'F' for 'Action & Adventure, Sci-Fi & Fantasy'\n"
                  "    (Enter) 'G' for 'Horror Movies, Thrillers'\n")
                 

            user_genre = input("Enter the letter for the genre you would like:\n ").upper() # prompt for user input
            list_options = ['A','B','C','D','E','F','G']  #setting the list with user options
            
            #list of genre options
            genre_options = ['Documentaries','Stand-Up Comedy','Dramas, Independent Movies, International Movies', "Kids\' TV",
                             'Dramas, International Movies, Romantic Movies','Action & Adventure, Sci-Fi & Fantasy','Horror Movies, Thrillers']
            #setting the condition and checking if the user options is in list options
            if user_genre in list_options:
                i = list_options.index(user_genre)   #getting the index of user genre
                genre_name = genre_options[i]      
                print(f"You selected {genre_name} genre.\n")   #printing the genre name
                choose_genre(user_genre = genre_name) #calling the function that will choose genre
            else:
                print()
                #print prompt
                print("You should select the above genre options. Please select genre from above options")
                menu() #if the user did not enter the input from the menu provided call the menu function again

            user_title =input("Enter the title name to get some recommendation like that: ") #getting title input
            print()
        
            
            try:
                get_df_title_genre(new_df,genre_name, user_title) #calling the title function passing the user chose title and the dataframe
            except Exception:
                print("The title could not be found. Please enter other title name.")
                menu()


        elif inp == 'N':  #setting condition to validate the user choice
            return "Thank you!!!!!"
            break  #breaking the loop if user entered the invalid input
            
        
        else:
            print("Please select the correct options.")
            continue  #continuing the loop to provide the user to continue with the program

```


```python
menu()  #calling the function

```

    How would you like to get the recommendations? 
          Enter 'T' if you would like to get recommendation just by title:
          Enter 'G' if you would like to get recommendation with genre and title:
          Enter 'N' for no recommendations and to quit:
    
    Please select the correct options.



    ---------------------------------------------------------------------------

    KeyboardInterrupt                         Traceback (most recent call last)

    <ipython-input-75-ef1f475bf5ec> in <module>
    ----> 1 menu()  #calling the function
    

    <ipython-input-74-2019602765ae> in menu()
          3     while True:
          4         #getting the input from users
    ----> 5         inp = input("How would you like to get the recommendations? \n"
          6                         "      Enter 'T' if you would like to get recommendation just by title:\n"
          7                         "      Enter 'G' if you would like to get recommendation with genre and title:\n"


    /opt/anaconda3/lib/python3.8/site-packages/ipykernel/kernelbase.py in raw_input(self, prompt)
        858                 "raw_input was called, but this frontend does not support input requests."
        859             )
    --> 860         return self._input_request(str(prompt),
        861             self._parent_ident,
        862             self._parent_header,


    /opt/anaconda3/lib/python3.8/site-packages/ipykernel/kernelbase.py in _input_request(self, prompt, ident, parent, password)
        902             except KeyboardInterrupt:
        903                 # re-raise KeyboardInterrupt, to truncate traceback
    --> 904                 raise KeyboardInterrupt("Interrupted by user") from None
        905             except Exception as e:
        906                 self.log.warning("Invalid Message:", exc_info=True)


    KeyboardInterrupt: Interrupted by user



```python

```

### Predicting Rating according to classification (machine learning technique)


```python
#n_data_filter.head(1)  #taking a glance of the dataframe
```


```python
# getting specific columns from the dataframe
data_knn = n_data_filter.loc[:,['netflixid','title','director','cast','rating']]

#dropping the nan values from the dataframe
data_knn = data_knn.dropna()
#data_knn   #looking how the dataframe looks like
```

Now we want to preidict the rating on based on cast, director, and rating category (TVMA, TV-14) of the movie/show. This technique is also called the supervised machine learning because we actually know what we want to predict. We know that all the features we are going to choose is in string format to we have to convert them to binary for classification


```python
#converting the cast names to binary

#making a empty list
castList = []

#using the for loop to loov over the cast column of dataframe to get the speciifc cast names
for ind, record in data_knn.iterrows():
    cast = record["cast"]
    
    # getting each cast names froma all the cast list
    for i in cast:
        #validating if the cast name is in the list because we do not want the same cast name to be repeated
        if i not in castList:  
            castList.append(i)  #only appending the cast name that is not in the list 


#print(castList)
```


```python
# once we have each cast name we have to convert it to 1 or 0's
#so we define the function called convert
def convert(x_list, data_list):
    
    #made a new list so that we will append it later
    convert_to_binary=[]
    
    #using for loop from the list passed 
    for y in data_list:
        if y in x_list:  #setting condition to check if the list contains the items
            convert_to_binary.append(1) #so if the item was in the list convert that item to 1
        else:
            convert_to_binary.append(0)  # if the item was not in the list convert it to 0.
        
    return convert_to_binary #returning the list

#applying the function for cast column of dataframe because we wanted to convert the cast column to binary
data_knn['cast_binary'] = data_knn['cast'].apply(lambda x: convert(x,castList)) 
data_knn['cast_binary'].head(2)
```




    0    [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...
    4    [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, ...
    Name: cast_binary, dtype: object




```python
# making a director list so that we will have director names and append it to this list
directorList=[]
for i in data_knn['director']:  #using for loop in director columns
    if i not in directorList:  #validating if the director name is not repeated
        directorList.append(i)   #appending the director names in the list
        
        
#calling a function and making a new column in dataframe with 1 and 0 values      
data_knn['director_binary'] = data_knn['director'].apply(lambda x: convert(x, directorList))
data_knn.head(2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>title</th>
      <th>director</th>
      <th>cast</th>
      <th>rating</th>
      <th>cast_binary</th>
      <th>director_binary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>81145628</td>
      <td>Norm of the North: King Sized Adventure</td>
      <td>Richard Finn, Tim Maltby</td>
      <td>Alan Marriott, Andrew Toth, Brian Dobson, Cole...</td>
      <td>TV-PG</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>80125979</td>
      <td>#realityhigh</td>
      <td>Fernando Lebrija</td>
      <td>Nesta Cooper, Kate Walsh, John Michael Higgins...</td>
      <td>TV-14</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, ...</td>
      <td>[0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
    </tr>
  </tbody>
</table>
</div>




```python
#also we are using rating category like: TV-MA, TV-14 to predict the rating so
#making a new description list

rating_list = []

#using for loop to get the row and column value of the dataframe
for ind, record in data_knn.iterrows():
    x = record["rating"]
    
    #using for loop to get each rating category
    for each in x:
        if each not in rating_list: #validating that the rating category is not repeated for same record
            rating_list.append(each)

# calling the function to convert it to binary and making a new column 
data_knn['rating_binary'] = data_knn['rating'].apply(lambda x: convert(x,rating_list))
data_knn.head(2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>title</th>
      <th>director</th>
      <th>cast</th>
      <th>rating</th>
      <th>cast_binary</th>
      <th>director_binary</th>
      <th>rating_binary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>81145628</td>
      <td>Norm of the North: King Sized Adventure</td>
      <td>Richard Finn, Tim Maltby</td>
      <td>Alan Marriott, Andrew Toth, Brian Dobson, Cole...</td>
      <td>TV-PG</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>80125979</td>
      <td>#realityhigh</td>
      <td>Fernando Lebrija</td>
      <td>Nesta Cooper, Kate Walsh, John Michael Higgins...</td>
      <td>TV-14</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, ...</td>
      <td>[0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
    </tr>
  </tbody>
</table>
</div>



spatial is python module is used to find the distance between two points. So when we imported spatial and used cosine distance modeule, it finds the distance between two points based on cosine. Cossine distance is based on cosine similarity. Cosine similarity is finding the distance based on cos-angle drawn by those two points. For example, if two points lie in same vector or nearer, the distance between them is nominal which increases the similarity or vice-versa. Thus this concept is applied to find the recommendation system as it finds the similarity between the features (casting,director and so on). 



```python

from scipy import spatial

#defining the fuunction that finds the similarity between two features
def Similarity(firstid, secondid):
    #getting specific rows
    first_set = data_knn.iloc[firstid] 
    second_set = data_knn.iloc[secondid]
    
    #getting the column data of cast binary of two sets
    first_cast = first_set['cast_binary']
    second_cast = second_set['cast_binary']
    
   # Compute the Cosine distance of 1-D array between first_cast and second_cast
    cast_distance = spatial.distance.cosine(first_cast, second_cast)
    
    
    #getting the column data of director binary of two sets
    first_director = first_set['director_binary']
    second_director = second_set['director_binary']
    
    # Compute the Cosine distance of 1-D array between first_director and second_director
    director_distance = spatial.distance.cosine(first_director, second_director)
    
    #getting the column data of rating binary of two sets
    first_rating = first_set['rating_binary']
    second_rating = second_set['rating_binary']
    
    # Compute the Cosine distance of 1-D array between first_rating and second_rating
    rating_distance = spatial.distance.cosine(first_rating, second_rating)
    
    return director_distance + cast_distance + rating_distance # returns total distance between the two data 
```


```python
# for example distance bewteen first row and hundreth row is calculated
Similarity(0,99)

# to understand more.....the data for the particular rows are printed
print(data_knn.iloc[0])
print(data_knn.iloc[99])
```

    netflixid                                                   81145628
    title                        Norm of the North: King Sized Adventure
    director                                    Richard Finn, Tim Maltby
    cast               Alan Marriott, Andrew Toth, Brian Dobson, Cole...
    rating                                                         TV-PG
    cast_binary        [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...
    director_binary    [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...
    rating_binary      [1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...
    Name: 0, dtype: object
    netflixid                                                   80243600
    title                                   Between Two Ferns: The Movie
    director                                              Scott Aukerman
    cast               Zach Galifianakis, Lauren Lapkus, Ryan Gaul, J...
    rating                                                         TV-MA
    cast_binary        [0, 1, 1, 1, 1, 0, 1, 1, 1, 0, 1, 0, 1, 0, 0, ...
    director_binary    [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...
    rating_binary      [1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...
    Name: 154, dtype: object



```python
# getting specific columns
rating_view_to_merge = netflix_data_filter.loc[:,['netflixid','rating']]

#renaming column names
rating_view_to_merge.rename(columns={'rating':'rating_num'}, inplace =True)

#mergind two dataframes
merge_for_recommendation = pd.merge(data_knn, rating_view_to_merge, on='netflixid', how='inner')

#print(merge_for_recommendation.shape) 
merge_for_recommendation.head(2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>title</th>
      <th>director</th>
      <th>cast</th>
      <th>rating</th>
      <th>cast_binary</th>
      <th>director_binary</th>
      <th>rating_binary</th>
      <th>rating_num</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>80045922</td>
      <td>6 Years</td>
      <td>Hannah Fidell</td>
      <td>Taissa Farmiga, Ben Rosenfield, Lindsay Burdge...</td>
      <td>NR</td>
      <td>[0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, ...</td>
      <td>5.6</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80157072</td>
      <td>Hold the Dark</td>
      <td>Jeremy Saulnier</td>
      <td>Jeffrey Wright, Alexander Skarsgård, James Bad...</td>
      <td>TV-MA</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>5.6</td>
    </tr>
  </tbody>
</table>
</div>




```python
# specifying range into new variable
new_id = range(0,merge_for_recommendation.shape[0])

#making a new column with customized sequential ids
merge_for_recommendation['new_id']=new_id

#specifying 
merge_for_recommendation=merge_for_recommendation.drop(columns = ['netflixid'])

#'original_title','genres','vote_average','genres_bin','cast_bin','new_id','director','director_bin','words_bin']]


merge_for_recommendation.head(15)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>title</th>
      <th>director</th>
      <th>cast</th>
      <th>rating</th>
      <th>cast_binary</th>
      <th>director_binary</th>
      <th>rating_binary</th>
      <th>rating_num</th>
      <th>new_id</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>6 Years</td>
      <td>Hannah Fidell</td>
      <td>Taissa Farmiga, Ben Rosenfield, Lindsay Burdge...</td>
      <td>NR</td>
      <td>[0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, ...</td>
      <td>5.6</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Hold the Dark</td>
      <td>Jeremy Saulnier</td>
      <td>Jeffrey Wright, Alexander Skarsgård, James Bad...</td>
      <td>TV-MA</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>5.6</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Joseph: King of Dreams</td>
      <td>Rob LaDuca, Robert C. Ramirez</td>
      <td>Ben Affleck, Mark Hamill, Richard Herd, Mauree...</td>
      <td>TV-PG</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>6.5</td>
      <td>2</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Swearnet: The Movie</td>
      <td>Warren P. Sonoda</td>
      <td>Mike Smith, John Paul Tremblay, Robb Wells, Pa...</td>
      <td>NR</td>
      <td>[0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, ...</td>
      <td>5.9</td>
      <td>3</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Gaga: Five Foot Two</td>
      <td>Chris Moukarbel</td>
      <td>Lady Gaga</td>
      <td>TV-MA</td>
      <td>[0, 0, 1, 0, 1, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>7.0</td>
      <td>4</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Barbie Dolphin Magic</td>
      <td>Conrad Helten</td>
      <td>Erica Lindbeck, Shannon Chan-Kent, Kazumi Evan...</td>
      <td>TV-G</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>5.7</td>
      <td>5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Keith Richards: Under the Influence</td>
      <td>Morgan Neville</td>
      <td>Keith Richards</td>
      <td>TV-PG</td>
      <td>[0, 0, 1, 0, 1, 0, 1, 1, 0, 1, 0, 1, 1, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>7.2</td>
      <td>6</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Cedric the Entertainer: Live from the Ville</td>
      <td>Troy Miller</td>
      <td>Cedric the Entertainer</td>
      <td>TV-MA</td>
      <td>[0, 0, 1, 1, 1, 0, 1, 1, 0, 1, 0, 1, 1, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>5.9</td>
      <td>7</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Cowspiracy: The Sustainability Secret</td>
      <td>Kip Andersen, Keegan Kuhn</td>
      <td>Kip Andersen</td>
      <td>NR</td>
      <td>[1, 0, 0, 1, 1, 0, 1, 1, 0, 0, 0, 1, 1, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, ...</td>
      <td>8.3</td>
      <td>8</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Jeff Dunham: Relative Disaster</td>
      <td>Michael Simon</td>
      <td>Jeff Dunham</td>
      <td>TV-MA</td>
      <td>[0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>NaN</td>
      <td>9</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Garbage</td>
      <td>Qaushiq Mukherjee</td>
      <td>Tanmay Dhanania, Trimala Adhikari, Satarupa Da...</td>
      <td>TV-MA</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>3.3</td>
      <td>10</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Brother's Shadow</td>
      <td>Todd S. Yellin</td>
      <td>Scott Cohen, Judd Hirsch, Susan Floyd, Elliot ...</td>
      <td>TV-14</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>6.1</td>
      <td>11</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Little Evil</td>
      <td>Eli Craig</td>
      <td>Adam Scott, Evangeline Lilly, Bridget Everett,...</td>
      <td>TV-MA</td>
      <td>[1, 1, 1, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>5.7</td>
      <td>12</td>
    </tr>
    <tr>
      <th>13</th>
      <td>A Noble Intention</td>
      <td>Joram Lürsen</td>
      <td>Gijs Scholten van Aschat, Jacob Derwig, Rifka ...</td>
      <td>NR</td>
      <td>[1, 1, 1, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, ...</td>
      <td>6.7</td>
      <td>13</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Bon Bini Holland</td>
      <td>Jelle de Jonge</td>
      <td>Jandino Asporaat, Liliana de Vries, Teun Kuilb...</td>
      <td>TV-14</td>
      <td>[1, 1, 1, 1, 1, 0, 1, 1, 1, 1, 1, 1, 1, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>5.6</td>
      <td>14</td>
    </tr>
  </tbody>
</table>
</div>




```python
for ind, merge_for_recommend in merge_for_recommendation.iterrows():
    print(merge_for_recommend)
    
    break
```

    title                                                        6 Years
    director                                               Hannah Fidell
    cast               Taissa Farmiga, Ben Rosenfield, Lindsay Burdge...
    rating                                                            NR
    cast_binary        [0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...
    director_binary    [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, ...
    rating_binary      [0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, ...
    rating_num                                                       5.6
    new_id                                                             0
    Name: 0, dtype: object



```python
merge_for_recommendation = merge_for_recommendation.dropna()
merge_for_recommendation.shape
```




    (287, 9)




```python
def getNeighbors(standard_movie_to_comp, K):
        distances = []
        
        #using for loop to acess the index no of rows and the data of rows with the columnnames
        for ind, merge_for_recommend in merge_for_recommendation.iterrows():
            
            #checking if the value of id of series is matched with the user entered value of the series
            if merge_for_recommend['new_id'] != standard_movie_to_comp['new_id'].values[0]:
                
                #calling similarity function to find the disance between the user selected title and the title located in dataframe
                dist = Similarity(standard_movie_to_comp['new_id'].values[0], merge_for_recommend['new_id'])
                
                #appending the value of distances 
                distances.append((merge_for_recommend['new_id'], dist))
        
        #sorting the distances, constructing iterable object and fetching the 1st element out of it.
        distances.sort(key=operator.itemgetter(1))
        neighbors = []  #empty list
    
        #using for loop to append the distances 
        for x in range(K):
            neighbors.append(distances[x])
        return neighbors

```


```python
def predict_rating():
    # asking title from the user
    #using try and except block
    try:
        name_movie = input('Enter a movie title: ')
        print('')

        #looking for the users title in the dataframe. Once the title is found picking whole row and converting it to dataframe and transposing it

        new_movie = merge_for_recommendation[merge_for_recommendation['title'].str.contains(name_movie)].iloc[0].to_frame().T
        print('Selected Movie: ',new_movie.title.values[0])
        
    
        K = 5 #supposing value of k to be 5 and Rating to be 0
        Rating = 0
        neighbors = getNeighbors(new_movie, K)  #calling function that will get the user input and title and find the distance


        for i in neighbors:  #using for loop to find the rating by summing all the rating distances
            Rating = Rating+merge_for_recommendation.iloc[i[0]][7] 
        
        print('\n')
        Rating = Rating/K  #the predicted rating
        print('The predicted rating for %s is %f' %(new_movie['title'].values[0],Rating))
        print('The actual rating for %s is %f' %(new_movie['title'].values[0],new_movie['rating_num']))
    
        #print(f"The predicted rating for {new_movie['title'].values[0]} is {Rating}")
        #print(f"The actual rating for {new_movie['title'].values[0]} is {new_movie['rating_num']}")

    
    except Exception:
        print("\nYour movie can not be processed/found for rating prediction. Please enter another movies like \n"
                     "Hold the Dark\n"
                    "Little Evil")
        predict_rating()
    
```


```python

```


```python
predict_rating()

#try the following:
    #Hold the Dark
    #Gaga: Five Foot Two
    # Time Trap
    #Supergirl
    #Little Evil

```

    Enter a movie title: Hold the Dark
    
    Selected Movie:  Hold the Dark
    
    
    The predicted rating for Hold the Dark is 6.320000
    The actual rating for Hold the Dark is 5.600000


## KNN classifications for rating by director


```python
#dropping duplicates
n_data_filter =n_data.drop_duplicates(subset=['netflixid','title'])
netflix_data_filter =netflix_dat.drop_duplicates(subset=['netflixid','title'])

print(netflix_data_filter.duplicated().any()) #again checking if any duplicates left
print(n_data_filter.duplicated().any()) # checking andy duplicates 
```

    False
    False



```python
copy_count_rated.head(2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>type</th>
      <th>title</th>
      <th>director</th>
      <th>cast</th>
      <th>country</th>
      <th>date_added</th>
      <th>release_year</th>
      <th>rating</th>
      <th>duration</th>
      <th>listed_in</th>
      <th>description</th>
      <th>added_year</th>
      <th>added_month</th>
      <th>rating_num</th>
      <th>unogsdate</th>
      <th>rating_standard</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>70234439</td>
      <td>TV Show</td>
      <td>Transformers Prime</td>
      <td>NaN</td>
      <td>Peter Cullen, Sumalee Montano, Frank Welker, J...</td>
      <td>United States</td>
      <td>2018-09-08</td>
      <td>2013</td>
      <td>TV-Y7-FV</td>
      <td>1 Season</td>
      <td>Kids' TV</td>
      <td>With the help of three human allies, the Autob...</td>
      <td>2018.0</td>
      <td>9.0</td>
      <td>7.8</td>
      <td>NaT</td>
      <td>High-rated</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80045922</td>
      <td>Movie</td>
      <td>6 Years</td>
      <td>Hannah Fidell</td>
      <td>Taissa Farmiga, Ben Rosenfield, Lindsay Burdge...</td>
      <td>United States</td>
      <td>2015-09-08</td>
      <td>2015</td>
      <td>NR</td>
      <td>80 min</td>
      <td>Dramas, Independent Movies, Romantic Movies</td>
      <td>As a volatile young couple who have been toget...</td>
      <td>2015.0</td>
      <td>9.0</td>
      <td>5.6</td>
      <td>NaT</td>
      <td>Low-rated</td>
    </tr>
  </tbody>
</table>
</div>




```python
#getting specific columns
rating_merge_classify = copy_count_rated.loc[:,['netflixid','rating_standard','rating_num']]
#merging two dataframes
merge_for_classification = pd.merge(data_knn, rating_merge_classify, on='netflixid', how='inner')

merge_for_classification.head(2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>title</th>
      <th>director</th>
      <th>cast</th>
      <th>rating</th>
      <th>cast_binary</th>
      <th>director_binary</th>
      <th>rating_binary</th>
      <th>rating_standard</th>
      <th>rating_num</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>80045922</td>
      <td>6 Years</td>
      <td>Hannah Fidell</td>
      <td>Taissa Farmiga, Ben Rosenfield, Lindsay Burdge...</td>
      <td>NR</td>
      <td>[0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, ...</td>
      <td>Low-rated</td>
      <td>5.6</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80157072</td>
      <td>Hold the Dark</td>
      <td>Jeremy Saulnier</td>
      <td>Jeffrey Wright, Alexander Skarsgård, James Bad...</td>
      <td>TV-MA</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>Low-rated</td>
      <td>5.6</td>
    </tr>
  </tbody>
</table>
</div>




```python
#merge_for_classification.director.to_list()
```


```python
#LabelEncoder is a utility class to help normalize labels such that they contain only values between 0 and n_classes-1 
from sklearn import preprocessing

#creating labelEncoder, this will encode the y(target) variables
le = preprocessing.LabelEncoder()

# Converting string labels into numbers.
rating_encoded=le.fit_transform(merge_for_classification['rating'])
merge_for_classification['rating_encoded'] = rating_encoded
casting_encoded = le.fit_transform(merge_for_classification['cast'])
merge_for_classification['casting_encoded'] = casting_encoded
director_encoded = le.fit_transform(merge_for_classification['director'])
merge_for_classification['director_encoded'] = director_encoded
rating_standard_encoded = le.fit_transform(merge_for_classification['rating_standard'])
merge_for_classification['rating_standard_encoded'] = rating_standard_encoded


```


```python
merge_for_classification
#.rating_standard_encoded.to_list()

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>netflixid</th>
      <th>title</th>
      <th>director</th>
      <th>cast</th>
      <th>rating</th>
      <th>cast_binary</th>
      <th>director_binary</th>
      <th>rating_binary</th>
      <th>rating_standard</th>
      <th>rating_num</th>
      <th>rating_encoded</th>
      <th>casting_encoded</th>
      <th>director_encoded</th>
      <th>rating_standard_encoded</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>80045922</td>
      <td>6 Years</td>
      <td>Hannah Fidell</td>
      <td>Taissa Farmiga, Ben Rosenfield, Lindsay Burdge...</td>
      <td>NR</td>
      <td>[0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, ...</td>
      <td>Low-rated</td>
      <td>5.6</td>
      <td>0</td>
      <td>257</td>
      <td>86</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80157072</td>
      <td>Hold the Dark</td>
      <td>Jeremy Saulnier</td>
      <td>Jeffrey Wright, Alexander Skarsgård, James Bad...</td>
      <td>TV-MA</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>Low-rated</td>
      <td>5.6</td>
      <td>6</td>
      <td>113</td>
      <td>114</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2</th>
      <td>60003155</td>
      <td>Joseph: King of Dreams</td>
      <td>Rob LaDuca, Robert C. Ramirez</td>
      <td>Ben Affleck, Mark Hamill, Richard Herd, Mauree...</td>
      <td>TV-PG</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>Low-rated</td>
      <td>6.5</td>
      <td>7</td>
      <td>20</td>
      <td>208</td>
      <td>1</td>
    </tr>
    <tr>
      <th>3</th>
      <td>70304191</td>
      <td>Swearnet: The Movie</td>
      <td>Warren P. Sonoda</td>
      <td>Mike Smith, John Paul Tremblay, Robb Wells, Pa...</td>
      <td>NR</td>
      <td>[0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, ...</td>
      <td>Low-rated</td>
      <td>5.9</td>
      <td>0</td>
      <td>191</td>
      <td>249</td>
      <td>1</td>
    </tr>
    <tr>
      <th>4</th>
      <td>80196586</td>
      <td>Gaga: Five Foot Two</td>
      <td>Chris Moukarbel</td>
      <td>Lady Gaga</td>
      <td>TV-MA</td>
      <td>[0, 0, 1, 0, 1, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, ...</td>
      <td>High-rated</td>
      <td>7.0</td>
      <td>6</td>
      <td>155</td>
      <td>37</td>
      <td>0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>298</th>
      <td>70245163</td>
      <td>Call the Midwife</td>
      <td>Philippa Lowthorpe</td>
      <td>Vanessa Redgrave, Bryony Hannah, Helen George,...</td>
      <td>TV-14</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>High-rated</td>
      <td>8.4</td>
      <td>4</td>
      <td>272</td>
      <td>197</td>
      <td>0</td>
    </tr>
    <tr>
      <th>299</th>
      <td>80062047</td>
      <td>Degrassi: Next Class</td>
      <td>Stefan Brogren</td>
      <td>Amanda Arcuri, Amir Bageria, Soma Bhatia, Jami...</td>
      <td>TV-14</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>High-rated</td>
      <td>7.0</td>
      <td>4</td>
      <td>8</td>
      <td>230</td>
      <td>0</td>
    </tr>
    <tr>
      <th>300</th>
      <td>70180293</td>
      <td>The Cat in the Hat Knows a Lot About That!</td>
      <td>Tony Collingwood</td>
      <td>Martin Short, Alexa Torrington, Jacob Ewaniuk,...</td>
      <td>TV-Y</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, ...</td>
      <td>Low-rated</td>
      <td>6.6</td>
      <td>8</td>
      <td>180</td>
      <td>244</td>
      <td>1</td>
    </tr>
    <tr>
      <th>301</th>
      <td>70204981</td>
      <td>Fullmetal Alchemist: Brotherhood</td>
      <td>Yasuhiro Irie</td>
      <td>Romi Park, Rie Kugimiya, Megumi Takamoto, Shin...</td>
      <td>TV-14</td>
      <td>[0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>High-rated</td>
      <td>9.1</td>
      <td>4</td>
      <td>224</td>
      <td>257</td>
      <td>0</td>
    </tr>
    <tr>
      <th>302</th>
      <td>70142436</td>
      <td>Merlin</td>
      <td>James Hawes</td>
      <td>Colin Morgan, Bradley James, Katie McGrath, An...</td>
      <td>TV-PG</td>
      <td>[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 0, 0, ...</td>
      <td>[0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>[1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, ...</td>
      <td>High-rated</td>
      <td>7.9</td>
      <td>7</td>
      <td>48</td>
      <td>100</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>303 rows × 14 columns</p>
</div>




```python
#defining x values and y values
X = merge_for_classification[['casting_encoded','director_encoded']].values
y= merge_for_classification['rating_standard_encoded'].to_numpy()

```


```python
from sklearn.model_selection import train_test_split
from sklearn import metrics

def classify_rating(c,d):
    
    X = merge_for_classification[['casting_encoded','director_encoded']].values
    y= merge_for_classification['rating_standard_encoded'].values

    #print(X)
    #print(y)

    # Split dataset into training set and test set
    X_train_first, X_test_first, y_train_first, y_test_first = train_test_split(X, y, train_size = 0.8,test_size=0.2, random_state=4) # 70% training and 30% test


    from sklearn.neighbors import KNeighborsClassifier
    # Create the knn model.
    # Look at the five closest neighbors.
    knn = KNeighborsClassifier(n_neighbors=5)
    # Fit the model on the training data.
    knn.fit(X_train_first, y_train_first)
    # Make point predictions on the test set using the fit model.
    #predictions = knn.predict(X_test_first)

    predicted= knn.predict([[c,d]]) 

    
    #print(predicted)
    #print(metrics.accuracy_score(y_test_first, predictions))
    
    print(" ")
    
    director_name = merge_for_classification[merge_for_classification['director_encoded'] == d].iloc[0][2]
    movie_title = merge_for_classification[merge_for_classification['casting_encoded'] == c].iloc[0][1]
    
    #print(f"The rating standard is: {predicted}")
    if predicted == [1]:
        print(f"If '{director_name}' directs '{movie_title}', the rating standard will be Low-rated.")
    else:
        print(f"If '{director_name}' directs '{movie_title}', the rating standard will be High-rated.")
    
    
    


```


```python

def get_cast_director_info():
    title = input("Enter a title name: ")
    print(" ")
    
    #getting title according to user
    new_title = merge_for_classification[merge_for_classification['title'].str.contains(title)].iloc[0].to_frame().T
    
    #getting encoded values from the user selection
    cast_encoded = new_title.casting_encoded.values[0]
    print(f"The cast name for this movie are: \n------{new_title.cast.values[0]}")
    print(" ")
    print(f"This movie/show is {new_title.rating_standard.values[0]}.")
    
    #asking for the director
    director =input("Enter a director name that you would like to see this movie directed: ")
    #new_movie = merge_for_classification[merge_for_classification['cast'].str.contains(name)].iloc[0].to_frame().T
    
    #getting movie data from director
    n_movie = merge_for_classification[merge_for_classification['director'].str.contains(director)].iloc[0].to_frame().T
    
    #getting director encoded
    direct_encoded = n_movie.director_encoded.values[0]
    
    return cast_encoded, direct_encoded

# Taissa Farmiga, Ben Rosenfield, Lindsay Burdge, Joshua Leonard, Jennifer Lafleur, 
#Peter Vack, Dana Wheeler-Nicholson, Jason Newman, Molly McMichael'
# Jay Karas

```


```python
##### note: use title name 6 Years. It is Low-rated and the director named Jay Karas will make it high-rated.
```


```python
#calling a function
cast,director = get_cast_director_info()
classify_rating(cast, director)

```

    Enter a title name: 
     
    The cast name for this movie are: 
    ------Taissa Farmiga, Ben Rosenfield, Lindsay Burdge, Joshua Leonard, Jennifer Lafleur, Peter Vack, Dana Wheeler-Nicholson, Jason Newman, Molly McMichael
     
    This movie/show is Low-rated.
    Enter a director name that you would like to see this movie directed: 
     
    If 'Hannah Fidell' directs '6 Years', the rating standard will be Low-rated.



```python

```
