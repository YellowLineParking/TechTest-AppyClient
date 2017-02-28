#1 Login
*As a* mobile app user  
*I want* to be able to log in using my username and password  
*So that* I can access the app functionality.  

### 1.1 Login Screen
*Given* I have not logged in before     
*When* I open the app    
*Then* I am presented with a login screen   
*And* the login form contains fields for username & password and a submit button   

### 1.2 Failed Login
*Given* I have filled out the login form with incorrect credentials   
*When* I click submit   
*Then* I am not logged in   
*And* an login failure message is shown   

### 1.3 Successful Login
*Given* I have filled out the login form with correct credentials   
*When* I click submit   
*Then* I am logged in   
*And* the login screen disappears   

### 1.4 Automatic Login
*Given* I have logged in previously   
*When* I open the app after a period of time   
*Then* I am already logged in   


#2 Map Screen 
*As a* Logged in user     
*I want* To use a map to search and display parking data   
*So that* I can find parking bays near a location   

### 2.1 Show Map
*Given* I am logged in   
*When* The app loads          
*Then* I am presented with a screen containing an interactive map   
*And* The map is centered on my current location   

### 2.2 Load Data In Map
*Given* The map has loaded   
*When* The viewport is initialised  
*Then* Pins are shown on the map for each parking bay inside the viewport 
*And* The pins are represented by custom icons   

### 2.3 Move Map
*Given* The map has loaded   
*When* The viewport is moved   
*Then* Pins are shown on the map for each parking bay inside the viewport   
*And* The pins are represented by custom icons   


#3 Pin Information Overlay 
*As a* Logged in user who is looking at the map    
*I want* To see information about a specific pin   
*So that* I can understand more detail about a particular parking space   

### 3.1 Open Pin Information
*Given* Pins are visible on the map    
*When* I click on a pin   
*Then* An information panel is overlayed on the map   
*And* The information panel contains additional details about the selected pin   
*And* The information panel contains a close button

### 3.2 Close Pin Information
*Given* A pin information panel is visible      
*When* I click on the close icon   
*Then* The information panel disappears   

#4 Pin Filters
*As a* Logged in user who is looking at the map    
*I want* To filter pins by type   
*So that* The map only shows pins for a particular type of bay   


### 4.1 Pin filter selection
*Given* The map screen is visible    
*When* The screen loads  
*Then* A filter panel is visible  
*And* the filter panel contains options for parking bay types   

### 4.2 Pin filtering updates the map
*Given* I am selecting a parking bay type filter   
*When* I change my filter selection   
*Then* The set of pins shown on the map is updated to only display pins matching the selected filter   


#5 Zone Information
*As a* Logged in user who is looking at the map     
*I want* To know where parking zones are located  
*So that* I can see where the borders of zones lie.   

### 5.1 Draw zone borders
*Given* The map has loaded   
*When* The viewport is initialised or moved   
*Then* The zone borders should be shown on the map   
