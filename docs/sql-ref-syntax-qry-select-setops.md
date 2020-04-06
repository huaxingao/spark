---
layout: global
title: Set Operators
displayTitle: Set Operators
license: |
  Licensed to the Apache Software Foundation (ASF) under one or more
  contributor license agreements.  See the NOTICE file distributed with
  this work for additional information regarding copyright ownership.
  The ASF licenses this file to You under the Apache License, Version 2.0
  (the "License"); you may not use this file except in compliance with
  the License.  You may obtain a copy of the License at
 
     http://www.apache.org/licenses/LICENSE-2.0
 
  Unless required by applicable law or agreed to in writing, software
  distributed under the License is distributed on an "AS IS" BASIS,
  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  See the License for the specific language governing permissions and
  limitations under the License.
---

Set operators are used to combine the results of two or more queries to a single result set. Spark supports three types od set operators:
- `EXCEPT` and `EXCEPT ALL`
- `INTERSECT` and `INTERSECT ALL`
- `UNION` and `UNION ALL`
Please note the queries' result sets must have the same number of columns and compatible data types for the respective columns.

### EXCEPT and EXCEPT ALL
`EXCEPT` and `EXCEPT ALL` return the row that are found in one query but not the other query. `EXCEPT` takes the distinct rows but `EXCEPT ALL` doesn't remove the duplicate.

#### Syntax
{% highlight sql %}
query EXCEPT [ ALL ] query
{% endhighlight %}

### INTERSECT and INTERSECT ALL
`INTERSECT` and `INTERSECT ALL` return the rows that are found in both queries. `INTERSECT` takes the distinct rows but `INTERSECT ALL` doesn't remove the duplicate.

#### Syntax
{% highlight sql %}
query INTERSECT [ ALL ] query
{% endhighlight %}

### UNION and UNION ALL
`UNION` and `UNION ALL` return the rows that are found in either query. `UNION` takes the distinct rows but `UNION ALL` doesn't remove the duplicate.

#### Syntax
{% highlight sql %}
query UNION [ ALL ] query
{% endhighlight %}

### Related Statement
- [SELECT](sql-ref-syntax-qry-select.html)