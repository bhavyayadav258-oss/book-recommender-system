# Book Recommender System

Simple Flask app that shows the top books and recommends similar books by title.

## What this project contains
- Main app: [`app.py`](app.py) — contains the Flask app and routes:
  - [`app.index`](app.py) — shows the top 50 books on [templates/index.html](templates/index.html)
  - [`app.recommend_ui`](app.py) — displays the recommendation form on [templates/recommend.html](templates/recommend.html)
  - [`app.recommend`](app.py) — computes and returns similar books based on user input
- Templates:
  - [templates/index.html](templates/index.html) — top books view
  - [templates/recommend.html](templates/recommend.html) — recommendation form and results
- A simple placeholder HTML: [html.html](html.html)

Data files required by the app (pickle files loaded in [`app.py`](app.py)):
- `popular.pkl` — dataframe with top books used on the homepage
- `pt.pkl` — pivot table (used for lookup)
- `books.pkl` — books dataframe with metadata (title, author, image)
- `similarity_scores.pkl` — similarity matrix used for recommendations

Place these pickle files in the project root so the app can load them.

## How to run (simple)
1. Create a virtual environment and install Flask and numpy (and pandas if used to create the pickles):
   ```sh
   pip install flask numpy