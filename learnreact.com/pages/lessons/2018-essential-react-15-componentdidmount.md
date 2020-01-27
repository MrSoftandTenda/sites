<Head>
  <title>Learn React | Essential React > componentDidMount</title>
</Head>

# Essential React

## componentDidMount

<iframe width="560" height="315" src="https://www.youtube.com/embed/KtrgV-_OMhg" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

So we have this function now that will fetch a pokemon for us. How do we connect that to a React component? Well let’s first make a React component. We’re going to use some of those special `api`s that only live on `class` [Example]. Our component looks right, but we need to import React and `ReactDom` again to set up this project properly. [Example]. Finally, we’ll use `ReactDOM` to render our component to the `DOM`, giving it first an element that we’d like to render, and secondly the location that we’d like to render it to. If you remember, our page is already setup to have a root element with his `id` that we’re capturing and using here.So how do we get our component to call this function. Where do we do that? As I said before, this component that we’re extending comes with a bunch of special properties. If you go to the Reactjs docs, you can see all of those. So we’ll click on docs, go to references down here, and see the React component `api` section. If we scan through that we’ll see that there are tons and tons of these life cycle methods. We’ve used the constructor, we’ve used render, but there’s several more that we can use when we need them. Right now, I’m interested in life cycle methods that fire when the component mounts. And where possible, I like to favor ones that happen after React does a bunch of work, which is signified by `componentDidMount`. Back to our app, let’s implement that. Going to add a definition for `componentDidMount`. And here we’ll call our `fetchPokemon` function with the `id` of `1`. And to validate that it worked, we’ll take the data and log it out. Now, we know that every component requires a render lifecycle method to be defined, which returns some kind of component, but we have additional life cycle hooks that we can hook into when we need to do things at certain times, so when this component gets inserted into the `DOM` for the first time, it’s going to fire this function, and we can stuff anything in here that we want. In our case, we want to fetch a pokemon, pokemon with the `id` of `1`. Now we’re just logging it out, but it would be really nice to figure out how to communicate that into this render function. I’ll give you a hint! We already learned about it, and if you say it before the next lesson, I will give you a virtual high five.