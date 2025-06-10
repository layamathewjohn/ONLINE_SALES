# ONLINE_SALES
SELECT 
  FORMAT_DATE('%B', Date) AS Month,
       COUNT(DISTINCT `Transaction ID`) AS Sales_Volume,
   ROUND(SUM(`Total Revenue`))AS MONTHLY_REVENUE,
FROM `my-project-as-intern.Online_sales.Sales`
WHERE Date BETWEEN '2024-01-01' AND '2024-12-31'
GROUP BY Month
ORDER BY Sales_Volume DESC,MONTHLY_REVENUE DESC;
