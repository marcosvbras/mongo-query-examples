# Using $group

To test all these examples, you will need to import **zips_dump** from [datasets](../datasets) directory. See how to import this one in [How to import and export databases](import.md).


Sum up the population (pop) by state and put the result in a field called population.

```js
db.locations.aggregate(
  [
    {
      $group: { _id: {state: "$state"}, population: {$sum: "$pop"} }
    }
  ]
)
```

Result:

```json
{ "_id" : { "state" : "CA" }, "population" : 29754890 }
{ "_id" : { "state" : "MT" }, "population" : 798948 }
{ "_id" : { "state" : "MS" }, "population" : 2573216 }
{ "_id" : { "state" : "FL" }, "population" : 12686644 }
{ "_id" : { "state" : "AR" }, "population" : 2350725 }
{ "_id" : { "state" : "GA" }, "population" : 6478216 }
{ "_id" : { "state" : "WA" }, "population" : 4866692 }
{ "_id" : { "state" : "SC" }, "population" : 3486703 }
{ "_id" : { "state" : "MN" }, "population" : 4372982 }
{ "_id" : { "state" : "NE" }, "population" : 1578139 }
{ "_id" : { "state" : "MD" }, "population" : 4781379 }
{ "_id" : { "state" : "TN" }, "population" : 4876457 }
{ "_id" : { "state" : "DE" }, "population" : 666168 }
{ "_id" : { "state" : "DC" }, "population" : 606900 }
{ "_id" : { "state" : "AZ" }, "population" : 3665228 }
{ "_id" : { "state" : "ME" }, "population" : 1226648 }
{ "_id" : { "state" : "OR" }, "population" : 2842321 }
{ "_id" : { "state" : "AL" }, "population" : 4040587 }
{ "_id" : { "state" : "PA" }, "population" : 11881643 }
{ "_id" : { "state" : "RI" }, "population" : 1003218 }
Type "it" for more
```
