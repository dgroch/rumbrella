# Rumbl

To start:

* Install dependencies with `mix deps.get`
* Create and migrate your database with `mix ecto.create && mix ecto.migrate`
* Install Node.js dependencies with `npm install`
* Start Phoenix endpoint with `mix phoenix.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](http://www.phoenixframework.org/docs/deployment).

## Chapter 2 : Lay of the Land

* We installed Phoenix, which is built using Erlang and OTP for the service layer, Elixir for the language, and Node.js for packaging static assets.
* We used the Elixir build tool mix to create a new project and start our server.
* Web applications in Phoenix are pipelines of plugs.
* The basic flow of traditional applications is endpoint, router, pipeline, controller.
* Routers distribute requests.
* Controllers call services and set up intermediate data for views.

## Chapter 3 : Controllers, Views and Templates

* We created a simple repository. We did so to simplify your plunge into
the world of controllers and views.
* We created actions, which serve as the main point of control for each
request.
* We created views, which exist to render templates.
* We created templates, which generate HTML for our users.
* We employed helpers, which are simple Phoenix functions used in templates.
* We used layouts, which are HTML templates that embed an action’s HTML.

## Chapter 4 : Ecto and Changesets

* We began the chapter by introducing Ecto and announcing our intention
to replace the in-memory repository with a database-backed repository
using Ecto.
* We configured our new database and connected it to OTP, so that Elixir
could do the right thing in the event of a Phoenix or Ecto crash.
* We created a schema, complete with information about each necessary
field.
* We created a migration, to help us specify our database tables and automate
doing and undoing any database changes.
* We created a changeset so Ecto could efficiently track and manage each
change requested by our application.
* We integrated this change into our application.

## Chapter 5 : Authenticating Users

* We added the comeonin dependency to our project.
* We built our own authentication layer.
* We built the associated changesets to handle validation of passwords.
*  We implemented a module plug that loads the user from the session and
made it part of our browser pipeline.
*  We implemented a function plug and used it alongside some specific
actions in our controller pipeline.

## Chapter 6 : Generators and Relationships

* We converted a private plug into a public function and shared it with our controllers and routers.
* You learned how to migrate and roll back changes to the database.
* We defined relationships between User and Video schemas and used functions from Ecto to build and retrieve associated data.
* You learned that Ecto uses strictly explicit semantics to determine if a
relationship is loaded or not.

## Chapter 7 : Ecto Queries and Constrains

* We used Ecto’s query API, which is independent of the repository API, to
do some basic queries.
* We used two forms of queries, a keyword list–based syntax and a pipebased
syntax.
* We used fragments to pass SQL commands through the query API
unchanged.
* We explored the different ways Ecto queries work with relationships,
beyond data preloading.
* We wrote constraint-style validations for unique indexes and foreign-key
violations.
* We learned how to choose between letting constraint errors go and when
to report them to the user.

## Chapter 8 : Testing MVC

* We examined how tests work in Phoenix.
* We set up some basic testing functions to insert users and videos, and
shared those across all of our potential test cases.
* We wrote some basic integration tests, bypassing only our authentication
plug.
* We used Phoenix test helpers to make multiple assertions in a compact
way.
* We tested our authentication plug in isolation.
* We tested our views.
* We tested models with and without side effects.

## Chapter 9 : Watching Videos

* You learned to use Brunch to support development-time reloading and
minimization for production code.
* We used generators to create an Ecto migration.
* We used changesets to create slugs.
* We used protocols to seamlessly build URLs from those new slugs.

## Chapter 10 : Using Channels

* Learned to connect to a server-side channel through an ES6 client.
* Built a server-side channel with both long-polling and WebSocket
support.
* Built a simple API to let users join a channel.
* Processed inbound messages from OTP with handle_info and channels
with handle_in.
* Sent broadcast messages with broadcast!.
* Authenticated users with Phoenix.Token.
* Persisted annotations with Ecto.

## Chapter 11 : OTP

* Built a counter that demonstrates how some OTP behaviors work.
* Looked at several OTP supervision and restart strategies.
* Looked at examples of a full OTP service as GenServer.
* Learned how tasks wrap behavior and agents encapsulate state.
* Implemented an information system abstract front end with concrete
backends.
* Learned to fetch WolframAlpha results from an HTTP service and
share them with our channels.

## Chapter 12 : Observer and Umbrellas

* Used Observer to view our application.
* Found a convenient place to split our application.
* Moved our information system into its own child umbrella project.
* Moved rumbl into its own child umbrella project.
* Learned to identify configuration changes, including dependencies,
supervision trees, and application configuration.
