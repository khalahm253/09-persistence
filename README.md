![cf](https://i.imgur.com/7v5ASc8.png) Lab 09: Vanilla REST API w/ Persistence


Travis link : https://travis-ci.com/khalahm253/09-persistence
Heroku link: https://lab-09-khalil.herokuapp.com/


*  I used promise constructs to manage asynchronous code
*  I created a vanilla RESTful API with in-memory persistence
* I saved resource data to the file system for a layer of data persistence
* I refactored commonly used coding constructs into custom helper modules




### `/api/vi/notes
* `POST` request
 * pass data as stringifed JSON in the body of a **POST** request to create a new resource
* `GET` request
 * pass `?id=<uuid>` as a query string parameter to retrieve a specific resource (as JSON)
* `DELETE` request
 * pass `?id=<uuid>` in the query string to **DELETE** a specific resource
 * this should return a 204 status code with no content in the body

## Tests
 * `GET`: test 404, it should respond with 'not found' for valid requests made with an id that was not found
 * `GET`: test 400, it should respond with 'bad request' if no id was provided in the request
 * `GET`: test 200, it should contain a response body for a request made with a valid id
 * `POST`: test 400, it should respond with 'bad request' if no request body was provided or the body was invalid
 * `POST`: test 200, it should respond with the body content for a post request with a valid body


