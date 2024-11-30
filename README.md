# Book Recommendation System

This project implements a book recommendation system using collaborative filtering with k-nearest neighbors (kNN). It analyzes user ratings and suggests books based on similarity scores, helping users discover new books they may enjoy. The system utilizes a user-item matrix and cosine similarity to find similar books.

## Features

- **Collaborative Filtering**: Recommends books based on user preferences using the k-nearest neighbors (kNN) algorithm.
- **Cosine Similarity**: Calculates similarity between books using cosine similarity on the user-item matrix.
- **User and Book Mapping**: Maps user IDs and book ISBNs to indices for matrix representation.
- **Recommender Output**: Given a book, the system suggests the most similar books that users might like.

## How It Works

1. **Data Loading and Preprocessing**:  
   - The `Ratings.csv` and `Books.csv` files are loaded using pandas.
   - The user-item matrix is constructed by mapping user IDs and book ISBNs to indices.
   - Data is preprocessed to fit the collaborative filtering model.

2. **k-Nearest Neighbors Model**:  
   - The kNN algorithm is used to find books that are most similar to the input book based on user ratings.
   - Cosine similarity is calculated to measure similarity between books.

3. **Recommendation Function**:  
   - Given a book ID, the `find_similar_books()` function returns a list of the top-k most similar books.

4. **Testing and Visualization**:  
   - The system recommends similar books for a given input book.
   - The output includes a list of recommended books based on similarity scores.

## Model Architecture

The recommendation system uses the following structure:

- **User-Item Matrix**:
  - Constructed using the ratings provided by users for different books.
  - The matrix is sparse, with the rows representing books and columns representing users.
  
- **kNN Algorithm**:
  - A k-nearest neighbors model is trained on the user-item matrix.
  - Cosine similarity is used to measure similarity between books.

## Results

The system successfully recommends books based on user ratings. Given a book, the model can find similar books that other users with similar tastes have rated highly. The recommended books are displayed in order of similarity.

## Conclusion

The project demonstrates the use of collaborative filtering and k-nearest neighbors to build a book recommendation system. By utilizing cosine similarity on a user-item interaction matrix, the system is able to recommend books based on similar user preferences. This approach can be extended to other domains where user preferences can be quantified, offering an effective way to suggest relevant items to users.
