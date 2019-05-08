We’re going to deploy a GraphQL instance on Heroku. Since, as I mentioned in Part 0, graphQL is _really_ just a standard, we have to pick a particular version of a GraphQL server to use. Like most people we’ll use the biggest project, [Apollo GraphQL](https://www.apollographql.com/). You can get Apollo GraphQL in a number of languages, but we’ll use the JavaScript version.

1. Create a Heroku App

Before you start, take just two steps:

- Setup a [Heroku](https://heroku.com/) account
- [Install the Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

The plan here is to create a heroku app to contain our GraphQL server, then we’ll download the Apollo GraphQL engine, and commit it to our Heroku app.

Before deploying, a new application must be setup. To do this, log into the [Heroku dashboard](https://dashboard.heroku.com/apps). Then click New > Create New App in the top right. The name you choose will be referred to later as <HEROKU_APP_NAME>, so be sure to replace it in the later sections. I chose to use heroku-graphql-toby so that’s the name that will appear in later commands. I assure you this app name isn’t magic and you can use whatever you’d like. Well, with an exception: since your app will get a nice Heroku URL at the end of this process, the app name has to be unique! Once you’ve found a unique name click ‘Create App’ to get started.

2. Create the app on your laptop

Now it’s time to create the app that we’re going to ‘push’ up to Heroku in a few moments.

> A word here on technique: I use the command line a lot. I do this because it looks a lot cooler than doing stuff in a file browser. Sometimes I do it for silly things like creating a file with the command, `>> index.js` > ![screenshot of a very vaporwave command terminal](https://pbs.twimg.com/media/D6E5SE8UIAAv4Zq?format=jpg&name=medium)
> I mean come on doesn't that look cool??

Start by
