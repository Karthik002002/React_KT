# Installation and Usage

## Install React Bootstrap

```bash
npm i react-bootstrap
```

## Include Bootstrap CSS

If you **don't want to customize** the Bootstrap CSS, you can simply include it using a CDN.  
Otherwise, install the vanilla Bootstrap via a package manager:

```bash
npm i bootstrap
```

## Import Bootstrap in Root Module

In your entry file (e.g., `index.js` or `App.js`), import Bootstrap CSS:

```js
import "bootstrap/dist/css/bootstrap.min.css";
```

> **Note:**  
> Importing Bootstrap CSS **should come before** importing any other CSS/SCSS files and React components that use CSS/SCSS styles.

# Components

## Accordion

Vertically collapsing element:

```jsx
<Accordion defaultActiveKey="0">
  <Accordion.Item eventKey="0">
    <Accordion.Header>Accordion Item #1</Accordion.Header>
    <Accordion.Body>Lorem ipsum</Accordion.Body>
  </Accordion.Item>
  <Accordion.Item eventKey="1">
    <Accordion.Header>Accordion Item #2</Accordion.Header>
    <Accordion.Body>Lorem ipsum</Accordion.Body>
  </Accordion.Item>
</Accordion>
```

### Accordion Props

- `defaultActiveKey={value}` – Specifies which `Accordion.Item` is open by default. The value corresponds to `eventKey`. If omitted, no item is open by default.
- `flush` – Removes the default background color and borders.
- `alwaysOpen` – Allows multiple items to stay open simultaneously. Example:

```jsx
<Accordion
  defaultActiveKey={["0", "1"]}
  alwaysOpen
>
```

- `onSelect={(selectedEventKey, event) => {}}` – Callback fired when the active item changes.

---

## Alerts

Styled feedback message:

```jsx
<Alert variant="warning">
  <Alert.Heading>Hey, just a warning</Alert.Heading>
  This is a 'warning' alert with <Alert.Link href="#">
    an example link
  </Alert.Link>.
</Alert>
```

### Alert Props

- `variant={value}` – Sets the style. Possible values:
  - `'primary'`
  - `'secondary'`
  - `'success'`
  - `'danger'`
  - `'warning'`
  - `'info'`
  - `'light'`
  - `'dark'`
- `dismissible` – Adds a button that dismisses the alert.
- `show={Boolean}` – Controls the visibility of the alert.
- `onClose={func}` – Callback invoked when the alert is closed.

## Badges

Count and labeling component, that matches the size of the immediate parent:

```jsx
<Button variant="primary">
  Profile <Badge bg="secondary">9</Badge>
  <span className="visually-hidden">unread messages</span>
</Button>
```

### Badge Props

- `bg="{keyword}"` – Applies Bootstrap's `.text-bg-{keyword}` style. The `keyword` matches the `variant` values from the Alert component.
- `pill` – Makes the badge have more rounded borders.

---

## Breadcrumbs

Indicates the current page’s location within a navigational hierarchy:

```jsx
<Breadcrumb>
  <Breadcrumb.Item href="#">Home</Breadcrumb.Item>
  <Breadcrumb.Item href="https://getbootstrap.com/docs/4.0/components/breadcrumb/">
    Library
  </Breadcrumb.Item>
  <Breadcrumb.Item active>Data</Breadcrumb.Item>
</Breadcrumb>
```

### Breadcrumb.Item Props

- `href={value}` – URL of the breadcrumb item.
- `active` – Marks the item as active and overrides `href`. The element is rendered as `<span>` instead of `<a>`.

---

## Buttons

### Button Props

- `variant={value}` – Style options:
  - `'primary'`
  - `'secondary'`
  - `'success'`
  - `'danger'`
  - `'warning'`
  - `'info'`
  - `'light'`
  - `'dark'`
  - `'link'`
  - `'outline-primary'`
  - `'outline-secondary'`
  - `'outline-success'`
  - `'outline-danger'`
  - `'outline-warning'`
  - `'outline-info'`
  - `'outline-light'`
  - `'outline-dark'`
- `size={value}` – Sets button size:
  - `'lg'`
  - `'sm'`
- `disabled` – Disables the button.
- `href={value}` – Renders the button as an `<a>` tag.
- `type={'button' | 'reset' | 'submit' | null}` – Sets the button’s HTML `type`.

---

## ToggleButton

Used to style a checkbox:

