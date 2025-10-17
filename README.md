Of course. Here is the updated `README.md` file based on your new brief.

---

# Product Sales Dashboard

## Summary

This is a lightweight, client-side web application designed to parse and display sales data from a `data.csv` file. The dashboard presents two key metrics: a prominent display of the total gross sales and a detailed breakdown of total sales for each individual product, presented in a clean, responsive Bootstrap table.

The application is built with vanilla JavaScript, HTML, and Bootstrap 5 for styling. It dynamically processes the CSV data upon page load to ensure the displayed information is always up-to-date with the source file.

## Setup

No complex build process or dependencies are required. All you need is a modern web browser.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd your-repo-name
    ```

3.  **Run a local server:**
    To avoid potential CORS issues when fetching the `data.csv` file, you should serve the files from a local web server. A simple way to do this is with Python:

    *If you have Python 3 installed:*
    ```bash
    python -m http.server
    ```
    *If you have Python 2 installed:*
    ```bash
    python -m SimpleHTTPServer
    ```
    Alternatively, you can use a tool like the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension for VS Code.

4.  **Open in your browser:**
    Navigate to `http://localhost:8000` (or the port specified by your local server).

## Usage

Upon loading the `index.html` page, the application's JavaScript will automatically perform the following actions:

1.  **Fetch and Parse Data:** It reads the contents of the `data.csv` file. The CSV is expected to have columns such as `product_name`, `price`, and `quantity`.

2.  **Calculate Total Sales:** It iterates through all records to calculate the grand total of all sales. This value is then rendered into the HTML element with the ID `#total-sales`.

3.  **Generate Product Sales Table:** The script aggregates sales data for each unique product. It then dynamically generates and populates a Bootstrap table with the ID `#product-sales`, where each row contains a product's name and its calculated total sales.

The application is designed to be seamless; both the `#total-sales` element and the `#product-sales` table are populated during the same data processing phase, ensuring data consistency across the dashboard.

To use your own data, simply modify or replace the `data.csv` file, ensuring it maintains a consistent column structure.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.