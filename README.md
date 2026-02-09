# congenial-octo-giggle
SELECT r.RiderName, COUNT(*) AS Wins
FROM Riders r
JOIN RaceResults rr ON r.RiderID = rr.RiderID
WHERE rr.Position = 1
GROUP BY r.RiderName
ORDER BY Wins DESC;
