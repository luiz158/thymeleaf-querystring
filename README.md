# Thymeleaf - module for manipulating query strings

The `#qs` expression object provides many useful query string manipulation methods and 
is designed to work with spring mvc `PagingAndSortingRepository`. See Features.

This module follows the same conventions as `#temporals` from the [temporals extras module](https://github.com/thymeleaf/thymeleaf-extras-java8time).

# Docs

The supplied java doc contains all available methods with detailed usage examples.

[View Java Docs](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html)

Full IDE support using intellij.

# Licence

This software is licensed under the [Apache License 2.0](https://github.com/mjstewart/thymeleaf-querystring/blob/master/LICENSE).

# Requirements (3.0.x)
- Java 8
- Thymeleaf 3.0.0+

# Maven info

This library is not on maven central yet so you will need to build the jar and manually add it to the project.
For convenience, I have already built the latest jar so you can download directly or clone and copy.

# Installation

If using Spring Boot, simply add a `QueryStringDialect` bean. 

```$java
@SpringBootApplication
public class MyApplication {

	public static void main(String[] args) {
		SpringApplication.run(MyApplication.class, args);
	}

	@Bean
	public QueryStringDialect queryStringDialect() {
		return new QueryStringDialect();
	}
}
```

# Tutorials

[![Youtube demo](https://github.com/mjstewart/thymeleaf-querystring/blob/master/video-thumb.png)](https://www.youtube.com/playlist?list=PL3YkDUcLBd9-5qsfWb5moY9e_iqU6ylm3 "Youtube demo")

[Example code used in video](https://github.com/mjstewart/hotel-reservation-springmvc/blob/master/src/main/resources/templates/hotel/hotels.html)

# Features

### Popular
- [Add key value pair](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#add-java.lang.String-java.lang.String-java.lang.String-)
- [Add many key value pairs](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#addAll-java.lang.String-java.util.List-)
- [Get a keys value](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#getFirstValue-java.lang.String-java.lang.String-)
- [Get every value associated to a key](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#getAllValues-java.lang.String-java.lang.String-)
- [Remove single key](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#removeFirst-java.lang.String-java.lang.String-)
- [Remove all keys](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#removeAll-java.lang.String-java.util.List-)
- [Remove key matching value](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#removeKeyMatchingValue-java.lang.String-java.lang.String-java.lang.String-)
- [Remove any key matching value](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#removeAnyKeyMatchingValue-java.lang.String-java.lang.String-)
- [Remove all and add](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#removeAllAndAdd-java.lang.String-java.util.List-java.util.List-)
- [Remove nth occurrence](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#removeNth-java.lang.String-java.lang.String-int-)
- [Remove first N values](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#replaceN-java.lang.String-java.lang.String-java.util.List-)
- [Replace existing value](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#replaceFirst-java.lang.String-java.lang.String-java.lang.String-)
- [Replace nth occurrence](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#replaceNth-java.lang.String-java.util.Map-)
- [Update a numeric value](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#adjustFirstNumericValueBy-java.lang.String-java.lang.String-int-)

### Spring mvc helpers

- [Increment page number](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#incrementPage-java.lang.String-int-)
- [Decrement page number](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#decrementPage-java.lang.String-)
- [Reset page number to 0](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#resetPageNumber-java.lang.String-)
- [Set page number](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#setPageNumber-java.lang.String-java.lang.String-)
- [Get page number](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#getPageNumber-java.lang.String-)
- [Toggle sort direction](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#toggleSortDefaultDesc-java.lang.String-java.lang.String-)
- [Get sort direction](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#getCurrentSortDirectionDesc-java.lang.String-java.lang.String-)
- [Is field sorted?](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#isFieldSorted-java.lang.String-java.lang.String-)
- [Set sort direction](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#setSortDirectionDesc-java.lang.String-java.lang.String-)
- [Keep sort field, remove the rest](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#keepSortField-java.lang.String-java.lang.String-)
- [Create new sort](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#createNewSort-java.lang.String-java.util.List-)
- [Conditional values on sort direction](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#valueWhenMatchesSortDesc-java.lang.String-java.lang.String-java.lang.String-java.lang.String-)
- [Table column sorting](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html#fieldSorterDesc-java.lang.String-)


### More
See [Docs](https://mjstewart.github.io/thymeleaf-querystring/com/github/mjstewart/querystring/expression/QueryStringHelper.html) for additional methods.


# Examples

Complete example showing how to implement a table with paging and sorting plus conditional css and tooltips
. [View](https://github.com/mjstewart/hotel-reservation-springmvc/blob/master/src/main/resources/templates/hotel/hotels.html#L21)

The hotel name on [Line 30](https://github.com/mjstewart/hotel-reservation-springmvc/blob/master/src/main/resources/templates/hotel/hotels.html#L30)
is sorted using `fieldSorterAsc` since ascending is assumed the default sort direction according to whatever the spring 
`PagingAndSortingRepository` configuration is for this field. This means the first toggle will change direction to descending.

The next field `stars` on line 40 is sorted using `fieldSorterDesc` since the default sort direction is descending resulting in the first toggle
changing the sort direction to ascending.

The semantics for `cssWhenFieldIsAsc` and `valueWhenMatchesSortDesc` work the same in terms of how to read what the 
trailing `Asc` or `Desc` does. See docs for full examples.
