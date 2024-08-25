```dataview
table School
from "4. Archieve/학교"
sort Final desc
```

```dataview
table ETS, GRE, subject, Treport, Due_Date as 마감일
from "4. Archieve/학교" where final="ok"
sort Final desc
```
