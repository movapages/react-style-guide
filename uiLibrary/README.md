# The Ellucian Path Design System

## _Best Practices for The Ellucian Path Design System_

**_The Ellucian Path Design System_** is a design language and system to build modern, consistent, and inclusive experiences for products and platforms across the Ellucian ecosystem.
It  provides design guidelines and a UI library of components.

> **Current release:** `7.10.0`

### Setup Guide
#### Peer Dependencies
- `react: ^17.0.2`
- `react-dom: ^17.0.2`

#### CDN Dependencies
- Fonts
    ```html
    <link 
      href="https://cdn.elluciancloud.com/assets/EDS2/7.10.0/fonts/fonts.css" 
      rel="stylesheet"
    />
    ```
- [Background Images](https://path-designsystem.elluciancloud.com/#/design-guidelines/backgrounds)
- [Large Illustrations](https://path-designsystem.elluciancloud.com/#/design-guidelines/illustration)

The assets for this release live [here](https://cdn.elluciancloud.com/assets/EDS2/7.10.0/).

#### Quick Start
Make `EDSApplication` the top-level component of your application. All EPDS components must be nested under this component.
```jsx
import { EDSApplication } from '@ellucian/react-design-system/core';

const App = () => (
    <EDSApplication>
      <p>Hello World</p>
    </EDSApplication>
);
```

**You can explore further items of the setup guide via [this link](https://path-designsystem.elluciancloud.com/#/getting-started/getting-started).**

### Design Standards
EPDS offers a set of design guidelines that developers should follow during the development process:
- [Accessibility](https://path-designsystem.elluciancloud.com/#/design-guidelines/accessibility)
- [Backgrounds](https://path-designsystem.elluciancloud.com/#/design-guidelines/backgrounds)
- [Color](https://path-designsystem.elluciancloud.com/#/design-guidelines/color)
- [Iconography](https://path-designsystem.elluciancloud.com/#/design-guidelines/iconography)
- [Illustration](https://path-designsystem.elluciancloud.com/#/design-guidelines/illustration)
- [Typography](https://path-designsystem.elluciancloud.com/#/design-guidelines/typography)
- [Writing Standards](https://path-designsystem.elluciancloud.com/#/design-guidelines/writing-standards)
- [Z-Index](https://path-designsystem.elluciancloud.com/#/design-guidelines/z-index)

### UI Component Library
EPDS offers a wide variety of UI components, which you can explore by visiting [this link](https://path-designsystem.elluciancloud.com/#/components).

## Links:
- [The Ellucian Path Design System](https://path-designsystem.elluciancloud.com/#/)