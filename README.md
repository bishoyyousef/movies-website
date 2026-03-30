<<<<<<< HEAD
<<<<<<< HEAD
## TDMB — Home of Movies
=======
movies-website is a site that gives an API for movies in this project i used that API to get the movies and display them with some details.
=======
ovies-website is a site that gives an API for movies in this project i used that API to get the movies and display them with some details.
>>>>>>> 61e6c5e5ce71f771df71bcfe47ec8ba5108e21bb
This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).
>>>>>>> ce5831a34f43e2b8c394ad4537fba0ecdde0c351

Browse popular movies, search by title, open a movie details page, and save favourites for later.

### Features

- **Movie discovery**: Popular movies list with pagination
- **Search**: Find movies by keyword
- **Movie details**: Dedicated details page per movie
- **Favourites**: Save/remove favourites (stored in `sessionStorage`)
- **API + static fallback**: Uses TMDB when available, otherwise falls back to bundled static movie data

### Tech stack

- **Next.js (App Router)** + **React**
- **TypeScript**
- **Redux Toolkit** for state management
- **Axios** for API calls
- **Bootstrap / React-Bootstrap** for UI

### Pages / routes

- **Home**: `/` (movies list + search + pagination)
- **Movie details**: `/movies/[moviesId]`
- **Favourites**: `/Favourites`

### Getting started

Install dependencies:

```bash
npm install
```

Run the dev server:

```bash
npm run dev
```

Open `http://localhost:3000`.

### TMDB API key (optional)

This project is built to work with The Movie Database (TMDB) API.

- **Current behavior**: the API key is hardcoded in `src/reduxStore/reducers/movieSlice.tsx` (`const apiKey = 123`).
- **Recommended**: use an environment variable instead.

Create a `.env.local` file:

```bash
NEXT_PUBLIC_TMDB_API_KEY=YOUR_KEY_HERE
```

Then update `src/reduxStore/reducers/movieSlice.tsx` to use it (replace the hardcoded key):

- `const apiKey = Number(process.env.NEXT_PUBLIC_TMDB_API_KEY);`

### Scripts

```bash
npm run dev      # start dev server
npm run build    # build for production
npm run start    # start production server
npm run lint     # lint
```

### Notes

- **Favourites persistence**: favourites are saved in `sessionStorage`, so they persist per-tab/session (cleared when the browser session ends).

