# CodeAlpha_EDA

# 1. Meaningful Questions
Do older customers spend more than younger ones?

Are there gender-based differences in purchase behavior?

Which product category generates the most revenue?

What payment method is most popular?

Are there unusually high or zero purchase amounts?

# 2. Data Structure

| **Column Name**     | **Data Type** | **Description**                                               |
|---------------------|---------------|---------------------------------------------------------------|
| `CustomerID`        | `int`         | Unique identifier assigned to each customer.                 |
| `Age`               | `int`         | Age of the customer in years.                                |
| `Gender`            | `object`      | Gender of the customer (e.g., Male, Female, Other).          |
| `PurchaseAmount`    | `float/int`   | Total amount spent in a single transaction.                  |
| `ProductCategory`   | `object`      | Category of the product purchased.                           |
| `PaymentMethod`     | `object`      | Mode of payment used (e.g., Credit Card, UPI).               |
| `PurchaseDate`      | `datetime`    | Timestamp of the transaction.                                |



# 3. Trends, Patterns & Anomalies
Trends: Electronics has high-value purchases.

Patterns: Younger users prefer UPI; older prefer Credit Card.

Anomalies: CustomerID 1007 made a ₹0 purchase (suspicious).

# 4. Hypotheses & Stats
H1: Men and women spend differently. → Use groupby('Gender')

H2: Average spend increases with age. → Use corr(Age, PurchaseAmount)

H3: Electronics = highest average purchase. → Use groupby('ProductCategory')

# 5. Data Quality Issues
Zero value in PurchaseAmount (likely error or return).

Small sample size → not generalizable.

No missing values in this case, but needs checking in real data.
