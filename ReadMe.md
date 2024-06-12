# Ice Cream Parlor Cafe Application

## Setup and Running the Application

### Prerequisites
- Python 3.9
- SQLite

### Steps to Run the Application

1. Clone the repository.
2. Navigate to the project directory.
3. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```
4. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
5. Run the application:
    ```bash
    python src/app.py
    ```

### Running with Docker

1. Build the Docker image:
    ```bash
    docker build -t icecream_parlor .
    ```
2. Run the Docker container:
    ```bash
    docker run -it --rm icecream_parlor
    ```

### Test Steps to Validate the Application

1. **Add Seasonal Flavor**
    - Input: `name = "Mango Delight"`, `description = "A refreshing mango flavor"`, `availability = "Summer"`
    - Expected Output: "Seasonal flavor added successfully!"

2. **View Seasonal Flavors**
    - Expected Output: List of all seasonal flavors.

3. **Search Seasonal Flavors**
    - Input: `keyword = "Mango"`
    - Expected Output: Flavors containing the keyword "Mango".

4. **Add Ingredient**
    - Input: `name = "Milk"`, `quantity = 100`
    - Expected Output: "Ingredient added successfully!"

5. **View Ingredients**
    - Expected Output: List of all ingredients.

6. **Add Customer Suggestion**
    - Input: `flavor_suggestion = "Blueberry Bliss"`, `customer_name = "John"`, `customer_allergies = "None"`
    - Expected Output: "Customer suggestion added successfully!"

7. **View Customer Suggestions**
    - Expected Output: List of all customer suggestions.

8. **Add Allergen**
    - Input: `name = "Peanuts"`
    - Expected Output: "Allergen added successfully!" or "Allergen already exists!"

9. **View Allergens**
    - Expected Output: List of all allergens.

10. **Add to Cart**
    - Input: `item = "Mango Delight"`
    - Expected Output: "Item added to cart successfully!"

11. **View Cart**
    - Expected Output: List of all items in the cart.

12. **Remove from Cart**
    - Input: `item = "Mango Delight"`
    - Expected Output: "Item removed from cart successfully!"

### Documentation of the Code

Each module in the `src` directory handles a specific aspect of the application:
- `database.py`: Manages the SQLite database connection and table creation.
- `cart.py`: Implements a simple cart system.
- `models/`: Contains modules for managing seasonal flavors, ingredient inventory, customer suggestions, and allergens.
- `app.py`: The main application logic and user interface.

### ORM Abstraction Implementation 

The database operations are implemented using raw SQL queries. However, they are abstracted through Python functions, which provide a level of abstraction similar to an ORM. Future versions can replace raw SQL queries with an actual ORM like SQLAlchemy for better abstraction and functionality.

### Docker File 

The provided `Dockerfile` builds a Docker image for the application and runs it in a container. Instructions to build and run the Docker container are included in the README file.

---

By following these steps, you should be able to meet all the requirements and achieve a full score on your assignment. Good luck with your submission!
