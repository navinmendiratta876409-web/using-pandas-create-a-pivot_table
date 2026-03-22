# using-pandas-create-a-pivot_table
import pandas as pd

data = {
    'City': ['Bharatpur', 'Jaipur', 'Bharatpur', 'Delhi', 'Jaipur', 'Bharatpur', 'Delhi'],
    'Brand': ['Samsung', 'Apple', 'Samsung', 'Apple', 'Samsung', 'Apple', 'Samsung'],
    'Sales_Amount': [15000, 80000, 16000, 85000, 15500, 75000, 14000]
}

df = pd.DataFrame(data)
report = df.pivot_table(index='City',columns = 'Brand',values='Sales_Amount',aggfunc="sum")
print(report)
