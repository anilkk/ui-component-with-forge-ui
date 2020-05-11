# ui-component-with-forge-ui

This is intended as a quick reference and showcase of common UI components using the **Forge UI**. For more complete info, see [Forge UI components developer documentation](https://developer.atlassian.com/platform/forge/ui-components/).

### Table of Contents

**[Heading](#Heading)**<br>
**[Link](#Link)**<br>
**[List](#List)**<br>
**[Button](#Button)**<br>
**[ButtonSet](#ButtonSet)**<br>
**[Layout](#Layout)**<br>
**[Images](#Images)**<br>
**[Icons](#Icons)**<br>
**[Carousel](#Carousel)**<br>
**[Video](#Video)**<br>
**[Accordion](#Accordion)**<br>
**[Modal](#Modal)**<br>
**[Navbar](#Navbar)**<br>

# Heading

Coming soon ...

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

```
<Text>
  [It's a link to my
  project](https://github.com/anilkk/ui-component-with-forge-ui)
</Text>
```

![Link demo](./img/link.png)

### Forge UI components used

1. [Text with link markdown](https://developer.atlassian.com/platform/forge/ui-components/text/#text)

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

Coming soon ...

# Images

Coming soon ...

# Icons

Coming soon ...

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

# Accordion

Coming soon ...

# Modal

Coming soon ...

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
