# Album Tracker

Album Tracker is a React web app for discovering music albums and keeping a
personal listening log. You can search albums and artists, play 30-second
previews, save albums with a status, star rating, and notes, and get
LLM-powered recommendations based on your saved albums and ratings.

**Live site:** https://album-tracker-m8mx.vercel.app

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/859a2f98-312c-479c-a12f-ebb1fcb66554" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a59d245c-462a-414e-b41b-76886c37938a" />


## Features

- Search albums and artists with the iTunes Search API
- Album page with cover, year, genre, and track list
- 30-second track previews with a mini player (play/pause, previous/next, seek bar) that keeps playing while you browse
- Save albums to a personal collection with a status (Want to listen, Listening, Listened), a 1-5 star rating, and notes
- Filter and sort the collection
- Collection persists in the browser with localStorage
- Optional full-album playback through the Deezer player when a match exists
- LLM-powered recommendations based on the user's saved albums and ratings

## Tech Stack

React, Vite, Context API, iTunes Search API, Deezer, Google Gemini, Vercel

## Run Locally

1. Clone the repository and open the project folder.
2. Install the packages:

   ```
   npm install
   ```

3. Create a file named `.env.local` in the project root (next to `package.json`) and add your Gemini API key:

   ```
   GEMINI_API_KEY=your-key-here
   ```

4. Start the app:

   ```
   npm run dev
   ```

5. Open the address the terminal prints (usually http://localhost:5173) in Chrome or Edge.

## Limitations

- Previews are only 30 seconds, because that is all the iTunes API provides.
- The collection is saved only in your browser (localStorage), so it does not sync between devices.
- Full Deezer playback needs you to be logged in to Deezer, and may depend on your plan and country.
- Recommendations depend on the Gemini API, which can be busy or rate limited.

## Privacy Note

The recommendations feature sends the titles, artists, star ratings, and
statuses of your saved albums to Google's Gemini API. Your notes are not sent.
This is LLM-powered recommendations based on the user's saved albums and
ratings. No recommendation model was trained for this project.

## Disclaimer

This is a learning project and is not affiliated with Apple, Spotify, Deezer,
or Google. Music data, artwork, and audio belong to their owners.
