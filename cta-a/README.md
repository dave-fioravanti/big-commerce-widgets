# BigCommerce Widget: CTA-A

A custom CTA widget for BigCommerce Page Builder featuring a two column grid layout with an image, title and description text, and a configurable action.

[Design Specification](design.png)

<img src="./example.png" width="600" alt="CTA-A Example Image">

## Features

- **Two Column Grid**: A balanced image-and-copy layout that highlights a message alongside a supporting visual.
- **Highly Configurable**: Tune colors, spacing, and typography through Page Builder settings.
- **Responsive Design**: Includes a breakpoint setting that handles mobile/tablet responsiveness.
- **Controllable Layout**: Display the image on the left or the right on desktop and above or below the copy below the responsive breakpoint value.

## Prerequisites

Before you begin installing the CTA-A widget, ensure you have the following:

- A BigCommerce store with access to the control panel.
- A BigCommerce theme that supports Page Builder.
- API credentials for your BigCommerce store to authenticate the Widget Builder CLI tool.

## Installation Instructions

To install the CTA-A widget in your BigCommerce theme, follow these steps:

### Setting Up the Widget Builder CLI

1. In your terminal, navigate to the root directory of the BigCommerce theme you want to install the widget in.

2. Clone the BigCommerce [widget-builder](https://github.com/bigcommerce/widget-builder) repository.

3. Follow the instructions in the widget-builder repository to set up the CLI tool.

### Installing the Widget

1. Run the following command to create a new widget (you can replace `cta-a` with your desired widget name):

```bash
widget-builder create cta-a
```

2. After creating the widget, replace the generated files with the corresponding files from the `src/` directory of this repository.

3. Once you have replaced the files, you can run the widget locally to test it and ensure that everything is working correctly:

```bash
widget-builder start cta-a
```

4. After testing the widget locally, you can build and deploy it to your BigCommerce store using the following command:

```bash
widget-builder publish cta-a
```

## Configuration Instructions

Once your widget is installed, you can configure it through the BigCommerce Page Builder interface.

### Layout Configuration

The Design tab includes layout controls that affect the overall structure and spacing of the CTA.

- **Layout Background Color**: Sets the background behind the image and copy.
- **Layout Margin / Padding**: Adjusts outer spacing and internal padding for the CTA container.
- **Layout Grid Gap**: Controls spacing between the image and text columns, with a separate value below the breakpoint.
- **Layout Grid Configuration**: Choose whether the image appears on the left or right on desktop.
- **Swap Layout Below Breakpoint**: Optionally flip the image and copy order on smaller screens.
- **Layout Border Radius**: Rounds the CTA container corners.
- **Center Content Vertically**: Aligns the text vertically with the image.

### Image Settings

- **Image**: Select or upload the CTA image from the Image Manager.
- **Image Alt Text**: Accessibility text used by screen readers.
- **Image Max Width**: Caps the image width as a percentage of its column.
- **Image Border Radius**: Rounds the image corners independently of the layout.

### Title Settings

- **Title Tag**: Choose the heading level for the CTA title.
- **Title Text**: The primary headline shown in the CTA.
- **Title Text Color / Font Size**: Controls title typography.
- **Title Margin**: Spacing around the title, with a separate value below the breakpoint.
- **Title Alignment**: Horizontal alignment, also configurable below the breakpoint.

### Description Settings

- **Description Text**: The supporting body copy below the title.
- **Description Text Color / Font Size**: Controls description typography.
- **Description Margin**: Spacing around the description, with a separate value below the breakpoint.
- **Description Alignment**: Horizontal alignment, also configurable below the breakpoint.

### Action Settings

- **Action Link**: The destination URL for the CTA button or link.
- **Action Text**: The label displayed for the action.
- **Action Font Size**: Controls the CTA label size.
- **Action Colors**: Set text, background, and border colors for default and active states.
- **Action Border Width / Radius**: Controls the CTA outline and corner rounding.
- **Action Padding**: Adds internal spacing within the action element.
- **Action Alignment**: Horizontal alignment, also configurable below the breakpoint.
- **Enable Full Width Action Below Breakpoint**: Expands the action element to full width below the breakpoint setting value.

### Breakpoint Settings

- **Breakpoint Width**: The screen width (in pixels) where mobile/tablet layout and alignment settings take effect.