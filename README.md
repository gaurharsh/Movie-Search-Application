
# Movie Search Application

Project Overview
The Movie Search Application is a web application that fetches and displays movie data from the OMDb API. The goal is to allow users to search for movies by title and filter results by year, while presenting movie information such as ratings, box office collections, plot, and more in a user-friendly UI.


## Technologies Used
- **HTML5, CSS3, JavaScript**: For building the frontend and UI interactions.
- **Bootstrap**: For responsive design and layout.
- **OMDb API**: To fetch and display movie-related data.
- **Git & GitHub**: For version control and repository management.
## Features
- Search for movies by title using the OMDb API.
- Display detailed movie information: box office collection, ratings, plot, runtime, genre, actors, director, etc.
- Filter movies by year for refined search results.
- Handle API responses and errors gracefully.
- Responsive and user-friendly UI.
## Setup and Installation
 A web browser (Google Chrome, Mozilla Firefox, etc.).
- [Git](https://git-scm.com/) installed on your machine.
- API key from the [OMDb API](http://www.omdbapi.com/apikey.aspx).
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

## Dependencies

- No external backend dependencies are required.
- Optional: Any local development server of your choice (e.g., Python, Node.js).
## API Key Configuration

- **Never hard-code your API key** in your JavaScript files. Instead, use environment variables or secure ways to handle them.
- For this project, ensure the API key is managed securely to prevent unauthorized usage.

## Data Handling

- Movie data is fetched in real-time using the OMDb API.
- If data like box office earnings is unavailable from the OMDb API, future versions may integrate with additional APIs or make reasonable assumptions.
- Data is displayed in a clean and organized manner for an enhanced user experience.
## Assumptions & Notes

- The project assumes that basic movie details like title, year, and ratings will be available for all movies.
- Any missing data is handled gracefully and does not break the user interface.
## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)


## Appendix

Any additional information goes here


## Documentation

Full project documentation is available in the [GitHub Wiki](https://github.com/gaurharsh/Movie-Search-Application/wiki).


## Support

For support, email gaurharsh5590@gmail.com or join our Slack channel.


## License

[MIT](https://choosealicense.com/licenses/mit/)


## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://www.polywork.com/harshvardhansingh_gaur)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/harshvardhaninghgaur)



