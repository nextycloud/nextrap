# Button

Buttons communicate the action that will occur when the user touches them. It consists of text, image, or both.

<!-- example -->
```jsx
import {Button, IconButton} from 'nextrap/components/button';


const TestButtons = () => (
  <div>
  <Button icon='bookmark' label='Bookmark' accent onRippleEnded={rippleEnded} />
  <Button icon='save' label='Save' raised primary rippleMultiple={false} onRippleEnded={rippleEnded} />
  <Button icon='inbox' label='Inbox' flat />
  <Button icon='add' floating />
  <Button icon='add' floating primary />
  <Button icon='add' floating primary disabled />
  <Button icon='add' floating accent mini />
  <IconButton icon='bookmark' accent />
  <IconButton icon='bookmark' />
  <IconButton icon='bookmark' disabled />
  <Button icon='add' label='Add this' flat primary />
  <Button icon='add' label='Add this' flat disabled />
  </div>
);
```

If you want to provide a theme via context, the component key is `RTButton`.

## Properties

| Name              | Type                  | Default     | Description|
|:-----|:-----|:-----|:-----|
| `accent`          | `Boolean`             | `false`     | Indicates if the button should have accent color.|
| `className`       | `String`              | `''`        | Set a class to style the Component.|
| `disabled`        | `Boolean`             | `false`     | If true, component will be disabled.|
| `flat`            | `Boolean`             | `false`     | If true, the button will have a flat look. |
| `floating`        | `Boolean`             | `false`     | If true, the button will have a floating look. |
| `href`            | `String`              |             | Creates a link for the button. |
| `icon`            | `String` or `Element` |             | Value of the icon (See Font Icon Component). |
| `inverse`         | `Boolean`             |             | If true, the neutral colors are inverted. Useful to put a button over a dark background. |
| `label`           | `String`              |             | The text string to use for the name of the button.|
| `mini`            | `Boolean`             | `false`     | To be used with floating button. If true, the button will be smaller.|
| `neutral`         | `Boolean`             | `true`      | Set it to `false` if you don't want the neutral styles to be included.|
| `onMouseLeave`    | `Function`            |             | Fires after the mouse leaves the Component.|
| `onMouseUp`       | `Function`            |             | Fires after the mouse is released from the Component.|
| `primary`         | `Boolean`             | `false`     | Indicates if the button should have primary color.|
| `raised`          | `Boolean`             | `false`     | If true, the button will have a raised look. |
| `ripple`          | `Boolean`             | `true`      | If true, component will have a ripple effect on click.|
| `theme`           | `Object`              |             | Theme object will classnames that will be used to style the component.|

By default it will have neutral colors and a flat aspect even though the `flat` property is `false` by default. Also, some properties exclude others, for example a button cannot be `flat` and `raised` at the same time.

The `Button` component also accept children so if you want to provide a custom component and text instead of a `label` and `icon` you can do it too. Just check the examples.

## Theme

| Name       | Description|
|:-----------|:-----------|
| `accent`   | Used for the root in case button is accent.|
| `button`   | Used for the root element in any button.|
| `flat`     | Used when the button is flat for the root element.|
| `floating` | Used when the button is floating for the root element.|
| `icon`     | For the icon inside a button.|
| `inverse`  | Used when colors are inverted.|
| `mini`     | Used for mini floating buttons.|
| `neutral`  | Used for neutral colored buttons.|
| `primary`  | Used for primary buttons when button is primary.|
| `raised`   | Used when the button is raised for root element.|
| `ripple`   | Used for the ripple element.|
| `toggle`   | Used for toggle buttons in the root element.|

## Icon Button

Icons are appropriate for toggle buttons that allow a single choice to be selected or deselected, such as adding or removing a star to an item. They are best located in app bars, toolbars, action buttons or toggles. We provide an `IconButton` component bundled with `Button` component. They share a similar API excluding onMouseLeave, onMouseUp and aspect properties.
