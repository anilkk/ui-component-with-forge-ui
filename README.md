# ui-component-with-forge-ui

This is intended as a quick reference and showcase of common UI components using the **Forge UI**. For more complete info, see [Forge UI components developer documentation](https://developer.atlassian.com/platform/forge/ui-components/).

### Table of Contents

**[Heading](#Heading)**<br>
**[Layout](#Layout)**<br>
**[Images](#Images)**<br>
**[Icons](#Icons)**<br>
**[Carousel](#carousel)**<br>

# Heading

Coming soon ...

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

### Note

1.  You may expect **delay** and you don't have smooth transition effect
