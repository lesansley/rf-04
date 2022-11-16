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
<div>
  {React.createElement(NewComponent, {
    children: 'Hello World',
    className: 'greeting',
  })}
</div>
```

- Option 2

```
<div>
  <NewComponent children="Goodbye Cruel World" className="farewell" />
<div/>
```

- Option 3

```
<div>
  {NewComponent({children: 'adieu', className: 'final'})}
</div>
```

## Renders as
```
<div id="root">
  <div class="greeting">Hello World</div>
  <div class="farewell">Goodbye Cruel World</div>
  <div class="final">adieu</div>
</div>
```
