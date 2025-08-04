# Soundtrack Your Story

**Elevate your reading experience by generating the perfect musical soundtrack for any book.**

"Soundtrack Your Story" is a dynamic web application that connects the worlds of literature and music. By leveraging the Google Books and Spotify APIs, it intelligently curates custom playlists that match the genre, theme, and mood of your favorite books.


https://github.com/user-attachments/assets/dfab6826-211d-4e02-92eb-f06a1323d8c8


## 🎵 Project Overview

The primary objective of this project is to enhance the immersion of reading. Users can search for any book, and the application will:

1.  **Fetch Book Data:** Retrieve detailed information about the book, including its genres, from the Google Books API.
2.  **Generate AI Playlists:** Map the book's genres to musical genres and use Spotify's recommendation engine to create a unique, AI-generated playlist.
3.  **Discover Community Playlists:** Find and display existing public playlists on Spotify that other users have created for that book.

The result is a multi-sensory experience that brings stories to life through the power of music.

## 🌐 Live Demo

You can test the live version of the application here:

**[Test Soundtrack Your Story](https://sushants-codeandproject-hub.on.drv.tw/sound%20/sound_ff.html)**

Simply click the link to open the webpage and start searching for books.

## 🚀 Setup and Installation

To get this project running locally, you'll need to configure your own API keys for the Google Books and Spotify APIs.

### Step 1: Clone the Repository

First, clone the repository to your local machine:

```
git clone [https://github.com/your-username/soundtrack-your-story.git](https://github.com/your-username/soundtrack-your-story.git)
cd soundtrack-your-story
```

### Step 2: Obtain API Keys

This project requires three keys to function:

* **Google Books API Key:** Allows the app to search for books.
* **Spotify Client ID & Client Secret:** Allows the app to authenticate with Spotify and fetch music data.

1.  **Google Books API:**
    * Go to the [Google Cloud Console](https://console.cloud.google.com/).
    * Create a new project.
    * Go to "APIs & Services" > "Library" and enable the "Google Books API".
    * Go to "APIs & Services" > "Credentials" and create a new API Key.
2.  **Spotify API:**
    * Go to the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/).
    * Log in and create a new application.
    * You will find your `Client ID` and `Client Secret` in the app's dashboard.

### Step 3: Configure the Application

Once you have your keys, open the `sound.html` file in a text editor. Find the `CONFIG` object within the `<script>` tag at the bottom of the file and replace the placeholder values with your actual keys.

```javascript
// sound.html

const CONFIG = {
    GOOGLE_BOOKS_API_KEY: 'YOUR_GOOGLE_BOOKS_API_KEY', // <-- Paste your key here
    SPOTIFY_CLIENT_ID: 'YOUR_SPOTIFY_CLIENT_ID',       // <-- Paste your client ID here
    SPOTIFY_CLIENT_SECRET: 'YOUR_SPOTIFY_CLIENT_SECRET', // <-- Paste your client secret here
    // ... other config variables
};
```

**Note:** It is not recommended to expose API keys on the client-side in a production application. This setup is for demonstration and local development purposes.

## 📖 Usage Guidelines

Since this is a client-side application built with HTML, CSS, and vanilla JavaScript, there are no build steps required.

1.  **Open the File:** Simply open the `sound.html` file in any modern web browser (e.g., Chrome, Firefox, Safari).
2.  **Search for a Book:** In the search bar, type the title of a book or the name of an author and click the search button or press `Enter`.
3.  **Explore Soundtracks:** The application will display:
    * An **AI-generated playlist** of individual tracks that match the book's mood.
    * A list of **community-curated full playlists** from Spotify.
4.  **Listen:** You can preview all tracks and playlists directly on the page through the embedded Spotify players.

### Troubleshooting

* **"API credentials are missing" error:** Ensure you have correctly pasted your API keys into the `CONFIG` object in `sound.html`.
* **"No books found" error:** Try a different or more specific search query. The Google Books API may not have data on very obscure books.
* **Playlists not loading:** This may be due to an issue with the Spotify API or an invalid access token. Check your browser's developer console for specific error messages.

## 🙏 Acknowledgments and Licensing

This project was made possible by the fantastic APIs and tools provided by the following companies and communities.

* **Data Providers:**
    * [Google Books API](https://developers.google.com/books) for all literary data.
    * [Spotify Web API](https://developer.spotify.com/documentation/web-api/) for all music and playlist data.
* **Front-End Tools:**
    * [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS framework.
    * [Font Awesome](https://fontawesome.com/) for icons.
    * [Google Fonts](https://fonts.google.com/) for typography.

### License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details. You are free to use, modify, and distribute this project as you see fit.
