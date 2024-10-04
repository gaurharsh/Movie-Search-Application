
# Movie Search Application

# Project Overview: 
The Movie Search Application is a web application that fetches and displays movie data from the OMDb API. The goal is to allow users to search for movies by title and filter results by year, while presenting movie information such as ratings, box office collections, plot, and more in a user-friendly UI.


## Table of Contents
# Features
# Setup and Run Instructions
# Usage
# Assumptions and Decisions
# Screenshots
# API Reference
# Technologies Used
# Documentation
# Dependencies
# Data Handling
# Badges
# License
# Links
# Support





## Features
- Search for movies by title using the OMDb API.
- Display detailed movie information: box office collection, ratings, plot, runtime, genre, actors, director, etc.
- Filter movies by year for refined search results.
- Handle API responses and errors gracefully.
- Responsive and user-friendly UI.
## Steps to Set Up Locally

1. **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/movie-info-app.git
    cd movie-info-app
    ```

2. **Obtain an API Key:**

    - Go to the [OMDb API](http://www.omdbapi.com/apikey.aspx) and request a free API key.
    
3. **Set up your environment:**

    - Create a `.env` file or manage the API key securely in your code. Example for a `.env` file:
    
    ```
    OMDB_API_KEY=your_api_key_here
    ```

    - Ensure your code retrieves this API key securely.

4. **Open the application:**

    - Simply open the `index.html` file in your preferred web browser.
    
    - Alternatively, serve the files using a local development server (optional):
    
    ```bash
    # If you have Python installed, you can run:
    python -m http.server
    ```

5. **Enjoy the application!**

## Setup and Installation
 A web browser (Google Chrome, Mozilla Firefox, etc.).
- [Git](https://git-scm.com/) installed on your machine.
- API key from the [OMDb API](http://www.omdbapi.com/apikey.aspx).
- 
## Usage/Examples
1. # Search for Movies by Title
Implementation:
Provide a search bar where users can input the movie title.
Use JavaScript's fetch() or XMLHttpRequest to call the OMDb API with the movie title provided by the user.
The API request will be formatted as:

http://www.omdbapi.com/?t=<MOVIE_TITLE>&apikey=<YOUR_API_KEY>

Once the data is fetched, display the movie information in the UI.

2. # Display Detailed Movie Information
Implementation:

Once the API response is received, extract details such as the box office collection, ratings, plot, runtime, genre, actors, and director from the response data.
Dynamically update the UI with these details.

3. # Filter Movies by Year
Implementation:

Add a dropdown or input field for the user to enter the release year.
Modify the API request to include the y parameter to filter results by year:
php

http://www.omdbapi.com/?t=<MOVIE_TITLE>&y=<MOVIE_YEAR>&apikey=<YOUR_API_KEY>

Ensure the filtered results only display movies that match both the title and the year.

4. # Handle API Responses and Errors Gracefully
Implementation:
Check if the API response contains an error message or if the movie is not found. Display user-friendly error messages accordingly.
Use try...catch blocks to handle any potential issues with API calls or network errors.

5. # Responsive and User-Friendly UI
Implementation:

Design the UI using HTML and CSS to ensure it is responsive on different screen sizes (e.g., desktop, mobile, tablet).
Display movie details in an easy-to-read format, with clear separation between sections (box office, ratings, etc.).
Include a loading spinner or placeholder while waiting for the API response to improve user experience.
Ensure accessibility features like proper labeling of input fields and buttons.

6. # Bonus Features
Multiple Ratings: Show ratings from different sources such as IMDb, Rotten Tomatoes, and Metacritic by accessing the Ratings array in the API response.
Poster and Trailers: Display movie posters and include links to movie trailers or YouTube searches.
Favorite/Watchlist: Allow users to mark movies as favorites or add them to a watchlist.

## Assumptions and Decisions

- Assumptions
# Assumption 1: User Input

Brief Description: We assume that users will provide the movie title in a reasonably correct format (spelling, order of words, etc.) for the search. Minor typos or errors may result in no results being returned, as the OMDb API does not support fuzzy search or spell check.


# Assumption 2: Availability of Data from OMDb API

Brief Description: We assume that the OMDb API will consistently return all relevant movie details such as box office collection, ratings, plot, runtime, and actors. However, in cases where certain fields (like box office or director information) are missing, we assume that the API response will provide "N/A" or handle empty fields gracefully.

# Decisions
Design Decision: User Interface Simplicity

The UI design prioritizes simplicity and clarity. A clean layout is used where users can search, view results, and filter by year without overwhelming them with too many advanced options. We decided not to clutter the UI with too many filters (such as genre, language, etc.) in the initial version to maintain ease of use.
Design Decision: Responsive Design

We decided to make the application responsive across different devices. This ensures that users on mobile, tablet, and desktop devices can all have a seamless experience. The layout automatically adjusts based on screen size, with elements stacked vertically on smaller screens and horizontally on larger ones.
Architectural Decision: Fetch API for Data Retrieval

The fetch() method is used to retrieve movie data from the OMDb API. We chose this over other methods (e.g., XMLHttpRequest) because of its simplicity, modern promise-based API, and better error-handling capabilities. It also allows for a cleaner asynchronous code structure with async/await.
Error Handling Design Decision

A key decision was to implement robust error handling for API requests. If the API fails to return data or if the user inputs an invalid title, a clear and informative error message will be displayed, rather than leaving the user with an empty or confusing interface.
Decision to Include Year Filter

We decided to include the year filter as an optional feature for users to refine their search. This helps users find specific versions of movies (e.g., remakes or different adaptations released in different years) and provides more accurate search results when dealing with common movie titles.
Data Structure Decision: Modular Handling of Movie Details

For better maintainability, the movie details are modularized into individual functions, such as displayMovieDetails(), making it easier to extend the application in the future. This allows us to add more features, such as additional details or advanced filters, without rewriting the core logic.

## Interaction
1. # Landing Page / Home Screen
Interaction:
When the user opens the application, they land on a simple home screen.
The central focus is a search bar where users can enter the movie title they wish to search for.
Beneath the search bar, there's an optional dropdown or input field where users can specify a year to filter the search results.
A "Search" button is present, allowing users to initiate the movie search.
Error Message Box: If the search yields no results or an error occurs, a clear error message will be displayed here.
Visual Elements:
A clean, minimal UI with input fields and buttons. Background imagery or subtle design elements related to movies (like movie reels, posters, etc.) can be used to enhance the look.

2. # Search Results Section
Interaction:
After hitting the search button, the application fetches data from the OMDb API.
The user sees a loading spinner or a placeholder while the results are being fetched to ensure they know the system is processing their request.
Once the API returns the data, the user is shown detailed information about the searched movie.
If multiple tabs or sections are present, they are dynamically updated with the movie data.

3. # Movie Details Section
Interaction:
Title and Poster: The movie title and poster are displayed at the top of the movie details section.
Key Details: Below the title and poster, detailed movie information is displayed in clear sections:
Box Office Collection: Displays the movie's box office earnings.
IMDB Rating: The IMDB rating, possibly alongside other ratings like Rotten Tomatoes or Metacritic.
Plot: A short description or plot summary of the movie.
Runtime: Displays how long the movie is.
Genre: Shows the genres the movie falls into (e.g., Drama, Action, Thriller).
Actors: A list of the main actors in the movie.
Director: The movie's director.
Interaction Options:
Users can click on an actor's name or director's name (if enabled) to perform a new search or view more information about that individual (e.g., linking to another API like Wikipedia or IMDB).
Additional Actions:
If implemented, users can add movies to a Favorites List or Watchlist by clicking on a button.
Users can click a "More Info" button to explore further details such as awards, language, country, etc.


4. # Filter by Year
Interaction:
Users can refine their search by entering or selecting a year.
When a user enters a movie title and year, the search results will only display movies from that specific year.
This feature is especially useful for searching remakes or movies with similar titles across different years.
If the year filter is applied, a "Clear Year Filter" button can appear to allow users to reset the search and view results from all years.

5. # Error Handling Section
Interaction:
If no movie is found or the user enters an invalid query, a user-friendly error message will be displayed in this section.
The error message might suggest tips like "Try refining your search" or "Make sure the title is spelled correctly."
Users can close or dismiss the error message easily and try a new search without reloading the page.


6. #  Responsive Design / Mobile Interaction
Interaction:
The application adapts to different screen sizes (mobile, tablet, desktop).
On smaller screens (like smartphones), the search bar and details section are stacked vertically to allow for easier scrolling.
Interactive elements like buttons, filters, and links are touch-friendly with appropriate padding to ensure a smooth experience on mobile devices.


7. # Optional: Tabs or Sections for Additional Features
If the application supports additional tabs or sections, users may navigate between different views:
Movie Overview Tab: Shows all major movie details like title, ratings, runtime, plot, etc.
Reviews Tab: Users can switch to a tab that pulls and displays reviews (if available through an API like IMDB or Rotten Tomatoes).
Similar Movies Tab: Displays similar movies based on the current search, allowing users to explore more content related to their interests.
Watchlist Tab: Shows a list of movies that the user has saved or favorited.

8. # Advanced Search Options (If Implemented)
Interaction:
The user might have the option to perform an advanced search, where they can add more filters like Genre, Actor, Director, or Language.
These advanced filters could be shown in a collapsible panel, allowing users to refine their search results for a more tailored experience.


9. # Dark Mode (Optional)

# Interaction:
A toggle switch can allow users to switch between light and dark mode.
This enhances the experience for users who prefer a darker UI or are using the app in low-light conditions.
Summary of User Interaction Flow:
Search: User enters a movie title in the search bar and optionally selects a year.
View Results: The search results (movie details) are displayed in various sections like Title, Plot, Box Office, Ratings, and Cast.
Error Handling: If no movie is found, a clear message is displayed.
Refine Search: The user can refine the search by entering a specific year or adding filters (if available).
Explore More: Users can interact with elements like actors, directors, or genres to explore more information.
Responsive Design: The app ensures seamless interaction across devices, including mobile and tablet.
This interaction model ensures that the user is constantly engaged while making the movie search experience straightforward, informative, and enjoyable.
## Screenshots


![Uploading Screenshot (59).png…]()

![Uploading Screenshot (60).png…]()

![Uploading image.png…]()

## API Key Configuration

- **Never hard-code your API key** in your JavaScript files. Instead, use environment variables or secure ways to handle them.
- For this project, ensure the API key is managed securely to prevent unauthorized usage.

## Technologies Used
- **HTML5, CSS3, JavaScript**: For building the frontend and UI interactions.
- **Bootstrap**: For responsive design and layout.
- **OMDb API**: To fetch and display movie-related data.
- **Git & GitHub**: For version control and repository management.
- 
## Documentation

[Documentation](https://linktodocumentation)


## Dependencies

- No external backend dependencies are required.
- Optional: Any local development server of your choice (e.g., Python, Node.js).
## Data Handling

- Movie data is fetched in real-time using the OMDb API.
- If data like box office earnings is unavailable from the OMDb API, future versions may integrate with additional APIs or make reasonable assumptions.
- Data is displayed in a clean and organized manner for an enhanced user experience.
## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)


## License

[MIT](https://choosealicense.com/licenses/mit/)


## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://www.polywork.com/harshvardhansingh_gaur)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/harshvardhaninghgaur)




## Support

For support, email gaurharsh5590@gmail.com or join our Slack channel.

