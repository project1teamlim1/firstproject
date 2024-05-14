# firstproject

# 연령대별 ___별 예약률
SELECT
	case
	when age < 30 then '20s'
	when age < 40 then '30s'
	when age < 50 then '40s'
	when age < 60 then '50s'
	ELSE '60s+'
	END AS age_group,
	country_destination, #원하는 컬럼으로 변경
	COUNT(1) AS cnt
FROM train
GROUP BY 1, 2
ORDER BY 1,2
