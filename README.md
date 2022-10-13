# TheMovieDB-API-Wrapper.js
A JavaScript library for easily fetching ALL info about movies / tv including (genres & actors) & more via TheMovieDB API. 


## Example usage

You can view a demo of the API wrapper in use [here.](https://marketingpipeline.github.io/Media-Element.js/demo)





	
 <br>
<details><summary>How to use <b>TheMovieDB-API-Wrapper.js</b>:</summary>
 <br>		
 
	
<br>	 
<br>	 
	
<details><summary>How to search up <b>Movie</b> info:</summary>
	
<br>	
	
You will require a API key from TheMovieDB and to define a variable called <code>TheMovieDB_APIKey</code> with your valid API key

A movie / film query name could look like the following example(s)

   
    Captain Russia
    Captain Russia (2014)
    Captain Russia The Summer Soldier (2014) 1080p BrRip x264 - YIFY
    
for more accurate results, a year should be provided in the query. 

	
	
### Usage
	 
   
When searching up a movie / film - any found media info & actor info  will be returned in seperated lists inside of a array. 


> Paramaters (Query [REQUIRED], Type [REQUIRED], Max Actors)


```js
 /// API WRAPPER USAGE EXAMPLE	
	
  // Valid API Key	
 var TheMovieDB_APIKey = "YOUR API KEY HERE"	
	
/// Both arrays (Media Info & Actors Info)
FetchDataFrom_TheMovieDB("8 Mile", "movie",  2).then(function(search_results) {
    console.log(search_results)
  });
  
/// Media Info Only
FetchDataFrom_TheMovieDB("8 Mile", "movie",  2).then(function(search_results) {
    console.log(search_results)[0]
  });  
  
/// Actor / Cast Info Only
FetchDataFrom_TheMovieDB("8 Mile", "movie",  2).then(function(search_results) {
    console.log(search_results)[1]
  });    
```



	
 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	
</details>
 <br>		
 
	
<br>	 
<br>	 
	
<details><summary>How to search up <b>TV Show</b> info:</summary>
	
<br>		
	
You will require a API key from TheMovieDB and to define a variable called <code>TheMovieDB_APIKey</code> with your valid API key
	
	
### Usage
	 

When searching up a TV show - any found media info & actor info will be returned in seperated lists inside of a array. 

A TV show query name could look like the following example(s)

   
    Captain Russia
    Captain Russia (2014)
    Captain Russia The Summer Soldier (2014) 1080p BrRip x264 - YIFY
    
for more accurate results, a year should be provided in the query. 


	
> Paramaters (Query [REQUIRED], Type [REQUIRED], Max Actors)


```js
  /// API WRAPPER USAGE EXAMPLE		
  // Valid API Key	
 var TheMovieDB_APIKey = "YOUR API KEY HERE"		
	
// Auto detecting name & year # from Torrent Name
FetchDataFrom_TheMovieDB("8 Mile 1080p BrRip x264 - YIFY", "movie",  2).then(function(search_results) {
    console.log(search_results)
  });
  
	
/// Both arrays (Media Info & Actors Info)
FetchDataFrom_TheMovieDB("8 Mile", "movie",  2).then(function(search_results) {
    console.log(search_results)
  });
  
/// Media Info Only
FetchDataFrom_TheMovieDB("8 Mile", "movie",  2).then(function(search_results) {
    console.log(search_results)[0]
  });  
  
/// Actor / Cast Info Only
FetchDataFrom_TheMovieDB("8 Mile", "movie",  2).then(function(search_results) {
    console.log(search_results)[1]
  });    
```



 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	
</details>


<br>		
 
	
<br>	 
<br>	 
	
<details><summary>How to show <b>Movie Collection</b> info:</summary>

<br>		
	
You will require a API key from TheMovieDB and to define a variable called <code>TheMovieDB_APIKey</code> with your valid API key


	
### Usage
	 

> Paramaters (Query [REQUIRED], Type [REQUIRED])


```js
  /// API WRAPPER USAGE EXAMPLE		
  // Valid API Key	
 var TheMovieDB_APIKey = "YOUR API KEY HERE"			
FetchDataFrom_TheMovieDB("Fast And Furious", "collection",  2).then(function(search_results) {
  console.log(search_results)
  });
```


 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	
</details>

<br>		
 
	
<br>	 
<br>	 
	
<details><summary>How to search up <b>Episode</b> info:</summary>
	
<br>		
	
You will require a API key from TheMovieDB and to define a variable called <code>TheMovieDB_APIKey</code> with your valid API key
	

	
### Usage

A episode info query could look like the following example(s)

   
    Captain Russia
    Captain Russia (2014)
    Captain Russia The Summer Soldier (2014) 1080p BrRip x264 - YIFY
    
<b>Note</b>: Season and Episode numbers will try to be auto-detected from query, tho they can be provided manually as parameters. If no season or episode name is found or provided, an error message will occur.  	
	
> Paramaters (Query [REQUIRED], Type [REQUIRED], Max Actors, Season, Episode)


```js
 /// API WRAPPER USAGE EXAMPLE		
  // Valid API Key	
 var TheMovieDB_APIKey = "YOUR API KEY HERE"		

// Auto detecting season & episode # from Torrent Name
FetchDataFrom_TheMovieDB("Two and a Half Men.S05E02", "episode",  2).then(function(search_results) {
    console.log(search_results)
  });
	
// Regular Name (with season and episodes as paramaters) 
FetchDataFrom_TheMovieDB("Two and a Half Men", "episode",  2, 5, 2).then(function(search_results) {
    console.log(search_results)
  });	
	
```



 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	
</details>


 <br>		
 
	
<br>	 
<br>	 
	
<details><summary>How to search up <b>Actor</b> info:</summary>
	
<br>	
	
You will require a API key from TheMovieDB and to define a variable called <code>TheMovieDB_APIKey</code> with your valid API key	
	
### Usage
	 

> Paramaters (Query [REQUIRED], Type [REQUIRED])

```js
/// API WRAPPER USAGE EXAMPLE		
  // Valid API Key	
 var TheMovieDB_APIKey = "YOUR API KEY HERE"		
FetchDataFrom_TheMovieDB("Eminem", "actor").then(function(search_results) {
  console.log(search_results)
  });
```



 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	 <br>	
</details>

####                                                                                                                    Options


<table>
<tr>
<th>Attribute</th>
<th>Meaning</th>
<th>Default</th>
<th>Required</th>
</tr>
<tr>
<td>query</td>
<td>The movie, TV show, actor or collection you would to search info for</td>
<td><code>undefined</code></td>
<td>Yes</td>
</tr>


<tr>
<td>type</td>
              <td>Type of query to search details for - options:<code>Movie, TV, Actor, Collection, Episode</code>.</td>
<td><code>undefined</code></td>
<td>Yes</td>
</tr>

<tr>
<td>max_actors</td>
<td>The maximum number of actor / cast members to return data for</td>
<td><code>5</code></td>
<td>No</td>
</tr>
	
<tr>
<td>season</td>
<td>The season number to search episode info for</td>
<td><code>undefined</code></td>
<td>No</td>
</tr>	

	
<tr>
<td>episode</td>
<td>The episode number to search episode info for</td>
<td><code>undefined</code></td>
<td>No</td>
</tr>	
	


</table>
	
	
</details>










## Contributing ![GitHub](https://img.shields.io/github/contributors/MarketingPipeline/Media-Element.js)

Want to improve this project? Create a pull request with detailed changes / improvements! If approved you will be added to the list of contributors of this awesome project!

See also the list of
[contributors](https://github.com/MarketingPipeline/Media-Element.js/graphs/contributors) who
participate in this project.

## License ![GitHub](https://img.shields.io/github/license/MarketingPipeline/Media-Element.js)

This project is licensed under the MIT License - see the
[LICENSE](https://github.com/MarketingPipeline/Media-Element.js/blob/main/LICENSE) file for
details.

