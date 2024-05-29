# JavaScript Documentation

## Overview

This JavaScript file contains handlers and functionality to enhance form validation, interface interactions, AJAX operations, and content dynamics in a public-facing web application. It utilizes jQuery and integrates with third-party libraries like TinyMCE and Slick carousel.

## Functionality Breakdown

### Form Validation

```
var forms = document.querySelectorAll(".needs-validation");
```

- Operation: Prevents form submission if validation fails and adds Bootstrap validation styles.
- Purpose: Implements custom validation on forms that have the class .needs-validation.

### Carousel Setup with Slick

```
$(".client-logos").slick({...});
```

- Purpose: Initializes the Slick carousel for elements with the class .client-logos.
- Details: Configures settings such as number of slides to show and scroll, responsiveness at different breakpoints, and whether to show dots and arrows.

### Country and State Dynamic Selector

```
$.getJSON(scriptParams.countryJsonUrl, function (data) {...});
```

- Purpose: Dynamically populates country and state dropdowns based on a JSON file loaded from a server.
- Details: Disables state selector until a country is chosen, then loads states for the selected country.

### Breadcrumb Traversal for Multi-Step Forms

```
$("#progress-button-1").click(function () {...});
```

- Purpose: Manages visibility of different sections of a multi-step form when navigating through steps using progress buttons.
- Details: Each button click shows the associated step and hides others, and updates the progress bar.

### Form Submission and Validation

```
$("#stepone").click(function () {...});
```

- Purpose: Handles client-side validation for a multi-step form's first step.
- Details: Checks the validity of input fields like full name, email, and job title, and only proceeds if all validations pass.

### TinyMCE Editor Initialization

```
tinymce.init({...});
```

- Purpose: Initializes TinyMCE editors for text areas where rich text editing is required.
- Details: Configures toolbars, plugins, and setup functions that hide validation messages on keyup events if content is present.

### AJAX Pagination for Loading More Press Releases

```
$(".load-more-btn").on("click", function () {...});
```

- Purpose: Implements load more functionality for press releases using AJAX.
- Details: Loads additional press releases from the server when the user clicks the "load more" button and updates the UI accordingly.

### Input Character Count Validation

```
$("#PressReleaseSubHeadline").on("input", function () {...});
```

- Purpose: Checks the number of characters entered in an input box and displays the count.
- Details: Ensures that the character count does not exceed a maximum limit, providing visual feedback to the user.

### Date Picker Initialization and Validation

```
var schedule_date = document.getElementById("PressReleasePublishDate");
```

- Purpose: Sets valid date ranges for a date picker input.
- Details: Configures the date input to allow only dates between two and ninety days from the current date.

### Utility Functions for Preview Updates

- Purpose: Updates previews of press release content, contact information, and images based on user input.
- Details: Functions like updatePressReleaseContent and updatePressReleaseContactInformation dynamically update HTML content to show a preview of the press release. The addImage function manages image previews when files are selected.
