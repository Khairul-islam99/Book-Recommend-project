# Book Recommendation System

## Overview 📖

This is a Python-based **Book Recommendation System** that uses two approaches:

1. **Popularity-Based Recommendation System**: Recommends books based on their popularity (number of ratings and average rating).
2. **Collaborative Filtering**: Recommends books based on user rating patterns using a similarity matrix.

The system leverages datasets containing book information, user data, and user ratings to provide personalized and general book recommendations.

## Features ✨

- **Popularity-Based Recommendations**:
  - Recommends books that have been rated by a large number of users with high average ratings.
- **Collaborative Filtering**:
  - Uses cosine similarity to recommend books similar to a specific input book based on user rating patterns.

## Datasets 🗂️

This system uses the following datasets:

1. **Books.csv**: Contains details about books, including titles, authors, and image URLs.
2. **Users.csv**: Contains information about users.
3. **Ratings.csv**: Contains user ratings for books.

## Prerequisites 🛠️

- Python 3.7+
- Libraries:
  - `numpy`
  - `pandas`
  - `scikit-learn`

## Installation ⚙️

1. Clone the repository:
   ```bash
   git clone https://github.com/Khairul-islam99/book-recommendation-system.git
   ```
2. Navigate to the project directory:
   ```bash
   cd book-recommendation-system
   ```
3. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

## Example Usage 🚀

### Popularity-Based Recommendation 🌟

Run the system to recommend the top 5 most popular books:

```python
print(popular_df.head())
```

Example output:

```
        Book-Title       Book-Author                 Image-URL-M  num_ratings  avg_rating_df
0      Harry Potter     J.K. Rowling  http://example.com/image1   500         4.8
1  The Great Gatsby   F. Scott Fitzgerald  http://example.com/image2   300         4.7
2   Pride and Prejudice   Jane Austen  http://example.com/image3   280         4.6
```

### Collaborative Filtering Recommendation 🤝

Use the collaborative filtering model to recommend books similar to a given book:

```python
recommend("1984")
```

Example output:

```
Animal Farm
Brave New World
Fahrenheit 451
The Handmaid's Tale
Slaughterhouse-Five
```

## Example Books for Testing 📚

You can use the following book titles as inputs:

- "1984"
- "Harry Potter"
- "The Great Gatsby"
- "Pride and Prejudice"
- "To Kill a Mockingbird"

## How It Works 🧠

### 1. Data Loading and Cleaning

- Load datasets (`Books.csv`, `Users.csv`, `Ratings.csv`).
- Handle missing values and duplicate records.

### 2. Popularity-Based Recommendations

- Group books by their titles.
- Calculate the total number of ratings (`num_ratings`) and average ratings (`avg_rating_df`) for each book.
- Filter and recommend books with at least 250 and the highest average ratings.

### 3. Collaborative Filtering

- Create a pivot table with books as rows and users as columns, with values representing ratings.
- Fill missing ratings with zeros.
- Compute cosine similarity between books based on user rating patterns.
- Recommend the top 5 most similar books for a given book.

## Contributing 🤗

Feel free to fork this repository and contribute by submitting a pull request. Suggestions for improvements are welcome!


---

**Happy Reading!** 📚
