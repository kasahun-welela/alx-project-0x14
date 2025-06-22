## API overview
Collection of information for movies, TV shows, and actors. Includes YouTube trailer URL, awards, full biography, and many other useful information

<b>Key features:</b>
 <ul>
   <li >Fetch movies by title, genre, and year></li>
   <li> Supports pagination and sorting</li>
   <li> Rich metadata including posters, descriptions, and ratings</li>
   <li> Fast, scalable access via authenticated requests
</li>
</ul>

## API version 
  V1
  
 ## Available Endpoints
 
<ul>
  <li><strong>GET /titles</strong> – Fetch a list of movies or series, with optional filtering (e.g., genre, year, etc.)</li>
  <li><strong>GET /titles/{id}</strong> – Get detailed information about a specific movie or show by ID</li>
  <li><strong>GET /titles/{id}/ratings</strong> – Get rating information for a specific title</li>
  <li><strong>GET /titles/{id}/aka</strong> – Fetch alternate titles (AKAs) for a specific title ID</li>
  <li><strong>GET /titles/x/titles-by-ids</strong> – Fetch multiple titles by an array of IDs</li>
  <li><strong>GET /titles/series/{seriesId}</strong> – Get general information about a TV series by its series ID</li>
  <li><strong>GET /titles/series/{seriesId}/{season}</strong> – Get season-specific information for a TV series</li>
  <li><strong>GET /titles/seasons/{seriesId}</strong> – Retrieve all seasons for a given series ID</li>
  <li><strong>GET /titles/episode/{id}</strong> – Get information about a specific TV episode by its ID</li>
  <li><strong>GET /titles/x/upcoming</strong> – Get a list of upcoming movies or TV shows</li>
  <li><strong>GET /titles/random</strong> – Fetch a random movie or TV title</li>
</ul>



## Request and Response Format

```javascript
const url = 'https://moviesdatabase.p.rapidapi.com/actors/random';
const options = {
	method: 'GET',
	headers: {
		'x-rapidapi-key': API-Key,
		'x-rapidapi-host': 'moviesdatabase.p.rapidapi.com'
	}
};

try {
	const response = await fetch(url, options);
	const result = await response.text();
	console.log(result);
} catch (error) {
	console.error(error);
}
```

## Sample Response: Main Actors for a Title

The following is a sample JSON response returned from the `/titles/{id}/main_actors` endpoint:

```json
{
  "entries": 10,
  "results": [
    {
      "nconst": "nm9001698",
      "primaryName": "Muireann McSherry",
      "birthYear": "\\N",
      "deathYear": "\\N",
      "primaryProfession": "actress",
      "knownForTitles": "tt6904122"
    },
    {
      "nconst": "nm9001699",
      "primaryName": "Seán ÓhEacháin",
      "birthYear": "\\N",
      "deathYear": "\\N",
      "primaryProfession": "actor",
      "knownForTitles": "tt6904122"
    },
   
    ]}
```

## Authentication
   X-RapidAPI-Key: API key
   
## Error Handling
401 - unauthorized \n
500 - server error

 ## Usage Limits and Best Practices

 usage limit depends on the subscription
 
