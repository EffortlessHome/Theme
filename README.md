# EffortlessHome Themes

Welcome to the EffortlessHome Themes repository! This repository contains a collection of themes designed to enhance the visual experience of your Home Assistant dashboard, aligning with EffortlessHome’s clean, modern, and user-friendly design philosophy.

Table of Contents

	•	About
	•	Installation
	•	Available Themes
	•	How to Use
	•	Contributing
	•	License

About

EffortlessHome Themes provide a cohesive and visually appealing interface for Home Assistant users. Whether you’re looking to create a minimalist, dark-themed control panel or prefer a bright and vibrant dashboard, these themes are designed to give your Home Assistant UI a polished and modern look.

EffortlessHome focuses on creating seamless and integrated home automation solutions, and the themes in this repository help maintain a consistent user experience that reflects our brand’s aesthetic.

Installation

To install these themes in your Home Assistant instance:

	1.	Enable Advanced Mode:
Go to Profile in Home Assistant and enable Advanced Mode if it is not already enabled.
	2.	Download the Themes:
Clone or download the themes from this repository to your local machine, or copy the specific theme .yaml file you want to use.
	3.	Add Themes to Your Configuration:
	•	Place the theme files in the /config/themes/ directory. If the themes directory doesn’t exist, create it.
	•	In your configuration.yaml file, add or update the following entry:

frontend:
  themes: !include_dir_merge_named themes


	4.	Reload Themes:
After saving your changes, go to Settings > System > Frontend and click on Reload Themes.
	5.	Apply the Theme:
Once the themes are installed, you can apply a theme by going to Profile and selecting your preferred theme under the Theme dropdown.

Available Themes

Here is a list of some of the available themes in this repository:

	1.	EffortlessHome Dark
A sleek, dark theme with carefully chosen accent colors, ideal for low-light environments and night-time use.
	2.	EffortlessHome Light
A bright and clean theme that enhances visibility and provides a modern feel for day-to-day use.
	3.	EffortlessHome Contrast
A high-contrast theme designed for better accessibility and visibility, suitable for users who need more distinction between elements.
	4.	EffortlessHome Minimal
A minimalist theme focused on reducing distractions, with neutral colors and minimal design elements.

More themes will be added over time to give users a variety of visual styles to choose from!

How to Use

Once you have installed the themes, you can switch between them easily from the Profile section in Home Assistant.

Example

To switch to the EffortlessHome Dark theme:

	1.	Go to Profile in Home Assistant.
	2.	In the Theme dropdown, select EffortlessHome Dark.
	3.	The theme will be applied instantly to your UI.

You can also automate theme changes based on time or events (e.g., switch to the dark theme at sunset) by using Home Assistant automations.

automation:
  - alias: 'Switch to Dark Theme at Sunset'
    trigger:
      platform: sun
      event: sunset
    action:
      service: frontend.set_theme
      data:
        name: EffortlessHome Dark

Contributing

We welcome community contributions! If you have a theme that complements the EffortlessHome aesthetic, or if you’d like to improve an existing theme, feel free to submit a pull request.

Please ensure your theme contributions follow the general design guidelines of simplicity, usability, and aesthetic consistency. Make sure to test your theme on various devices and screen sizes for optimal display.

For bug reports or feature requests, please open an issue in this repository.

License

This repository is licensed under the MIT License. See the LICENSE file for more details.

This README.md gives users a clear guide on how to install and use themes in Home Assistant, along with how they can contribute to the repository. You can update the “Available Themes” section with more details as the collection grows.