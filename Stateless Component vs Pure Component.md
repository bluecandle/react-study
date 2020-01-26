<h1>
<a href = "https://medium.com/groww-engineering/stateless-component-vs-pure-component-d2af88a1200b">
    Stateless Component vs Pure Component
</a>
</h1>

<strong>PureComponent <strong> changes the life-cycle method shouldComponentUpdate and adds some logic to automatically check whether a re-render is required for the component. This allows a PureComponent to call the method render only if it detects changes in state or props.

Pure Components gives a considerable increase in performance because it reduces the number of render operation in the application which is a huge win for complex UI and therefore advised to use if possible. Also, there will be cases where you want to use the lifecycle methods of Component and in such cases, we cannot use stateless components.

<b>Stateless Components are easy and fast to implement. They are good for very small UI view where re-render cost won’t matter that much. They provide cleaner code and less number of files to deal with.</b>