# liri-node-app
 LIRI is like iPhone's SIRI. However, while SIRI is a Speech Interpretation and Recognition Interface, LIRI is a _Language_ Interpretation and Recognition Interface. LIRI will be a command line node app that takes in parameters and gives you back data.


 LIRI will search Spotify for songs, Bands in Town for concerts, and OMDB for movies.

### What Each Command Should Do

1. `node liri.js concert-this <artist/band name here>`

   * This will search the Bands in Town Artist Events API (`"https://rest.bandsintown.com/artists/" + artist + "/events?app_id=codingbootcamp"`) for an artist and render the following information about each event to the terminal:

     * Name of the venue

     * Venue location

     * Date of the Event (use moment to format this as "MM/DD/YYYY")

2. `node liri.js spotify-this-song '<song name here>'`

   * This will show the following information about the song in your terminal/bash window

     * Artist(s)

     * The song's name

     * A preview link of the song from Spotify

     * The album that the song is from

   * If no song is provided then your program will default to "The Sign" by Ace of Base.

   
3. `node liri.js movie-this '<movie name here>'`

   * This will output the following information to your terminal/bash window:

     ```
       * Title of the movie.
       * Year the movie came out.
       * IMDB Rating of the movie.
       * Rotten Tomatoes Rating of the movie.
       * Country where the movie was produced.
       * Language of the movie.
       * Plot of the movie.
       * Actors in the movie.
     ```

   * If the user doesn't type a movie in, the program will output data for the movie 'Mr. Nobody.'

     * If you haven't watched "Mr. Nobody," then you should: <http://www.imdb.com/title/tt0485947/>

     * It's on Netflix!

   * You'll use the request package to retrieve data from the OMDB API. Like all of the in-class activities, the OMDB API requires an API key. You may use `trilogy`.

4. `node liri.js do-what-it-says`

   * Using the `fs` Node package, LIRI will take the text inside of random.txt and then use it to call one of LIRI's commands.

     * It should run `spotify-this-song` for "I Want it That Way," as follows the text in `random.txt`.

     * Edit the text in random.txt to test out the feature for movie-this and concert-this.


SCREENSHOTS:

Belen@Jaime_PC MINGW64 ~/desktop/liri-node-app (master)
$ node liri.js movie-this scarface
this is loaded
Title:  Scarface
Date Released:  09 Dec 1983
IMDB Rating:  8.3
Rotten Tomatoes Rating:  82%
Produced in :  USA
Languaged in :  English, Spanish
Plot Synopsis :  In Miami in 1980, a determined Cuban immigrant takes over a dru
g cartel and succumbs to greed.
Starring :  Al Pacino, Steven Bauer, Michelle Pfeiffer, Mary Elizabeth Mastranto
nio

Belen@Jaime_PC MINGW64 ~/desktop/liri-node-app (master)
$ node liri.js spotify-this-song beat it
this is loaded
Artist:  Michael Jackson
Song Name:  Beat It - Single Version
Album Title:  Thriller 25 Super Deluxe Edition
Preview Link:  https://open.spotify.com/artist/3fMbdgg4jU18AjLCKBhRSm

Artist:  The Beatles
Song Name:  Let It Be - Remastered 2009
Album Title:  Let It Be (Remastered)
Preview Link:  https://open.spotify.com/artist/3WrFJ7ztbogyGnTHbHJFl2

Artist:  Michael Jackson
Song Name:  Beat It - Single Version
Album Title:  Michael Jackson's This Is It
Preview Link:  https://open.spotify.com/artist/3fMbdgg4jU18AjLCKBhRSm


Belen@Jaime_PC MINGW64 ~/desktop/liri-node-app (master)
$ node liri.js spotify-this-song 'beat it'
this is loaded
Artist:  Michael Jackson
Song Name:  Beat It - Single Version
Album Title:  Thriller 25 Super Deluxe Edition
Preview Link:  https://open.spotify.com/artist/3fMbdgg4jU18AjLCKBhRSm

Artist:  The Beatles
Song Name:  Let It Be - Remastered 2009
Album Title:  Let It Be (Remastered)
Preview Link:  https://open.spotify.com/artist/3WrFJ7ztbogyGnTHbHJFl2

Artist:  Michael Jackson
Song Name:  Beat It - Single Version
Album Title:  Michael Jackson's This Is It
Preview Link:  https://open.spotify.com/artist/3fMbdgg4jU18AjLCKBhRSm


Belen@Jaime_PC MINGW64 ~/desktop/liri-node-app (master)
$ node liri.js concert-this u2
this is loaded

Belen@Jaime_PC MINGW64 ~/desktop/liri-node-app (master)
$ node liri.js concert-this beyonce
this is loaded

Belen@Jaime_PC MINGW64 ~/desktop/liri-node-app (master)
$ node liri.js concert-this rolling stones
this is loaded
Venue:  Hard Rock Stadium
Location:  Miami Gardens ,  United States
Date (MM-DD-YYYY):  3 - 20 - 2019

Venue:  TIAA Bank Field
Location:  Jacksonville ,  United States
Date (MM-DD-YYYY):  3 - 24 - 2019

Venue:  NRG Arena
Location:  Houston ,  United States
Date (MM-DD-YYYY):  3 - 28 - 2019

Venue:  State Farm Stadium (formerly University of Phoenix Stadium)
Location:  Glendale ,  United States
Date (MM-DD-YYYY):  4 - 7 - 2019

Venue:  Rose Bowl Stadium
Location:  Pasadena ,  United States
Date (MM-DD-YYYY):  4 - 11 - 2019

Venue:  Levi's Stadium
Location:  Santa Clara ,  United States
Date (MM-DD-YYYY):  4 - 18 - 2019

Venue:  CenturyLink Field
Location:  Seattle ,  United States
Date (MM-DD-YYYY):  4 - 22 - 2019

Venue:  Broncos Stadium at Mile High
Location:  Denver ,  United States
Date (MM-DD-YYYY):  4 - 26 - 2019

Venue:  FedEx Field
Location:  Landover ,  United States
Date (MM-DD-YYYY):  4 - 31 - 2019

Venue:  Lincoln Financial Field
Location:  Philadelphia ,  United States
Date (MM-DD-YYYY):  5 - 4 - 2019

Venue:  Gillette Stadium
Location:  Foxborough ,  United States
Date (MM-DD-YYYY):  5 - 8 - 2019

Venue:  MetLife Stadium
Location:  East Rutherford ,  United States
Date (MM-DD-YYYY):  5 - 13 - 2019

Venue:  Soldier Field
Location:  Chicago ,  United States
Date (MM-DD-YYYY):  5 - 21 - 2019


 https://jaime-fajardo.github.io/liri-node-app/