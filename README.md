
![Logo](https://wallpapers.com/images/high/spotify-logo-blackand-white-dw7m8iuoy0jbk8a0.png)




Spotify, a global leader in music streaming, revolutionizes the way we listen to music with its vast library and personalized recommendations. Launched in 2008, it offers millions of tracks, podcasts, and exclusive content accessible across various devices. By seamlessly blending technology and artistry, Spotify caters to diverse musical tastes and enhances the listening experience. Its innovative algorithms and user-friendly interface keep listeners engaged and connected. Whether discovering new artists or enjoying timeless classics, Spotify has become an essential part of modern musical life.





## 📄 **OBJECTIVE**
The project entails the developement of a insightful Power-BI dashboard aimed at providind valuable insights into **SPOTIFY**🎧 **MUSIC**🎶. Leveraging a comprehensive dataset , the dashboard offers detail analysis of most played🎸 streams & tracks🎧 of a particular Artist 

🔨 Applications that are used :
1. **Powerpoint** : Used for Creating a beautiful Background
2. **Canva** : Used for Creating Some Important **LOGOs** That are later used in dashboard 
3. **Power-BI** : The dashboard is created using POWER-BI & the concepts used are
    
    --Power Query for Data cleaning 🔧
    
    -- Different charts📈 ,cards 💳 , tables for Visualiation 📅


Analyse the given dataset make different predictions and draw meaningful conclusion in order to grow the business.
 




##  📥 **DATA SOURCING & DATA MODELING**
Download the following data from the link beleow
  
  Dataset: https://onyxdata.ck.page/a12261b1fb

  Here, we have two spreadshets📋 out of which we selct the spotify data-sets & click transform data, which takes us to power query for cleaning & trasforming the data-sets✂️.

  **Data cleaning* : cleaned the required columns by removing the errors ❌ , changing its datatypes & replacing the values wherever required.
    
    
like, removed the errors from streams changed the datatype of track_name column replaced the null values in key columns & shazam_charts columns

➕ Merged released_year,released_month & released_day to single column.

Next, created an addtional Date table(Name of the table calendar) using power query
 
 the DAX Formula used ➡️

 Calendar = 
ADDCOLUMNS(
    CALENDAR(MIN('Spotify Dataset'[Date]), MAX('Spotify Dataset'[Date])),
    "Year", YEAR([Date]),
    "Quarter", QUARTER([Date]),
    "Quarter (Q)", "Q" & QUARTER([Date]),
    "Month", MONTH([Date]),
    "Month Name", FORMAT([Date], "mmm"),
    "Day Week", WEEKDAY([Date]),
    "Day Name", FORMAT([Date], "dddd")
)

This is done so that the model could predict performance over time.

After, this we performed Data modeling.

![Screenshot (24)](https://github.com/Akash-Dutta07/Spotify_Data_Analysis/assets/164155681/cc50f235-2888-444d-92b7-7184b58fee6b)

calendar to spotify dataset showing one to many-relation


  
## 📊 **VISUALIZATION & INSIGHTS**
![Screenshot (25)](https://github.com/Akash-Dutta07/Spotify_Data_Analysis/assets/164155681/9de2a29b-cd5a-4523-bac8-5966388f8711)
   
     
This is the Final Visualzation....

1. Total streams , total no. of tracks &  Avg streams 🎵
   
   ![Screenshot (2)](https://github.com/Akash-Dutta07/Spotify_Data_Analysis/assets/164155681/c7777e71-bf9b-437a-8ea8-c7bc6065c71a)

 
 2. Table is created to analyse Tracks & streams by month 📆 where January happens have the highest avgerage streams and tracks and August has the lowest tracks Febuary has the lowest Average streams

 ![Screenshot (26)](https://github.com/Akash-Dutta07/Spotify_Data_Analysis/assets/164155681/0fbda8dd-28ac-46ec-a910-c577091ed9e0)

 where as line charts 📈 shows total streams over time .
 
 Also, from the Bar charts we get an insight that Friday has the highest streams for all tracks

 3. ![Screenshot (25)](https://github.com/Akash-Dutta07/Spotify_Data_Analysis/assets/164155681/36608036-8588-42c6-b3af-6650337856a3)

 
  Created, a filter using tracks_name & streams(measure)
    
& for the image(of the respective track)we have **URL** column that is cover URL in the spotify_Dataset that would filter down the images of the respective Track.

Used multi card  💶 to get the insights on the following for the respective tracks


  - Release Date    📆
  
  - streams  🎼
  
  - Mode ▶️
  
  - key 🎹
   

   Again, used card to show 

   - Energy⚡ 
   - Speechiness🎸
   - liviness of the track  🌟
   - Dancebality 💃
   - Instrumentals 🎷



 4. For the third Section we agin use (NEW) Slicer to show top 5 tracks with highest number of streams 
 

  
  ![Screenshot (28)](https://github.com/Akash-Dutta07/Spotify_Data_Analysis/assets/164155681/2c0ca786-33ba-4c57-a2aa-8f63e1bb5e35) 

  **The images 📷 appeared because of the column "Cover_URL" in the spotify Data_sets which we formated in the image section of the Visual panel*

  5. Finally, we add a slicer to the top in a drop down format that shows all the tracks .
   we did the same for Dates and Artists_Name.
Also, for the Artists_name slicer we turned off interaction with few of the visuals.    
  
  ![Screenshot (27)](https://github.com/Akash-Dutta07/Spotify_Data_Analysis/assets/164155681/007c780c-82bc-40c8-a786-f3857becaea5)
  

## 📝 **CONCLUSION**
By analyzing Spotify's data, users can make informed decisions about their listening habits and discover new music preferences. They can gain insights into trending genres, popular tracks, and personalized recommendations tailored to their tastes. Identifying the most streamed songs and artists helps users find popular content and emerging talents. This analysis can engage listeners who seek fresh and relevant music experiences. Ultimately, such data insights can enhance user satisfaction, boost Spotify's reputation, and drive revenue growth through increased user engagement and retention.
