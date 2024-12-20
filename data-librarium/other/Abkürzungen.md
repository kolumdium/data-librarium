```dataview
TABLE aliases FROM ""
WHERE (aliases != null)
AND (length(aliases) > 0) 
AND (length(aliases[0]) < 5)
```
