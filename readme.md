# PropertyPro

This is a Property shortlisting app using the Google maps api.
It allows the user to save a detailed property list visually on a geographical map.

![alt text](http://i.imgur.com/ghOAlbH.png)

The user simply creates a short list of potential real estate. This could be for either for rental or investment. All important information is saved such as address, type of property, price, notes (hyperlink is necessary) etc...

## Lessions learned, Technology used.

This was my first collaborative project. It really help emphasise the importance of dividing work, Git branching and dealing with potential merge conflicts.

###Back- End
The back-end was created with Ruby on Rails. The SQL database referenced was created with PostGres. We explored the prospect of using 'geocoder' GEM to match longitude and latitude co-ordinates but eventually settled on using gmaps.js on the front-end.  

###Front-End
The front end markup was split into a top banner above left column (2 wide) and right column (10 wide). 

__Right column - GMAPS__ <br>
gmaps.js (Google maps) was used to fill the right column. This aloud us to drop pins which returned a longitude and latitude and created a pop up box. The user could add details to this pop up box and save the property to their list. 

![alt text](http://i.imgur.com/UWj0koW.png)

This was a huge learning curve. The [gmaps api](https://hpneo.github.io/gmaps/) had extensive documentation covering everything from start page centering to attaching labels and of course matching latitude and longitude to an address. It was a extremely important to pass information as detailed in the documentation.

__Left Column__ <br>
I split this column into the top 'login'/'sign up' panes and below it the saved Property List.

* I learnt how to use the bootstrap tab panes. To give the user the option of signing up or logging into an existing account. Learning to use this was fairly easy and straight forward process of assigning the correct bootstrap classes.

* The property list below was a little more difficult. As the number of properties on the list would be an undetermined length, it was important to find a formatting solution. We used the CSS3 "height: __ vh;"  function to keep the list finishing at the same level/point as the map in the right column. We then added "overflow: scroll;" which meant that if the complete property list can not be seen in the allocated space, The user can scroll up and down to see the whole list.




