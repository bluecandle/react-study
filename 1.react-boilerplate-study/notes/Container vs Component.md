<strong>A container does data fetching and then renders its corresponding sub-component. That’s it.</strong>
<a href="https://medium.com/@learnreact/container-components-c0e67432e005">link</a>

“Corresponding” meaning a component that shares the same name:
StockWidgetContainer => StockWidget
TagCloudContainer => TagCloud
PartyPooperListContainer => PartyPooperList
You get the idea.

A component should be dumb, which means that it can only present how an interface should look like. A container is a stateful, smart component. It contains data and has all the logic for mutating a data. For example, if you want to make a user login form, you can consider the form to be a separate component from it’s container. The container can call the form component and pass the submit handler function to the form component. More about components and containers here. Remember that components should be small, yep… Smaller than a you might think.

You’ll find your components much easier to reuse and reason about if you divide them into two categories. I call them Container and Presentational components* but I also heard Fat and Skinny, Smart and Dumb, Stateful and Pure, Screens and Components, etc. These all are not exactly the same, but the core idea is similar.

<strong>Remember, components don’t have to emit DOM. They only need to provide composition boundaries between UI concerns.</strong>



