# rf-04

## Rendering JSX from functions

**`Message` component**
```
function message({children}) {
  return <div className="message">{children}</di>
}

const goodbyeElement = message({children: "Goodbye"}

const element = (
  <div className="container">
    {message({children: "Hello"})}
    {goodbyeElement}
  </div>
)
```
Renders as
```
<div className="container">
  <div class="message">Hello</div>
  <div class="message">Goodbye</div>
</div>
```

## Methods of rendering JSX

**`NewComponent` component**

```
function NewComponent(props) {
  return <div {...props} />
}
```

- React.createElement

```
<React.Fragment>
  {React.createElement(NewComponent, {
    children: 'Hello World',
    className: 'greeting',
  })}
</React.Fragment>
```

- JSX

```
<React.Fragment>
  <NewComponent children="Goodbye Cruel World" className="farewell" />
</React.Fragment>
```

- Function call

```
<React.Fragment>
  {NewComponent({children: 'adieu', className: 'final'})}
</React.Fragment>
```

## Renders as
```
<div id="root">
  <div class="greeting">Hello World</div>
  <div class="farewell">Goodbye Cruel World</div>
  <div class="final">adieu</div>
</div>
```

Attribution: https://epicreact.dev/modules/react-fundamentals/
