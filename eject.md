# what does eject command do?
### simple explanation
<a href = "https://stackoverflow.com/questions/48308936/what-does-this-react-scripts-eject-command-do">link</a>

create-react-app encapsulates all of the npm modules it is using internally, so that your package.json will be very clean and simple without you having to worry about it.

However, if you want to start doing more complex things and installing modules that may interact with modules create-react-app is using under the hood, those new modules need to know what is available and not, meaning you need to have create-react-app un-abstract them.

That, in essence, is what react-scripts eject does. It will stop hiding what it's got installed under the hood and instead eject those things into your project's package.json for everyone to see.

### official

<a href = "https://github.com/facebook/create-react-app/blob/master/packages/cra-template/template/README.md#npm-run-eject"> link </a>

<b>Note: this is a one-way operation. Once you eject, you can’t go back! </b>

If you aren’t satisfied with the build tool and configuration choices, you can eject at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except eject will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use eject. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