```jsx
<ToggleButton
  id="toggle-check"
  type="checkbox"
  variant="outline-primary"
  checked={checked}
  value="1"
  onChange={(e) => {
    setChecked(e.currentTarget.checked);
  }}
>
  Controlled checked
</ToggleButton>
```

## ToggleButton (Radio)

Styled radio buttons using `ToggleButton`:

```jsx
<ToggleButton
  id="radio-1"
  type="radio"
  variant="outline-secondary"
  name="radioOptions"
  value="1"
  checked={radioValue === '1'}
  onChange={(e) => setRadioValue(e.currentTarget.value)}
>
  radio option 1
</ToggleButton>

<ToggleButton
  id="radio-2"
  type="radio"
  variant="outline-secondary"
  name="radioOptions"
  value="2"
  checked={radioValue === '2'}
  onChange={(e) => setRadioValue(e.currentTarget.value)}
>
  radio option 2
</ToggleButton>
```

---

## Button Group

Grouping buttons together:

```jsx
<ButtonGroup>
  <Button>Left</Button>
  <Button>Middle</Button>
  <Button>Right</Button>
</ButtonGroup>
```

### Additional Components

- `<ButtonGroup>` – Wrapper around a group of `<Button>`, `<DropdownButton>`.
- `<ButtonToolbar>` – Wrapper around sets of `<ButtonGroup>` and `<InputGroup>`.

### ButtonGroup Props

- `size={'sm' | 'lg'}` – Applies the size to all inner buttons.
- `vertical` – Stacks the buttons vertically.

---

## Cards

A flexible and extensible container:

```jsx
<Card className="text-center">
  <Card.Img variant="top" src="#" />
  <Card.Header as="h3">Featured</Card.Header>
  <Card.Body>
    <Card.Title>Card Title</Card.Title>
    <Card.Subtitle>Card Subtitle</Card.Subtitle>
    <Card.Text>Card Text</Card.Text>
    <Card.Link href="#">Card Link</Card.Link>
    <Card.Link href="#">Another Link</Card.Link>
    <Button variant="primary">Go somewhere</Button>
  </Card.Body>
  <Card.Footer>Footer</Card.Footer>
</Card>
```

> **Note:**  
> `<Card.Body>` adds padding inside the card.

### Card Props

- `bg={'primary' | 'secondary' | ...}` – Sets background color.
- `text={'muted' | 'primary' | ...}` – Sets text color.
- `border={'primary' | 'secondary' | ...}` – Sets border color.

### Card.Img Props

- `variant="top"` or `variant="bottom"` – Positions the image at the top or bottom.

---

## Image Overlays

Turn an image into a card background:

```jsx
<Card style={{ width: '18rem' }} className="text-center">
  <Card.Img src="https://cdn.pixabay.com/photo/2024/05/05/05/55/goose-8740266_1280.jpg" />
  <Card.ImgOverlay>
    <Card.Header as="h3">Featured</Card.Header>
    <Card.Body>
      <!-- Add content here -->
    </Card.Body>
  </Card.ImgOverlay>
</Card>
```

---

## Navigation in Cards

```jsx
<Card.Header>
  <Nav variant="tabs" defaultActiveKey="#first">
    <Nav.Item>
      <Nav.Link href="#first">Active</Nav.Link>
    </Nav.Item>
    <Nav.Item>
      <Nav.Link href="#link">Link</Nav.Link>
    </Nav.Item>
  </Nav>
</Card.Header>
```

---

## Card Groups

Row-direction flexbox layout for multiple cards:

```jsx
<CardGroup>
  <Card>
    <!-- Card Content -->
  </Card>
  <Card>
    <!-- Another Card -->
  </Card>
</CardGroup>
```

## Carousels

Slideshow component for cycling through elements—images or slides of text:

```jsx
{
  /* Uncontrolled Carousel */
}
<Carousel style={{ width: "17rem" }}>
  <Carousel.Item>
    <Card>
      <Card.Img src="https://cdn.pixabay.com/photo/2024/04/25/06/50/banana-8719086_960_720.jpg" />
    </Card>
    <Carousel.Caption>
      <h3>First slide label</h3>
      <p>Nulla vitae elit libero, a pharetra augue mollis interdum.</p>
    </Carousel.Caption>
  </Carousel.Item>
  <Carousel.Item>
    <Card>
      <Card.Img src="https://cdn.pixabay.com/photo/2024/04/25/06/50/banana-8719086_960_720.jpg" />
    </Card>
    <Carousel.Caption>
      <h3>Second slide label</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </Carousel.Caption>
  </Carousel.Item>
</Carousel>;
```

### Carousel Props

