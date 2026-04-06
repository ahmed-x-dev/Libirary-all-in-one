# Library All-in-One

A desktop application for managing a personal media library with a focus on movies and series. Built with PySide6 and SQLite, with a schema that can be extended to games, books, and comics/manga.

## Project Status
This project is currently inactive/abandoned and not under active maintenance.

## Key Features
- Add, edit, delete, and move items between sections.
- Sections: Watching, Want to Watch, Continue Later, Don’t Want to Continue, Watched.
- Search, sort, and random pick for quick discovery.
- List or grid view with per-section preferences.
- Metadata auto-fill via TMDB and OMDb.
- Detailed item view with cast, ratings, posters, and trailers.
- Optional Google Drive sync (disabled by default).

## Tech Stack
- Python 3.10+
- PySide6
- SQLite
- requests, beautifulsoup4
- google-auth, google-auth-oauthlib, google-api-python-client (optional)

## Installation
1. `git clone https://github.com/a8392280-web/Libirary-all-in-one.git`
2. `cd Libirary-all-in-one`
3. (Optional) Create and activate a virtual environment.
4. Install dependencies: `pip install PySide6 requests beautifulsoup4 google-auth google-auth-oauthlib google-api-python-client`
5. Configure API keys in `config.py`.
6. Run the app: `python main.py`

## Configuration
Edit `config.py` and provide your own keys:
- `TMDB_API_KEY` and `OMDB_API_KEY` are required for metadata search and auto-fill.
- `MY_ANIME_LIST` and `RAWG_API_KEY` are included for future features.

## Data Storage
- Local SQLite database at `data/movies.db`.
- Schema defined in `app/db/sqlite_manger.py`.

## Optional Features
- Google Drive sync is implemented but commented out in `main.py`. See `app/sync/drive_sync.py`.
- Watch-link scrapers are included for movies and may be region-specific or unstable.

## Feature Coverage
- Movies and series are fully supported in the UI.
- Games, books, and comics/manga tables exist in the database but do not yet have full UI support.

## License
You are free to:
- Use, copy, modify, and distribute this project.
- Build new apps based on it.

Requirements:
- Always give credit to the original author.
- If you make improvements or fixes, please submit them as a Pull Request to the original repository.
- You may not claim this project as entirely your own.
