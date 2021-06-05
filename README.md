# NodeJS

it is async, event driven, single threaded JS based framework
it can handle a high amount of concurrent request. Not great for
CPU intensive task such as data crunching, ML or large calculations

## API

API is application programming interface. API in nodeJS terms means a server on remote machine that can do CRUD operations on
the DB

### REST API

it is an API design that combines DB resources , route paths
and HTTP verbs to allow application to describe that action
they are trying to perform. Works with basic data model to do
CRUD operations. Does not scale for complex data models.


## Node Basic terminologies and frameworks
### API

### REST

REST is an API design that combines DB resources, route paths and HTTP verbs
to allow application describe what action they are trying to perform.  

### Express

Handles tedious task like managing sockets, route matching, error handling and more

## Express framework

### Middlewares

Middleware allows you to execute function on incoming request
with guranteed order. Middlewares for authenticating, transforming the request, tracking and error handling

Middleware can also respond to a request like a controller function.
###  Routes
 
Express has a robust route matching system that allows user
for exact, regex, glob, and parameter matching. it also supports
HTTP verbs on route based level.  Express allows you to create 
sub routers

<b>Routes are matched in the order they were defined (Top to bottom)</b>

```js
const router = express.Router() // Routing framework from express
const app = express() // creating an express server

// creating a route and controlling the action
router.get('/products', (req, res, next) => {
    res.send({
        message: 'Hello';
    })
})

// Registering the route
app.use('/api', router)
app.use('/admin'router2)
```