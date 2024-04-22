# Dark-Mode-Power-BI-dashboard
This is my dashboard with implemented dark mode toggle button

### Creating a dashboard with light/dark mode toggle
<img src="BI/store_dash.gif?raw=true"/>

### 1. The Retail Store Sales dataset was taken from from [kaggle](https://www.kaggle.com/datasets/mohammadtalib786/retail-sales-dataset)
### 2. The Power BI dashboard was created
<img src="BI/light_store_dash.png?raw=true"/>
<img src="BI/dark_store_dash.png?raw=true"/>
### 3. To create dark mode option:
- I've created an additional table
<br><br>
<img src="BI/mode_table.png?raw=true"/>

- Added slicer
<br><br>
<img src="BI/mode_slicer.png?raw=true"/>

- Added measures with if function oriented on the slicer
```DAX
Background Vis = IF(
    SELECTEDVALUE(
        'Mode Selection'[Mode]) = "Light",
        "#ffffff",
        "#303036"
)
```
- Adjusted visualization formats to change automatically according to the measure
At this stage the switch is already working, all that's teft is to add a toggle button which is not that straight-forward.
### 4. Toggle button creating
- Create a bookmarks in this manner (The groupped one should be the switch itself)
<br><br>
<img src="BI/bookmarks.png?raw=true"/>
- Pass the following settings
<br><br>
<img src="BI/deselection.png?raw=true"/>
- Set the needed parameters in the Style section for defualt, selected, etc. states of the toggle.
<br><br>
<img src="BI/toggle_style.png?raw=true"/>
- The last step is to switch the mode slicer and update the bookmarks in the bookmars menu
-Your toggle is ready 🥳🎉🎊
<br><br>
<img src="BI/toggle.png?raw=true"/>







