Data transformation allows the user to get back a specific part of a data set from a larger data set. Different methods like forEach, filter, map, and reduce are used to aid the user in retrieving the data they want. A good example of how this is used, is when a user is given a data set through an api; the user can make a webpage using only the data they want to see.

The forEach method allows the user to invoke a function of each element in the dataset with no specific purpose.
Example:
[1,2,3].forEach(function(value){
  console.log(value);
});

The filter method is used for extracting items of a specific value.
Example:
[12, 5, 8, 130, 44].filter(function(value) {
  return value >= 10;
})
(the following is returned) [12, 130, 44]
The above example can be used using the 'fat arrow' syntax.
[12, 5, 8, 130, 44].filter(value => value >= 10)
(returns) [12, 130, 44]

The map method is used to create array by manipulating each value in the array.
Example:
["IOS", "Java"].map((word) => word + " sucks!")
(returns) ["IOS sucks!", "Java sucks!"]

The reduce method can transform an entire array to a single value.
Example:
var tempsSatsinAugust = [98, 90, 103, 99];
tempsSatsinAugust.reduce((temp, i) => temp + i)/arr.length;
(returns) 97.5

In addition to the methods being very useful on their own, the user can chain multiple methods together. For example given a data set of cars and prices, the user can filter just sedans, then reduce to find the average price of a sedan.
Example:
[car-data].filter((car) => car.type.includes("sedan")).reduce((price, i) => price + i)/[car-data].length
