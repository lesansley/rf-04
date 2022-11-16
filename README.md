# rf-04

Rendering JSX from functions

```
function NewComponent(props) {
  return <div {...props} />
}
```

## Methods of consuming the NewComponent

- Option 1

```
<React.Fragment>
  {React.createElement(NewComponent, {
    children: 'Hello World',
    className: 'greeting',
  })}
</React.Fragment>
```

- Option 2

```
<React.Fragment>
  <NewComponent children="Goodbye Cruel World" className="farewell" />
</React.Fragment>
```

- Option 3

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
