# CodeAlpha_EDA

✅ 2. Meaningful Questions
Do older customers spend more than younger ones?

Are there gender-based differences in purchase behavior?

Which product category generates the most revenue?

What payment method is most popular?

Are there unusually high or zero purchase amounts?

🔍 3. Data Structure
Column Name	Data Type
CustomerID	int
Age	int
Gender	object
PurchaseAmount	float/int
ProductCategory	object
PaymentMethod	object
PurchaseDate	datetime

📊 4. Trends, Patterns & Anomalies
Trends: Electronics has high-value purchases.

Patterns: Younger users prefer UPI; older prefer Credit Card.

Anomalies: CustomerID 1007 made a ₹0 purchase (suspicious).

📈 5. Hypotheses & Stats
H1: Men and women spend differently. → Use groupby('Gender')

H2: Average spend increases with age. → Use corr(Age, PurchaseAmount)

H3: Electronics = highest average purchase. → Use groupby('ProductCategory')

⚠️ 6. Data Quality Issues
Zero value in PurchaseAmount (likely error or return).

Small sample size → not generalizable.

No missing values in this case, but needs checking in real data.