- `fade` – Use fade transition instead of sliding.
- `slide={false}` – Disables sliding animation.
- `controls={false}` – Hides previous and next arrows.
- `indicators={false}` – Hides slide position indicators.
- `activeIndex={number}` – Manually set the current visible slide.
- `onSelect={(newIndex, event) => {}}` – Callback when the active slide changes.
- `interval={number | null}` – Time in milliseconds between auto slide changes.

### Carousel.Item Props

- `interval={value}` – How long to show a slide (in ms).

---

## Dropdowns

Toggler for displaying lists of links:

```jsx
<Dropdown>
  <Dropdown.Toggle id="dropdown-basic">Dropdown Button</Dropdown.Toggle>
  <Dropdown.Menu>
    <Dropdown.Header>Dropdown header</Dropdown.Header>
    <Dropdown.Item href="#/action-1">Action</Dropdown.Item>
    <Dropdown.Item href="#/action-2">Another action</Dropdown.Item>
    <Dropdown.Divider />
    <Dropdown.Item href="#/action-3">Something else</Dropdown.Item>
  </Dropdown.Menu>
</Dropdown>
```

### DropdownButton Alternative

```jsx
<DropdownButton id="dropdown-basic-button" title="Dropdown button">
  <Dropdown.Item href="#/action-1">Action</Dropdown.Item>
  <Dropdown.Item href="#/action-2">Another action</Dropdown.Item>
  <Dropdown.Item href="#/action-3">Something else</Dropdown.Item>
</DropdownButton>
```

### Dropdown.Item Variants

- Defaults to rendering as a link (`<a>`).
- Use `as="button"` to render as button.
- Use `<Dropdown.ItemText>` for non-interactive text items.

### Dropdown Props

- `drop={value}` – Dropdown menu position:
  - `'up'`, `'up-centered'`, `'start'`, `'end'`, `'down'`, `'down-centered'`
- `show` – Manually control visibility.
- `onToggle={func}` – Callback when dropdown is toggled.
- `autoClose={value}` – Closing behavior:
  - `true`, `'outside'`, `'inside'`, `false`

### Dropdown.Toggle Props

- `split` – Create a split-button dropdown:

```jsx
<Dropdown as={ButtonGroup}>
  <Button variant="success">Split Button</Button>
  <Dropdown.Toggle id="dropdown-basic" split />
</Dropdown>
```

### Dropdown.Menu Props

- `variant={value}` – Style variant.

---

## Images

Responsive image element:

```jsx
<Container className="w-25">
  <Image
    src="https://cdn.pixabay.com/photo/2024/03/30/04/56/tea-8664063_960_720.jpg"
    roundedCircle
    fluid
  />
</Container>
```

### Image Props

- `fluid` – Makes image scale to the parent element.
- Shape modifiers:
  - `rounded`
  - `roundedCircle`
  - `thumbnail`

---

## List Groups

Flexible component for displaying a series of content:

```jsx
<ListGroup numbered>
  <ListGroup.Item>Cras justo odio</ListGroup.Item>
  <ListGroup.Item>Dapibus ac facilisis in</ListGroup.Item>
</ListGroup>
```

### ListGroup Props

- `variant="flush"` – Removes outer borders and rounded corners.
- `horizontal={true | 'sm' | 'md' | 'lg' | 'xl' | 'xxl'}` – Makes the list horizontal from a given breakpoint. _Cannot be combined with `flush`._
- `numbered` – Adds automatic numbering to list items.

### ListGroup.Item Props

- `variant={'primary' | 'secondary' | ...}` – Color variant.
- `action` – Makes the item clickable:
  ```jsx
  <ListGroup.Item action href="#">Link Item</ListGroup.Item>
  <ListGroup.Item action onClick={() => {}}>Click Handler</ListGroup.Item>
  ```
- `active` – Highlights the item as selected.
- `disabled` – Makes the item unclickable.
- `href="#"` – Use for navigation links.
- `onClick={() => {}}` – Handle click events.

## Modals

- Modal elements appear over all other content.
- Only **one** modal window should be open at a time.

### Example:

```jsx
const [show, setShow] = useState(false);

const handleClose = () => setShow(false);
const handleShow = () => setShow(true);

return (
  <>
    <Button variant="primary" onClick={handleShow}>
      Launch demo modal
    </Button>

    <Modal show={show} onHide={handleClose}>
      <Modal.Header closeButton>
        <Modal.Title>Modal heading</Modal.Title>
      </Modal.Header>
      <Modal.Body>Woohoo, you are reading this text in a modal!</Modal.Body>
      <Modal.Footer>
        <Button variant="secondary" onClick={handleClose}>
          Close
        </Button>
        <Button variant="primary" onClick={handleClose}>
          Save Changes
        </Button>
      </Modal.Footer>
    </Modal>
  </>
);
```

