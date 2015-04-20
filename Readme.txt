The web application consists of 4 pages.
login.jsp
registtration.jsp
search.jsp
searchresult.jsp
forgotpassword.jsp

The user first logins using the login.jsp where the login validation is done using ajax calling.
After successful validation the user will be redirected to search page where the user can enter the search criteria.
The user can enter his search using  3 constraints 
1. Keyword based search
2. The location coordinates
3. Radius (that is search radius from the location provided)

After submitting the search Criteria the application uses the google apis to find the videos which the user has requested. The top 25 videos from will be returned based on the search criteria.
These videos will be displayed in table in a the searchresult.jsp

Basically the flow will be as follows.
 login.jsp ---- forgotpassword.jsp
    |    |(LoginUnsuccessful)
Login.java
	|(LoginSuccessfull)
 search.jsp  
	|
SearchPage.java
	|
GeoLocationSearch.java
    |
searchresult.jsp	
	