# Monthly Sales Analyzer

In this project, you will take on the role of a data analyst responsible for evaluating the sales performance of three products over a month. To do this, you will work with a dataset structured as a list of dictionaries, where each entry represents the daily sales of each product. Your task is to complete several Python functions that will allow you to calculate totals, averages, identify the most and least successful days, and analyze sales trends. As you complete each function, you will strengthen your data manipulation and programming logic skills, preparing yourself for future data science projects.

<how-to-start>
   
### 🌱 How to start this project

Follow these instructions:

1. Clone or fork this repository: [matthewkane-ml/MonthlySalesAnalyzer_MTK](https://github.com/matthewkane-ml/MonthlySalesAnalyzer_MTK).
2. Open the newly created repository in Codespace using the [Codespace button extension](https://docs.github.com/en/codespaces/developing-in-codespaces/creating-a-codespace-for-a-repository#creating-a-codespace-for-a-repository).
3. Once the VSCode in Codespace has finished opening, start your project by following the instructions below.

</how-to-start>


## 📝 Instructions

You have been provided with a Python file (`monthly_sales_analyzer.py`) that contains sales data for a month for three products over 20 days. Your task is to complete the empty functions to analyze this data using basic Python skills: loops, conditionals, and data structures. This project will assess your ability to process and extract information from a dataset, preparing you for data science concepts.


- The data is stored in a variable called `sales_data`, a list of 20 dictionaries. Each dictionary represents a day and has:
   - `"day"`: Day number (1 to 20).
   - `"product_a"`: Sales of Product A.
   - `"product_b"`: Sales of Product B.
   - `"product_c"`: Sales of Product C.

Example: 

```python
{"day": 1, "product_a": 150, "product_b": 80, "product_c": 200}
```

- Complete the five placeholder functions in the file. 

- Each function analyzes the `sales_data` in a specific way. Use only basic Python, no external libraries. The file includes `print` statements to test your work.

#### Functions to Complete:  
- **`total_sales_by_product(data, product_key)`:** Calculate the total sales of a given product (e.g., `"product_a"`) over 20 days.


- **`average_daily_sales(data, product_key)`:** Calculate the average daily sales of a given product.


- **`best_selling_day(data)`:** Find the day with the highest total sales (sum of the three products).

- **`days_above_threshold(data, product_key, threshold)`:** Count how many days the sales of a product exceeded a given threshold (e.g., 18).

- **`top_product(data)`:** Identify which product (A, B, or C) had the highest total sales.

- To test your code, run the following command in the command line:

   ```bash
   python3 monthly_sales_analyzer.py
   ```

## Feeling confident? 😎:  
- Add a function to find the day with the worst sales.
- Sort the days by total sales and show the top 3.
- Calculate the range (maximum - minimum) of the sales of a product.

  
In the end, you will have practiced handling a realistic dataset with basic Python, developing skills for your next data science course. 

Have fun analyzing!🚀


## 🚛 How to deliver this project

Once you complete the exercises, follow these steps to submit them correctly:  

1. **Save and commit the changes** in your local repository:  

   ```sh
   git add .
   git commit -m "Completed exercises"
   ```
2. Push the changes to GitHub with:

   ```sh
   git push origin main
   ```
3. Ensure your repository is up to date on GitHub.