### Modal Props

- `size={'sm' | 'lg' | 'xl'}` – Controls modal size.
- `fullscreen={true | 'sm-down' | 'md-down' | 'xl-down' | 'xxl-down'}` – Makes modal fullscreen under specific breakpoints.
- `centered` – Vertically centers the modal.
- `backdrop={'static' | true | false}` – `static` prevents closing by clicking outside; `false` removes backdrop entirely.
- `keyboard={false}` – Disables closing modal with the Escape key.
- `scrollable` – Enables scrolling only within `<Modal.Body>`.
- `animation={false}` – Disables opening/closing animation.
- `show` – Controls modal visibility.
- `onShow={() => {}}` – Callback triggered when modal opens.
- `onHide={() => {}}` – Callback triggered when modal closes.

### Modal.Header Props

- `closeButton` – Adds a close (×) button to the header.

---

## Navs

Basic flexbox-based navigation:

```jsx
<Nav>
  <Nav.Item>
    <Nav.Link href="/home">Active</Nav.Link>
  </Nav.Item>
  <Nav.Item>
    <Nav.Link eventKey="link-1">Link</Nav.Link>
  </Nav.Item>
  <Nav.Item>
    <Nav.Link eventKey="link-2">Link</Nav.Link>
  </Nav.Item>
  <Nav.Item>
    <Nav.Link eventKey="disabled" disabled>
      Disabled
    </Nav.Link>
  </Nav.Item>
</Nav>
```

### Nav Props

- `variant={'tabs' | 'pills' | 'underline'}` – Style variant.
- `activeKey={eventKey | href}` – The currently active item.
- `defaultActiveKey={eventKey | href}` – The default active item.
- `fill` – All items share equal width.
- `justify` – All items spread evenly across the container.

### Nav.Link Props

- `active` – Marks link as active.
- `disabled` – Disables the link.
- `href="#"` – Navigation link target.
- `eventKey={string | number}` – Unique key for Nav items.

---

## NavDropdown

Dropdown within a Nav component:

```jsx
<Nav>
  <NavDropdown title="Dropdown" id="nav-dropdown">
    <NavDropdown.Item eventKey="4.1">Action</NavDropdown.Item>
    <NavDropdown.Item eventKey="4.2">Another action</NavDropdown.Item>
    <NavDropdown.Item eventKey="4.3">Something else here</NavDropdown.Item>
    <NavDropdown.Divider />
    <NavDropdown.Item eventKey="4.4">Separated link</NavDropdown.Item>
  </NavDropdown>
</Nav>
```

### NavDropdown Props

- `title={string}` – Text content of the dropdown button.
- `disabled` – Disables the dropdown.
- `active` – Marks the dropdown as active.

## Navbars

- `expand` prop controls at which breakpoint the navbar collapses.
- Navbar is fluid by default.

```jsx
<Navbar expand="lg">
  <Container>
    <Navbar.Brand href="#home">React-Bootstrap</Navbar.Brand>
    <Navbar.Toggle aria-controls="basic-navbar-nav" />
    <Navbar.Collapse id="basic-navbar-nav">
      <Navbar.Text href="#link">Not Link</Navbar.Text>
      <Nav className="me-auto">
        <Nav.Link href="#home">Home</Nav.Link>
        <NavDropdown title="Dropdown" id="basic-nav-dropdown">
          <NavDropdown.Item href="#action/3.1">Action</NavDropdown.Item>
          <NavDropdown.Item href="#action/3.2">Another action</NavDropdown.Item>
          <NavDropdown.Item href="#action/3.3">Something</NavDropdown.Item>
          <NavDropdown.Divider />
          <NavDropdown.Item href="#action/3.4">Separated link</NavDropdown.Item>
        </NavDropdown>
      </Nav>
    </Navbar.Collapse>
  </Container>
</Navbar>
```

- The toggler appears only below the `lg` breakpoint.

### Navbar Props

- `expand={breakpoint}`
- `bg={'primary' | 'secondary'}`
- `fixed={'top' | 'bottom'}`
- `sticky={'top' | 'bottom'}`
- `collapseOnSelect`

---

## Offcanvas

Hidden sidebars that slide in from the edges.

