# Font Icon

The font icon component is used to represent an icon from the [Google Material Design](https://www.google.com/design/icons/) icon font.

<!-- example -->
```jsx
import FontIcon from 'nextrap/components/font_icon';

const FontIcons = () => (
  <span>
    <FontIcon value='add' />
    <FontIcon value='favorite' />
    <FontIcon>star</FontIcon>
  </span>
);
```

## Properties

| Name            | Type                    | Default         | Description|
|:-----|:-----|:-----|:-----|
| `children`      | `String`                |                 | The key string for the icon you want to be displayed.|
| `className`     | `String`                | `''`            | The class name to give custom styles such as sizing.|
| `value`         | `String` or `Element`   |                 | The key string for the icon you want be displayed.|
