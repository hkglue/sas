# Grammar logic instructions {#concept_umr_4zc_zdb .concept}

The log query feature supports multiple search conditions. You can include multiple operators in a query on one log, or combine multiple queries on several logs based on different logic. This document describes the operators and keywords that are supported in log queries. Examples are provided to help you understand them.

The following operators and keywords are supported in log queries:

|Operator|Description|
|and|Binary operator. The format is `query1 and query2`. The result returns the records that match both  `query1` and `query2` .**Note:** When no operator has been specified among multiple words, the default operator `and` is used. 

|
|or|Binary operator. The format is `query1 or query2`. The result returns all records that match either `query1` or `query2`.|
|not|Binary operator. The format is `query1 not query2`. The result returns the records that match  `query1` but not `query2`, which is equivalent to `query1–query2`.**Note:** If only `not query1` is specified, the result returns all records that do not match `query1` .

|

