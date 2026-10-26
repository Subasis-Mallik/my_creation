# my_creation
this my third repo
from- odisha
<br>
Name- Subasis

SELECT
    c.AcquisitionChannel,
    COUNT(DISTINCT c.CustomerID) AS CustomerCount,
    SUM(t.TransactionAmount) AS TotalSpending,
    AVG(t.TransactionAmount) AS AverageTransaction
FROM Customers c
JOIN CreditCards cc
    ON c.CustomerID = cc.CustomerID
JOIN Transactions t
    ON cc.CardID = t.CardID
GROUP BY c.AcquisitionChannel
ORDER BY TotalSpending DESC;
