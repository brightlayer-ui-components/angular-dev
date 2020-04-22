# Channel Value

The `<pxb-channel-value>` component is used to display a channel value (and units). This component abstracts the styles used to display the channel and units as well as an optional inline icon. These are used as part of the [`<pxb-hero>`](./Hero.md) component, but can also be used inline (e.g., in a list).

Icons are passed in as a child element of the `<pxb-channel-value>` component.

<div style="text-align:center; margin-bottom:20px">
    <img width="100%" style="max-width: 600px" alt="Channel Value in Hero" src="./images/heroes.png">
    <hr/>
    <img width="100%" style="max-width: 600px" alt="Channel Value in a list item" src="./images/channelValue.png">
</div>

## Usage

<div style="width: 100%; text-align: center">
    <img width="100%" style="max-width: 400px" alt="Channel Value Anatomy" src="./images/channelValueAnatomy.png">
</div>

```typescript
// app.module.ts
import { ChannelValueModule } from '@pxblue/angular-components';
...
imports: [
    ChannelValueModule
],
```

```html
// your-component.html
<pxb-channel-value class="content" value="65" units="%" [prefix]="true" fontSize="10px">
    <mat-icon>trending_up</mat-icon>
</pxb-channel-value>
```

## API

Parent element (`pxb-channel-value`) attributes:

<div style="overflow: auto;">

| Attributes | Description                                    | Type              | Required | Default   |
| ---------- | ---------------------------------------------- | ----------------- | -------- | --------- |
| fontSize   | The size of the font                           | `string`          | no       | 'inherit' |
| prefix     | Show units before the value                    | `boolean`         | no       | false     |
| units      | The text to display for the units (light text) | `string`          | no       |           |
| value      | The the value (bold text) to display           | `string | number` | yes      |           |

</div>

Child element:

| Attributes | Description             | Required | Default |
| ---------- | ----------------------- | -------- | ------- |
| (child)    | Icons shown on the left | no       |         |
