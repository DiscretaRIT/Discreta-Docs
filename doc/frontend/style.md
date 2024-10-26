# Frontend Style Guide
The following is a general style guide for the frontend of `Discreta`.

# Code formatting
Code formatting must be done with [Prettier](https://prettier.io/).
Ensure that all code is formatted before making PRs or commits to main repositories.

# Component styling
New components must be added into the `components/` directory. They have to be named in [Pascal Case](https://titlecapitalize.com/programming-case-styles/#pascal-case). 

The Component's filename must match with the component name itself.
Eg:
```jsx
const BaseComponent = () => {
    return (
        <>
            <h1> Hello World! </h1>
        </>
    )
}

export default BaseComponent
```
The above contents would be saved in a file named `BaseComponent.jsx`.

A component should be made if a particular part of your UI is re-used more than once.
Eg:
```jsx
const TitleBar = ({ title }) => {
    return (
        <>
            <div>
                <h1> {title} </h1>
            </div>
        </>
    )
}

export default TitleBar
```
The above component can be re-used over and over with only the title being changed per use. So refactoring it into a component makes sense here.

Components **have** to be functional **only**. Do not use class components. Refer more [here](https://www.geeksforgeeks.org/differences-between-functional-components-and-class-components/). They also **have** to be arrow functions.

A component has to be made within a `.jsx` file **only**. Do not use a `.js` file and `import { React } from "react"` every time. A consistent format for a component has to be maintained as follows:
```jsx
// Put your imports here.

const ComponentExample = (props) => {
    return (
        <>
            <div>
            </div>
        </>
    )
}

export default ComponentExample
```

Always start your component's return with an empty tag. This is to make sure that adding new children doesn't need a full refactor of the entire component structure.
```jsx
const HomePage = () => {
    return (
        <>
            <h1> Hello World! </h1>
        </>
    )
}
```

If the tag is short enough along with its contents and styling, they can be on a singular line as:
```jsx
<h1>Hello World!</h1>
```

But if its large enough, it has to be multi-line as:
```jsx
<parent-tag>
    <tag-child-1/>
    <tag-child-2>
        lorem ipsum dolor
    </tag-child-2>
</parent-tag>
```

Tags without any content inside it must be started and ended at the same time as:
```jsx
<img src="" alt="" className=""/>
```

Do not end lines with semicolon.

Images must be imported in the javascript and not used as a filepath source.
```jsx
import { IconExample } from "./icon.png"

const ImageComponent = () => {
    return (
        <>
            <img src={IconExample} alt="Icon Example"/>
        </>
    )
}

export default ImageComponent
```

CSS must also be directly imported in the javascript and not linked in the component's HTML.
```jsx
import "./index.css"
```

CSS of a component must be named the same as the component's file itself.
```jsx
import "BaseComponent.css"

const BaseComponent = () => {
    return (
        <>
            <h1> Hello World! </h1>
        </>
    )
}

export default BaseComponent
```

A blank line is to be maintained after the block of `import` statements and the component function's end.

# Variable naming
Variables have to named in [Camel Case](https://titlecapitalize.com/programming-case-styles/#camel-case).
```jsx
const exampleVariable = "Hello World!"
```

Variables used in the `useState` hook must follow the following consistent style. The setter function must be named as `set` followed by the variable name all written in Camel Case.
```jsx
import { useState } from "react"

const UseStateExample = () => {
    const [stateVar, setStateVar] = useState(true)

    return (
        <>
            <h1> {stateVar} </h1>
        </>
    )
}

export default UseStateExample
```

Variable declarations within the function must be in a block, followed by a blank line after all the variables are declared.