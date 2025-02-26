> [!NOTE]
> This repository was previously named **tailwind-starter-kit** and has been renamed to **david-ai** to better reflect its purpose and direction.

# David UI - Free Tailwind CSS Components Library

[David UI](https://www.creative-tim.com/david-ui) is a free and open-source collection of customizable, production-ready UI components built with **Tailwind CSS**. Designed to be developer-friendly and performance-focused, David UI streamlines the creation of modern, visually appealing interfaces, helping you deliver high-quality user experiences faster.

[![David UI Thumb](https://github.com/creativetimofficial/public-assets/blob/master/ct-assets/david-ai.png?raw=true)](https://www.creative-tim.com/david-ui/html/overview)

<div align="center">
  
[![npm version](https://img.shields.io/npm/v/david-ai.svg)](https://www.npmjs.com/package/david-ai)
[![npm downloads](https://img.shields.io/npm/dm/david-ai.svg)](https://www.npmjs.com/package/david-ai)

</div>

## Table of Contents

- [David UI - Free Tailwind CSS Components Library](#david-ui---free-tailwind-css-components-library)
  - [Table of Contents](#table-of-contents)
  - [Getting Started](#getting-started)
    - [Using with CDN](#using-with-cdn)
    - [Basic Usage NPM](#basic-usage-npm)
    - [Using with Global Access](#using-with-global-access)
    - [Typescript](#typescript)
  - [Documentation](#documentation)
  - [Explore Components](#explore-components)
  - [Community](#community)
  - [License](#license)
  - [Contribute \& Feedback](#contribute--feedback)

## Getting Started

Learn how to use `david-ai` components to quickly and easily create elegant and flexible pages using Tailwind CSS.

`david-ai` is working with Tailwind CSS classes and you need to have Tailwind CSS installed on your project - <a href="https://tailwindcss.com/docs/installation" target="_blank">Tailwind CSS Installation.</a>

### Using with CDN

You can include david-ai via a CDN and initialize alerts globally in the browser. Add the following script to your HTML file:

```html
<script
  src="https://cdn.jsdelivr.net/gh/creativetimofficial/david-ai@1.0.6/packages/dist/david-ai.min.js"
  defer
></script>
```

### Basic Usage NPM

```bash
npm i david-ai
```

After installing, you can use the components in your project across different frameworks:

```tsx
import { initAlert } from "david-ai";

// Initialize alerts
initAlert();
```

### Using with Global Access

If you prefer, you can use the DavidAI global object instead of directly importing initAlert:

```tsx
import * as DavidAI from "david-ai";

// Initialize alerts
DavidAI.initAlert();
```

## TypeScript

David AI components can be used in two ways - through simple ESM imports or programmatically with TypeScript support. Here's how to use both approaches:

### Simple ESM Import

The quickest way to use components is through direct ESM imports:

```tsx
import { initAlert } from "david-ai";

// Initialize alerts
initAlert();
```

### Programmatic Usage with TypeScript

For more control and type safety, you can use the programmatic approach with full TypeScript support:

This programmatic approach provides:

- Full TypeScript support
- Fine-grained control over component behavior
- Access to component instance methods
- Proper cleanup on unmount

```tsx
import { Accordion } from "david-ai";
import type { AccordionConfig, IAccordion } from "david-ai";

document.addEventListener("DOMContentLoaded", () => {
  const container = document.getElementById("accordion-container");

  if (container) {
    const config: AccordionConfig = {
      exclusive: true,
      allOpen: false,
    };

    const accordion: IAccordion = new Accordion(container, config);

    // Handle external button controls
    const showAllButton = document.getElementById("show-all");
    const hideAllButton = document.getElementById("hide-all");
    const toggleFirstButton = document.getElementById("toggle-first");

    showAllButton?.addEventListener("click", () => {
      accordion.showAll();
    });

    hideAllButton?.addEventListener("click", () => {
      accordion.hideAll();
    });

    toggleFirstButton?.addEventListener("click", () => {
      const firstButton = document.getElementById("button-1") as HTMLElement;
      if (firstButton) {
        accordion.toggle(firstButton);
      }
    });

    // Cleanup on unmount
    window.addEventListener("unload", () => {
      accordion.cleanup();
    });
  }
});
```

For detailed usage of each component, check out their respective documentation:

- [Accordion](https://www.creative-tim.com/david-ui/docs/html/accordion) (ESM & Programmatic)
- [Alert](https://www.creative-tim.com/david-ui/docs/html/alert) (ESM)
- [Collapse](https://www.creative-tim.com/david-ui/docs/html/collapse) (ESM & Programmatic)
- [Dropdown](https://www.creative-tim.com/david-ui/docs/html/dropdown) (ESM & Programmatic)
- [Gallery](https://www.creative-tim.com/david-ui/docs/html/gallery) (ESM)
- [Modal](https://www.creative-tim.com/david-ui/docs/html/modal) (ESM & Programmatic)
- [Popover](https://www.creative-tim.com/david-ui/docs/html/popover) (ESM & Programmatic)
- [Stepper](https://www.creative-tim.com/david-ui/docs/html/stepper) (ESM & Programmatic)
- [Tabs](https://www.creative-tim.com/david-ui/docs/html/tabs) (ESM & Programmatic)
- [Tooltip](https://www.creative-tim.com/david-ui/docs/html/tooltip) (ESM & Programmatic)

Congratulations 🥳, you did it, now you're ready to use `david-ai`.

## Documentation

David UI’s documentation includes code snippets, previews, and detailed usage instructions for each component, ensuring a smooth implementation process.

Visit the **[David UI Docs](https://www.creative-tim.com/david-ui)** to explore the entire library.

## Explore Components

<table>
  
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/accordion">
        <img alt="accordion" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/accordion-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/alert">
        <img alt="alert" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/alert-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/avatar">
        <img alt="avatar" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/avatar-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Accordion</td>
    <td width="33.3333%">Alert</td>
    <td width="33.3333%">Avatar</td>
  </tr>
  <tr height="30"></tr>
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/badge">
        <img alt="typography" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/badge-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/breadcrumb">
        <img alt="breadcrumbs" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/breadcrumbs-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/button">
        <img alt="button" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/button-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Badge</td>
    <td width="33.3333%">Breadcrumbs</td>
    <td width="33.3333%">Button</td>
  </tr>
  <tr height="30"></tr>
  
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/button-group">
        <img alt="select" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/buttongroup-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/card">
        <img alt="card" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/card-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/checkbox">
        <img alt="checkbox" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/checkbox-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Button Group</td>
    <td width="33.3333%">Card</td>
    <td width="33.3333%">Checkbox</td>
  </tr>
  <tr height="30"></tr>
  
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/chip">
        <img alt="chip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/chip-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/collapse">
        <img alt="tooltip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/collapse-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/dropdown">
        <img alt="menu" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/menu-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Chip</td>
    <td width="33.3333%">Collapse</td>
    <td width="33.3333%">Dropdown</td>
  </tr>
  <tr height="30"></tr>
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/footer">
        <img alt="typography" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/footer-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/icon-button">
        <img alt="icon-button" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/icon-button-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/image">
        <img alt="typography" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/img-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Footer</td>
    <td width="33.3333%">Icon Button</td>
    <td width="33.3333%">Image</td>
  </tr>
  <tr height="30"></tr>
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/input">
        <img alt="input" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/input-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/list">
        <img alt="tooltip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/list-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/modal">
        <img alt="dialog" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/dialog-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Input</td>
    <td width="33.3333%">List</td>
    <td width="33.3333%">Modal</td>
  </tr>
  <tr height="30"></tr>
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/navbar">
        <img alt="navbar" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/navbar-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/pagination">
        <img alt="pagination" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/pagination-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/popover">
        <img alt="popover" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/popover-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Navbar</td>
    <td width="33.3333%">Pagination</td>
    <td width="33.3333%">Popover</td>
  </tr>
  <tr height="30"></tr>
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/progress">
        <img alt="progress-bar" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/progress-bar-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/radio">
        <img alt="radio-button" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/radio-button-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/rating">
        <img alt="tooltip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/ratingbar-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Progress Bar</td>
    <td width="33.3333%">Radio Button</td>
    <td width="33.3333%">Rating Bar</td>
  </tr>
  <tr height="30"></tr>
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/sidebar">
        <img alt="tooltip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/sidebar-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/spinner">
        <img alt="tooltip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/spinner-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/stepper">
        <img alt="tooltip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/stepper-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Sidebar</td>
    <td width="33.3333%">Spinner</td>
    <td width="33.3333%">Stepper</td>
  </tr>
  <tr height="30"></tr>
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/switch">
        <img alt="switch" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/switch-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/table">
        <img alt="typography" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/table-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/tabs">
        <img alt="tabs" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/tabs-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Switch</td>
    <td width="33.3333%">Table</td>
    <td width="33.3333%">Tabs</td>
  </tr>
  <tr height="30"></tr>
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/textarea">
        <img alt="textarea" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/text-area-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/tooltip">
        <img alt="tooltip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/tooltip-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/typography">
        <img alt="typography" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/typography-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Textarea</td>
    <td width="33.3333%">Tooltip</td>
    <td width="33.3333%">Typography</td>
  </tr>
  <tr height="30"></tr>
  <tr>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/timeline">
        <img alt="tooltip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/timeline-thumbnail.jpg">
      </a>
    </td>
    <td width="33.3333%" style="padding: 0;">
      <a href="https://www.creative-tim.com/david-ui/docs/html/video">
        <img alt="tooltip" src="https://raw.githubusercontent.com/creativetimofficial/public-assets/refs/heads/master/david-ui/img/video-thumbnail.jpg">
      </a>
    </td>
  </tr>
  <tr>
    <td width="33.3333%">Timeline</td>
    <td width="33.3333%">Video</td>
  </tr>
</table>

## Community

- We're excited to see the community adopt David AI, raise issues, and provide feedback.
- Whether it's a feature request, bug report, or a project to showcase, please get involved!

## License

Copyright (c) 2020-2025 [Creative Tim](https://www.creative-tim.com)

David UI is distributed under the **[MIT License](https://creative-tim.com/david-ui/docs/html/license)**, providing freedom and flexibility for all projects.

## Older Version

You can find the older version of the David UI in the [tailwind-starter-kit](https://github.com/creativetimofficial/david-ai/tree/tailwind-starter-kit) branch.

## Contribute & Feedback

We welcome contributions and feedback! If you have suggestions, encounter issues, or want to propose new components, feel free to open an issue or submit a pull request on our repository. Your input helps make David UI better for everyone.

---

**Build better, faster, and smarter with David UI.** Explore the documentation and start leveraging our components to deliver polished, user-friendly interfaces with ease.
