# BigCommerce Widget: Product Pinboard

A custom product pinboard widget for BigCommerce Page Builder with interactive pins, tooltips, and a synced product card carousel.

[Design Specification](design.png)

<img src="./example.gif" width="600" alt="Product Pinboard Example GIF">

## Features

- **Interactive Pins**: Clickable pins on the product image that open tooltips with product details.
- **Product Card Carousel**: A carousel that displays product cards corresponding to the pins, synchronized with the pin interactions.
- **Responsive Design**: The widget is designed to be responsive and works well on both desktop and mobile devices.
- **Customizable**: Easily customize the appearance and behavior of the pins, tooltips, and carousel through CSS and JavaScript.

## Prerequisites

Before you begin installing the Product Pinboard widget, ensure you have the following:

- A BigCommerce store with access to the control panel.
- A BigCommerce theme that supports Page Builder.
- API credentials for your BigCommerce store to authenticate the Widget Builder CLI tool.

## Installation Instructions

To install the Product Pinboard widget in your BigCommerce theme, follow these steps:

### Setting Up the Widget Builder CLI

1. In your terminal, navigate to the root directory of the BigCommerce theme you want to install the widget in.

2. Clone the BigCommerce [widget-builder](https://github.com/bigcommerce/widget-builder) repository.

3. Follow the instructions in the widget-builder repository to set up the CLI tool.

### Installing the Widget

1. Run the following command to create a new widget (you can replace `product-pinboard` with your desired widget name):

```bash
widget-builder create product-pinboard
```

2. After creating the widget, replace the generated files with the corresponding files from the `src/` directory of this repository.

3. Once you have replaced the files, you can run the widget locally to test it and ensure that everything is working correctly:

```bash
widget-builder start product-pinboard
```

> Note: The widget will initially appear without products. To see the pins and the carousel working, you will need to provide real product IDs from your BigCommerce store in the pins array within `config.json`.

4. After testing the widget locally, you can build and deploy it to your BigCommerce store using the following command:

```bash
widget-builder publish product-pinboard
```

## Configuration Instructions

Once your widget is installed, you can configure it through the BigCommerce Page Builder interface. 

### Pin Configuration

The main configuration panel for the widget contains two dropdowns worth of settings for the product pins. In the first dropdown, you can add more pins by clicking the plus button on the top dropdown and reorder them using drag-and-drop. Pins can also be removed by clicking the ellipse button on the right of each pin. 

The second dropdown contains position and product selection settings for each pin. You can cycle through the pins by clicking the left and right arrows on the top of the secondary tab. For each pin, you will need to set the following:
- **Position**: The X and Y coordinates for the current pin. These values are expressed as percentages, so if you want a pin to be in the middle of the image, you would set both X and Y to 50.
- **Product**: The product ID that corresponds to the current pin. To find the product ID, navigate to the Products section of your BigCommerce control panel and click on the product you want to use. The product ID will be in the URL as the last segment (e.g., `https://store-xyz.mybigcommerce.com/manage/products/123` - in this case, `123` is the product ID).

### Settings Configuration

The widget settings tab can be accessed by clicking the ellipsis button on the top right of the widget configuration panel. This tab contains configuration for the pinboard title, description and image. It also includes a number of styling settings for pins, tooltips, product carousel and more. The following sections will cover the relevant fields.

#### Pinboard Header Settings

- **Pinboard Title**: The title of the pinboard, displayed above the product image.
  - If left blank, the title section will not be rendered, allowing for a cleaner look if a title is not necessary.
- **Pinboard Title Text Color**: The color of the pinboard title text.
- **Pinboard Title Font Size**: The font size of the pinboard title, measured in pixels.
- **Pinboard Description**: A short description of the pinboard, displayed below the title.
  - Similar to the title, if left blank, the description section will not be rendered.
- **Pinboard Description Text Color**: The color of the pinboard description text.
- **Pinboard Description Font Size**: The font size of the pinboard description, measured in pixels.

#### Pinboard Image Settings

- **Main Image**: The main image for the pinboard where the pins will be placed. This should ideally be an image that showcases the products being pinned.
    - You can use the Image Manager to upload and select an image from your BigCommerce store or provide an external image URL.
- **Pinboard Image Alt Text**: A text description of the pinboard image for accessibility purposes. This is important for users who rely on screen readers and for SEO.

#### Breakpoint Settings

- **Tablet Breakpoint Width**
  - The screen width (in pixels) at which the widget will switch to tablet layout. Below this width, the widget will adjust its layout to better fit smaller screens.
- **Mobile Breakpoint Width**
    - The screen width (in pixels) at which the widget will switch to mobile layout. Below this width, the widget will further adjust its layout for optimal display on mobile devices.
- **Show Product Card Above Image**
  - A toggle setting that allows you to choose whether the product card carousel is displayed above the pinboard image on mobile devices. Enabling this setting can improve the user experience on smaller screens by making the product information more immediately visible.

#### Pin Settings

- **Pin Default Size**: The default size of the pins, measured in pixels.
- **Pin Default Color**: The default color of the pins on the pinboard image.
- **Pin Default Border Color**: The default border color of the pins on the pinboard image.
- **Pin Active Size**: The size of the pins when a user hovers over them with their mouse cursor, clicks them or focuses on them using keyboard navigation, measured in pixels.
- **Pin Active Color**: The color of the pins when a user hovers over them with their mouse cursor, clicks them or focuses on them using keyboard navigation.
- **Pin Active Border Color**: The border color of the pins when a user hovers over them with their mouse cursor, clicks them or focuses on them using keyboard navigation.

#### Product Card Settings

- **Card Background Color**: The background color of the product cards in the carousel.
- **Card Border Color**: The border color of the product cards in the carousel.
- **Card Link Color**: The color of the product name link in the product cards.
- **Card Border Radius**: The border radius of the product cards in the carousel, measured in pixels.
- **Show Product Card SKU**: A toggle setting that allows you to choose whether to display the product SKU on the product cards in the carousel.