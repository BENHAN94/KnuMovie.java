
// Entity and attributes

1.	MOVIE

1. Movie_id: Identification of movie
2. Primary_title: The most popular title of movie
3. Original_title: Original title of movie
4. Grade: grade of movie e.g. 15 rated, 12 rated, 19 rated
5. Release_date: Release date of movie
6. Running_time: Running time of movie
7. Production_country: Country where movie was taken from
8. Director: Director of movie
9. Season_number: Season number of TV series
10. Year- start, end: Start and end years of TV series

2.	GENRE

1. Genre_name: Name of genre

3.	RATING

1. Rating_id: Identification of rating
2. Rating: Rating which user evaluate
3. Comment: Comment which user write

4.	ACTOR

1. Actor_id: Identification of actor
2. Actor_name: Name of actor
3. Actor_age: Age of actor
4. Actor_sex: Sex of actor
5. Filmography: Filmography of actor

5.	Character

1. Character_id: Identification of character
2. Character_name: Name of character

6.	EPISODE

1. Episode_id: Identification of episode
2. Episode_name: Name of episode
3. Episode_number: Number of episode

7.	Version

1. Version_id: Identification of version
2. Location: Location or country that version was made for
3. Localized_title: Title of movie in location 
4. Location_language: Language of location of version

8.	ACCOUNT

1. Email_add: Email address of user
2. Password: Password of account
3. Phone: Phone number of user
4. Name(first, last): Name of user
5. Sex: Sex of user
6. Birthday: Birthday of user

9. 	Membership

1. Membership_title: Name of membership

// Relationship between entities

1. GENRE OF MOVIE: Represents genres of movies.
2. CHARACTER APPEAR IN MOVIE: Represents characters who appear in movies.
3. ACTOR PLAY CHARACTER: Represents actors who played characters in a movie.
4. VERSION PROVIDED BY MOVIE OR EPISODE: Represents versions of movies or episodes of TV series.
5. EPISODE CONTAINED BY MOVIE: Represents epsisodes of TV series.
6. MOVIE EVALUATED AS RATING: Represents movies evaluated as rating by users.
7. ACCOUNT EVALUATE RATING: Represents rating and comment of movies evaluated by users.
8. ACCOUNT SUBSCRIBE MEMBERSHIP: Represents membership which users subscribe.
 