```jsx
<Button variant="primary" onClick={handleShow}>Launch</Button>

<Offcanvas show={show} onHide={handleClose}>
  <Offcanvas.Header closeButton>
    <Offcanvas.Title>Offcanvas</Offcanvas.Title>
  </Offcanvas.Header>
  <Offcanvas.Body>
    Some placeholder content.
  </Offcanvas.Body>
</Offcanvas>
```

### Offcanvas Props

- `backdrop='static' | true | false`
- `keyboard={false}`
- `scroll` – allows body scrolling while open
- `placement={'start' | 'end' | 'top' | 'bottom'}`
- `responsive={'sm' | 'md' | 'lg' | 'xl' | 'xxl'}`

---

## Progress Bars

```jsx
<ProgressBar
  now={current}
  label={`${current}%`}
  variant="info"
  striped
  animated
/>
```

### ProgressBar Props

- `min`, `now`, `max` (numbers)
- `label={string}`
- `visuallyHidden`
- `striped`
- `animated`
- `variant={'success' | 'danger' | 'warning' | 'info'}`

---

## Spinners

Shows loading state.

```jsx
<Spinner animation="border" role="status">
  <span className="visually-hidden">Loading...</span>
</Spinner>
```

### Spinner Props

- `variant={'primary' | 'secondary' | ...}`
- `animation={'border' | 'grow'}`
- `size="sm"`

---

## Tables

### Table Props

- `striped` or `striped="columns"`
- `bordered`
- `hover`
- `variant={'primary' | 'secondary' | ...}`
- `responsive={true | 'sm' | 'md' | 'lg' | 'xl' | 'xxl'}`

---

## Tabs

```jsx
<Tabs defaultActiveKey="profile" id="uncontrolled-tab-example" className="mb-3">
  <Tab eventKey="home" title="Home">
    Tab content for Home
  </Tab>
  <Tab eventKey="profile" title="Profile">
    Tab content for Profile
  </Tab>
  <Tab eventKey="contact" title="Contact">
    Tab content for Contact
  </Tab>
</Tabs>
```

### Tabs Props

- `variant={'tabs' | 'pills' | 'underline'}`
- `fill`
- `justify`
- `activeKey={string}`
- `defaultActiveKey={string}`
- `onSelect={(eventKey, event) => {}}`

### Tab.Container (For more complex layouts)

```jsx
<Tab.Container id="left-tabs-example" defaultActiveKey="first">
  <Row>
    <Col sm={3}>
      <Nav variant="pills" className="flex-column">
        <Nav.Item>
          <Nav.Link eventKey="first">Tab 1</Nav.Link>
        </Nav.Item>
        <Nav.Item>
          <Nav.Link eventKey="second">Tab 2</Nav.Link>
        </Nav.Item>
      </Nav>
    </Col>
    <Col sm={9}>
      <Tab.Content>
        <Tab.Pane eventKey="first">First tab content</Tab.Pane>
        <Tab.Pane eventKey="second">Second tab content</Tab.Pane>
      </Tab.Content>
    </Col>
  </Row>
</Tab.Container>
```

---

## Toasts

Push notifications:

```jsx
<Button onClick={handleShow}>Show Toast</Button>

<Toast show={show} onClose={handleClose}>
  <Toast.Header>
    <strong className="me-auto">Bootstrap</strong>
    <small>11 mins ago</small>
  </Toast.Header>
  <Toast.Body>Hello, world! This is a toast message.</Toast.Body>
</Toast>
```

Multiple toasts:

```jsx
<ToastContainer position="bottom-end" className="p-3" style={{ zIndex: 1 }}>
  <Toast>
    <Toast.Header>
      <strong className="me-auto">Bootstrap</strong>
      <small className="text-muted">just now</small>
    </Toast.Header>
    <Toast.Body>See? Just like this.</Toast.Body>
  </Toast>
  <Toast>
    <Toast.Header>
      <strong className="me-auto">Bootstrap</strong>
      <small className="text-muted">2 seconds ago</small>
    </Toast.Header>
    <Toast.Body>Heads up, toasts will stack automatically</Toast.Body>
  </Toast>
</ToastContainer>
```

### Toast Props

- `autohide`
- `delay={number}`
- `bg={'primary' | 'secondary' | ...}`

### ToastContainer Props

- `position={value}` – Toast placement:
  - `'top-start'`
  - `'top-center'`
  - `'top-end'`
  - `'middle-start'`
  - `'middle-center'`
  - `'middle-end'`
  - `'bottom-start'`
  - `'bottom-center'`
  - `'bottom-end'`
