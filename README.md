# ui-component-with-forge-ui

This is intended as a quick reference and showcase of common UI components using the **Forge UI**. For more complete info, see [Forge UI components developer documentation](https://developer.atlassian.com/platform/forge/ui-components/).

### Table of Contents

**[Heading](#installation-instructions)**<br>
**[Carousel](#carousel)**<br>

# carousel

```jsx
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
```

![Carousel demo](./img/carousel-demo.gif)
