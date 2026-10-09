# Book Recommendation System

A command-line book recommender written in Python (standard library only, no installs needed).

## Features
- **Search books** by title, author, genre or keyword
- **Select genre and author** to get ranked recommendations
- **Similar books**: pick a book you like and get matches
- **Ratings & details**: star rating, year, pages and description
- **Top rated** list

## Project Structure
```
book-recommender/
├── book_recommender.py   # main program
├── books.csv             # sample dataset (30 books)
└── README.md
```

## Requirements
- Python 3.8+

## How to Run
```bash
cd book-recommender
python book_recommender.py
```

## Example
```
===== Book Recommendation System =====
1. Search books
2. Recommend by genre / author
...
Choose an option: 2

Select a genre:
  0. Any
  1. Dystopian
  2. Fantasy
  ...
```

## How Recommendations Work
Each book gets a score:
- +2.0 if the author matches your selection
- +1.0 if the genre matches
- + rating / 5 as a tie-breaker

"Similar books" also compares authors, genres and shared description keywords.

## Adding Your Own Books
Add rows to `books.csv` using the same columns:
`id,title,author,genre,year,rating,pages,description`

Ratings in the sample data are approximate and for demonstration only.

## Ideas for Extension
- Save user favorites and ratings
- TF-IDF / cosine-similarity recommendations (scikit-learn)
- Fetch live data from the Open Library or Google Books API
- Add a GUI (Tkinter) or web UI (Flask)
