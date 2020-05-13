# ui-component-with-forge-ui

This is intended as a quick reference and showcase of common UI components using the **Forge UI**. For more complete info, see [Forge UI components developer documentation](https://developer.atlassian.com/platform/forge/ui-components/).

### Table of Contents

**[Heading](#Heading)**<br>
**[Link](#Link)**<br>
**[List](#List)**<br>
**[Code](#Code)**<br>
**[Button](#Button)**<br>
**[ButtonSet](#ButtonSet)**<br>
**[Layout](#Layout)**<br>
**[Image](#Image)**<br>
**[Icons](#Icons)**<br>
**[Carousel](#Carousel)**<br>
**[Video](#Video)**<br>
**[Collapse](#Collapse)**<br>
**[Progress](#Progress)**<br>
**[Pagination](#Pagination)**<br>
**[Chart](#Chart)**<br>
**[Alert](#Alert)**<br>
**[Modal](#Modal)**<br>
**[Navbar](#Navbar)**<br>

# Heading

It's tempting to think heading with HTML header tags (h1 to h6). But, we need to understand [Forge](https://www.atlassian.com/forge) apps are embeded in the Atlassian products (JIRA, Confluence, page).

## Strong text

```
  <Text> **It's a strong text**</Text>
  <Text> __It's a strong text__</Text>
```

![strong text demo](./img/strong-text.png)

### Forge UI components used

1. [Strong text with star and underscore](https://developer.atlassian.com/platform/forge/ui-components/text/#text)

## Emphasis text

```
  <Text> *It's a emphasis text*</Text>
  <Text> _It's a emphasis text_</Text>
```

![emphasis text demo](./img/emphasis-text.png)

### Forge UI components used

1. [Emphasis text with star and underscore](https://developer.atlassian.com/platform/forge/ui-components/text/#text)

# Link

```
<Text>
  [It's a link to my
  project](https://github.com/anilkk/ui-component-with-forge-ui)
</Text>
```

![Link demo](./img/link.png)

### Forge UI components used

1. [Text with link markdown](https://developer.atlassian.com/platform/forge/ui-components/text/#text)

# List

## unordered list

```jsx
<Text> - Item 1 </Text>
<Text> - Item 2 </Text>
<Text> - Item 3 </Text>
<Text> - Item 4 </Text>
```

![Unordered list](./img/unordered-list.png)

### Forge UI components used

1.  [Text](https://developer.atlassian.com/platform/forge/ui-components/text/#text)

## ordered list

```jsx
<Text> 1. Item 1 </Text>
<Text> 2. Item 2 </Text>
<Text> 3. Item 3 </Text>
<Text> 4. Item 4 </Text>
```

![Ordered list](./img/ordered-list.png)

### Forge UI components used

1.  [Text](https://developer.atlassian.com/platform/forge/ui-components/text/#text)

# Code

```jsx
const sampleCode = `<Button text="sample button" onClick={() => { console.log('do some action')}}/>`;
return (
  <Fragment>
    <Text>{sampleCode}</Text>
  </Fragment>
);
```

![Code demo](./img/code.png)

### Forge UI components used

1. [Text with markdown for code ](https://developer.atlassian.com/platform/forge/ui-components/text/)

# Button

```jsx
<Button text="demo button" onClick={() => console.log('perform action')} />
```

![Button demo](./img/button.png)

### Forge UI components used

1. [Button](https://developer.atlassian.com/platform/forge/ui-components/button/)

# ButtonSet

```jsx
<ButtonSet>
  <Button text="demo button 1" onClick={() => console.log('perform action')} />
  <Button text="demo button 2" onClick={() => console.log('perform action')} />
</ButtonSet>
```

![Link demo](./img/buttons-group.png)

### Forge UI components used

1. [ButtonSet](https://developer.atlassian.com/platform/forge/ui-components/button-set/)
2. [Button](https://developer.atlassian.com/platform/forge/ui-components/button/)

# Layout

### Two columns

```jsx
<Image
  src="https://images.unsplash.com/photo-1560969184-10fe8719e047?auto=format&fit=crop&w=1200&q=50"
  alt="Berlin"
/>
```

![Two columns](./img/two-columns.png)

### Three columns

```jsx
<Image
  src="https://images.unsplash.com/photo-1560969184-10fe8719e047?auto=format&fit=crop&w=1200&q=50"
  alt="Berlin"
/>
```

![Three columns](./img/three-columns.png)

### Columns with spacing

```jsx
<Image
  src="https://images.unsplash.com/photo-1560969184-10fe8719e047?auto=format&fit=crop&w=1200&q=50"
  alt="Berlin"
/>
```

![columns with spacing demo](./img/column-with-spacing.png)

### Forge UI components used

1. [Table](https://developer.atlassian.com/platform/forge/ui-components/table/)

### Note

1. Be careful while using Table cells as a column, same UI is also rendred on the mobile apps.

# Image

You don't have option to style image(example: width and height). It's good practice to pass correct image.

```jsx
<Image
  src="https://images.unsplash.com/photo-1560969184-10fe8719e047?auto=format&fit=crop&w=1200&q=50"
  alt="Berlin"
/>
```

![Image demo](https://images.unsplash.com/photo-1560969184-10fe8719e047?auto=format&fit=crop&w=1200&q=50)

## Thumbnail image

```jsx
<Image
  src="https://res.cloudinary.com/anilkumark/image/upload/c_thumb,w_200,g_face/v1589315094/projects/forge/ui-components/photo-1560969184-10fe8719e047_hfksqn.jpg"
  alt="Berlin"
/>
```

![Thumbnail](https://res.cloudinary.com/anilkumark/image/upload/c_thumb,w_200,g_face/v1589315094/projects/forge/ui-components/photo-1560969184-10fe8719e047_hfksqn.jpg)

## Round image

```jsx
<Image
  src="https://res.cloudinary.com/anilkumark/image/upload/w_1000,c_fill,ar_1:1,g_auto,r_max,bo_5px_solid_red,b_rgb:262c35/v1589315094/projects/forge/ui-components/photo-1560969184-10fe8719e047_hfksqn.jpg"
  alt="Berlin"
/>
```

![Thumbnail](https://res.cloudinary.com/anilkumark/image/upload/w_1000,c_fill,ar_1:1,g_auto,r_max,bo_5px_solid_red,b_rgb:262c35/v1589315094/projects/forge/ui-components/photo-1560969184-10fe8719e047_hfksqn.jpg)

### Forge UI components used

1. [Image](https://developer.atlassian.com/platform/forge/ui-components/image/)

### Note

1. You can't style using CSS and so please your 3rd party services like [cloudinary](https://cloudinary.com/) to customize your image.

# Icons

You can use small [Image](#Image) component and you can also use emoji as icon with text.

```jsx
<Button text="✅ button with emoji icon" />
```

![Button text with icon emoji](./img/icon-emoji.png)

### Forge UI components used

1. [Image](https://developer.atlassian.com/platform/forge/ui-components/image/)

### Note

1. You can find collection of emojis on [getemoji](https://getemoji.com/) and [emojipedia](https://emojipedia.org/).

# Carousel

```jsx
const [images] = useState(() => {
  // You can make API call here
  return imageUrls;
});
const [currentIndex, setCurrentIndex] = useState(0);
return (
  <Fragment>
    <Text>**Carousel demo**</Text>
    <Table>
      <Row>
        <Cell>
          <Button
            text="<"
            onClick={() => {
              setCurrentIndex(
                currentIndex === 0 ? images.length - 1 : currentIndex - 1
              );
            }}
          />
        </Cell>
        <Cell>
          <Image src={images[currentIndex]} />
        </Cell>
        <Cell>
          <Button
            text=">"
            onClick={() => {
              setCurrentIndex(
                currentIndex === images.length - 1 ? 0 : currentIndex + 1
              );
            }}
          />
        </Cell>
      </Row>
    </Table>
  </Fragment>
);
```

![Carousel demo](./img/carousel-demo.gif)

### Forge UI components used

1. [Image](https://developer.atlassian.com/platform/forge/ui-components/image/)
2. [Button](https://developer.atlassian.com/platform/forge/ui-components/button/)
3. [Table](https://developer.atlassian.com/platform/forge/ui-components/table/)

### Forge UI hooks used

4. [useState](https://developer.atlassian.com/platform/forge/ui-hooks-reference/#usestate)

### Note

1.  You may expect **delay** and you don't have smooth transition effect

# Video

```jsx
  <Image
    src="https://res.cloudinary.com/anilkumark/image/upload/v1589197328/projects/forge/ui-components/Group_4_3_w6zihu.png"
    alt="forge tunnel debug"
  />
  <Text>
    [**Play Demo of Forge tunnel debug ▶️**](https://youtu.be/1AlzjCsczV4)
  </Text>
```

![forge tunnel debug](./img/forge-tunnel--debug.png)

### Forge UI components used

1. [Image](https://developer.atlassian.com/platform/forge/ui-components/image/)
2. [Text with link markdown](https://developer.atlassian.com/platform/forge/ui-components/text/#text)

### Note

1. Yes, it's not a video component, it's just a fallback.

# Collapse

```jsx
const [isOpen, setIsOpen] = useState(false);
<Button
  text="Toggle text view"
  onClick={() => {
    setIsOpen(!isOpen);
  }}
/>;
{
  isOpen && <Text>It's a collapsable text content</Text>;
}
```

![collapse](./img/collapse.gif)

### Forge UI components used

1. [Button](https://developer.atlassian.com/platform/forge/ui-components/button/)
1. [Text](https://developer.atlassian.com/platform/forge/ui-components/text/)

# Chart

```jsx
<Image
  src="https://quickchart.io/chart?bkg=white&c={type:%27bar%27,data:{labels:[2012,2013,2014,2015,2016],datasets:[{label:%27Users%27,data:[120,60,50,180,120]}]}}"
  alt="progress"
/>
```

![progress](https://quickchart.io/chart?bkg=white&c={type:%27bar%27,data:{labels:[2012,2013,2014,2015,2016],datasets:[{label:%27Users%27,data:[120,60,50,180,120]}]}})

### Forge UI components used

1. [Image](https://developer.atlassian.com/platform/forge/ui-components/image/)

### Note

1. For more details refer documentation [quickchart](https://quickchart.io/documentation/).

### Forge UI components used

1. [Image](https://developer.atlassian.com/platform/forge/ui-components/image/)

# Progress

```jsx
<Image
  src="https://quickchart.io/chart?c={type:'radialGauge',data:{datasets:[{data:[70],backgroundColor:'blue'}]}}"
  alt="progress"
/>
```

![progress](https://quickchart.io/chart?c={type:'radialGauge',data:{datasets:[{data:[70],backgroundColor:'blue'}]}})

### Forge UI components used

1. [Image](https://developer.atlassian.com/platform/forge/ui-components/image/)

# Pagination

```jsx
const handleClick = (buttonPressed) => {
  console.log('buttonPressed ---->', buttonPressed);
};

<ButtonSet>
  <Button
    text="Previous"
    onClick={(event) => {
      console.log('EVENT ---->', event);
      handleClick('Previous');
    }}
  />
  <Button
    text="2"
    onClick={() => {
      handleClick(2);
    }}
  />
  <Button
    text="3"
    onClick={() => {
      handleClick(3);
    }}
  />
  <Button
    text="4"
    onClick={() => {
      handleClick(4);
    }}
  />
  <Button
    text="Next"
    onClick={() => {
      handleClick('Next');
    }}
  />
</ButtonSet>;
```

![pagination demo](./img/pagination.png)

### Forge UI components used

1. [Button](https://developer.atlassian.com/platform/forge/ui-components/button/)
2. [ButtonSet](https://developer.atlassian.com/platform/forge/ui-components/text/#button-set)

# Alert

### Using Lozenge

Alerts are available for any length of text. For proper styling, use one of the six **appearance** value (e.g., .inprogress).

```jsx
      <Text>
        <Lozenge text="A simple default alert" appearance="default" />
      </Text>
      <Text>
        <Lozenge text="A simple primary alert" appearance="inprogress" />
      </Text>
      <Text>
        <Lozenge text="A simple info alert" appearance="new" />
      </Text>
      <Text>
        <Lozenge text="A simple warning alert ⚠️" appearance="moved" />
      </Text>
      <Text>
        <Lozenge text="A simple danger alert ⛔" appearance="removed" />
      </Text>
      <Text>
        <Lozenge text="A simple success alert ✅" appearance="success" />
      </Text>
```

![forge tunnel debug](./img/alert.png)

### Using ModalDialog

#### Danger ModelDialog

```jsx
const [isOpen, setIsOpen] = useState(false);

<Button text="Show modal" onClick={() => setIsOpen(true)} />;
{
  isOpen && (
    <ModalDialog
      header="My modal dialog"
      onClose={() => setIsOpen(false)}
      appearance="danger"
    >
      <Text>It's a ModalDialog danger on the header</Text>
    </ModalDialog>
  );
}
```

![danger ModalDialog](./img/danger-modal-dialog.png)

#### Warning ModelDialog

```jsx
const [isOpen, setIsOpen] = useState(false);

<Button text="Show modal" onClick={() => setIsOpen(true)} />;
{
  isOpen && (
    <ModalDialog
      header="My modal dialog"
      onClose={() => setIsOpen(false)}
      appearance="warning"
    >
      <Text>It's a ModalDialog warning on the header</Text>
    </ModalDialog>
  );
}
```

![danger ModalDialog](./img/danger-modal-dialog.png)

### Forge UI components used

1. [Text](https://developer.atlassian.com/platform/forge/ui-components/text/#text)
2. [Lozenge](https://developer.atlassian.com/platform/forge/ui-components/text/#lozenge)
3. [ModalDialog](https://developer.atlassian.com/platform/forge/ui-components/modal-dialog)

# Modal

```jsx
const [isOpen, setOpen] = useState(false);
<Button text="Show modal" onClick={() => setOpen(true)} />;
{
  isOpen && (
    <ModalDialog header="My modal dialog" onClose={() => setOpen(false)}>
      <Text>It's a ModalDialog</Text>
    </ModalDialog>
  );
}
```

![ModalDialog](./img/modaldialog.gif)

### Forge UI components used

1. [ModalDialog](https://developer.atlassian.com/platform/forge/ui-components//modal-dialog/)

# Navbar

## Navbar with buttons

```jsx
<Table>
  <Row>
    <Cell>
      <Image
        src="https://res.cloudinary.com/anilkumark/image/upload/c_thumb,w_200,g_face/v1589212010/projects/forge/ui-components/anil-logo_yq4vyu.png"
        alt="demo logo"
      />
    </Cell>
    {/* Create many empty Cell for spacing */}
    <Cell></Cell>
    <Cell></Cell>
    <Cell></Cell>
    <Cell>
      <ButtonSet>
        <Button text="Home" />
        <Button text="About" />
        <Button text="Contact" />
      </ButtonSet>
    </Cell>
  </Row>
</Table>
```

![Navbar using Forge UI](./img/navbar-with-buttons.png)

### Forge UI components used

1. [Image](https://developer.atlassian.com/platform/forge/ui-components/image/)
2. [Button](https://developer.atlassian.com/platform/forge/ui-components/button/)
3. [ButtonSet](https://developer.atlassian.com/platform/forge/ui-components/button-set/)
4. [Table](https://developer.atlassian.com/platform/forge/ui-components/table/)

## Navbar with text lnks

```jsx
<Table>
  <Row>
    <Cell>
      <Image
        src="https://res.cloudinary.com/anilkumark/image/upload/c_thumb,w_200,g_face/v1589212010/projects/forge/ui-components/anil-logo_yq4vyu.png"
        alt="demo logo"
      />
    </Cell>
    {/* Create many empty Cell for spacing */}
    <Cell></Cell>
    <Cell></Cell>
    <Cell></Cell>
    <Cell>
      <Text>
        [Home](https://developer.atlassian.com/platform/forge)
        {'  '} {/* For extra spacing */}
        [Reference](https://developer.atlassian.com/platform/forge/manifest-reference/)
        {'  '} {/* For extra spacing */}
        [Help](https://developer.atlassian.com/platform/forge/get-help/)
      </Text>
    </Cell>
  </Row>
</Table>
```

![Navbar using Forge UI](./img/navbar-with-links.png)

### Forge UI components used

1. [Image](https://developer.atlassian.com/platform/forge/ui-components/image/)
2. [Text with link markdown](https://developer.atlassian.com/platform/forge/ui-components/text/#text)
3. [Table](https://developer.atlassian.com/platform/forge/ui-components/table/)
