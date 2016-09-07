# Avatar

Avatars can be used to represent users, contacts, accounts or apps. You can provide an image source, a font icon or a title to use its first letter.

<!-- example -->
```jsx
import Avatar from 'nextrap/components/avatar'; 

const AvatarTest = () => (
  <section>
    <h5>Avatars</h5>
    <p>Avatars can be used to represent users, contacts, accounts or apps. You can provide an image source, a font icon or a title to use its first letter.</p>
    <Avatar style={{backgroundColor: 'deepskyblue'}} icon="folder" />
    <Avatar icon="folder_shared" />
    <Avatar image="https://d3fj8d3h19iopa.cloudfront.net/wp-content/uploads/2014/11/Virgin_logo_Cover_image.png" />
    <Avatar image="https://nextycloud.com/fr/assets/img/app/s-contact.png" cover />
    <Avatar title="Paul"/>
    <Avatar style={{backgroundColor: 'yellowgreen'}} icon="attach_money"></Avatar>
  </section>
);
```

If you want to provide a theme via context, the component key is `RTAvatar`.

## Properties

| Name          | Type                    | Default     | Description|
|:-----|:-----|:-----|:-----|
| `children`    | `Node`                  |             | Children for the avatar. You can pass an SVG for a custom icon or, for example, an image.|
| `className`   | `String`                | `''`        | Set a class to style the Component.|
| `cover`       | `Boolean`               | `''`        | Set to true if your image is not squared so it will be used as a cover for the element.|
| `icon`        | `String` or `Element`   |             | A key to identify an Icon from Material Design Icons or a custom Icon Element.|
| `image`       | `String` or `Element`   |             | An image source or an image element. |
| `title`       | `String`                | `''`        | A title for the image. If no image is provided, the first letter will be displayed as the avatar. |
| `theme`       | `Object`  | `null`   | Classnames object defining the component style.|

## Theme

| Name     | Description|
|:---------|:-----------|
| `avatar` | Used for the root class of the element.|
| `image`  | Added to the root element when the component has image.|
| `letter` | Used for the root element if the component shows the letter.|
