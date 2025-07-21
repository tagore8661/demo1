# HTML Input Types Reference

This document provides a comprehensive reference of all HTML input types in alphabetical order.

## Button
```html
<input type="button" value="Click Me">
```
- Creates a clickable button
- Use `value` attribute to set button text
- No default behavior, requires JavaScript for functionality

## Checkbox
```html
<input type="checkbox" id="agree" name="agree" value="yes">
<label for="agree">I agree to the terms</label>
```
- Creates a checkbox for boolean values
- Use `checked` attribute to pre-select
- Multiple checkboxes can have the same name for multiple selections

## Color
```html
<input type="color" id="favcolor" name="favcolor" value="#ff0000">
```
- Creates a color picker
- Returns hex color value (e.g., #ff0000)
- Default value is #000000 (black)

## Date
```html
<input type="date" id="birthday" name="birthday" min="1900-01-01" max="2023-12-31">
```
- Creates a date picker
- Format: YYYY-MM-DD
- Use `min` and `max` attributes to set date range

## Datetime-local
```html
<input type="datetime-local" id="meeting" name="meeting">
```
- Creates a date and time picker (no timezone)
- Format: YYYY-MM-DDTHH:MM
- Combines date and time selection

## Email
```html
<input type="email" id="email" name="email" placeholder="user@example.com">
```
- Creates an email input field
- Built-in email validation
- Mobile keyboards show @ symbol
- Use `multiple` attribute to allow multiple emails

## File
```html
<input type="file" id="upload" name="upload" accept=".jpg,.png,.pdf">
```
- Creates a file upload button
- Use `accept` attribute to specify file types
- Use `multiple` attribute to allow multiple files

## Hidden
```html
<input type="hidden" name="csrf_token" value="abc123">
```
- Creates a hidden input field
- Not visible to users
- Used to store data that needs to be submitted with the form

## Image
```html
<input type="image" src="submit-button.png" alt="Submit" width="100" height="30">
```
- Creates an image that acts as a submit button
- Requires `src` attribute for image source
- Submits x,y coordinates of click

## Month
```html
<input type="month" id="start" name="start" min="2020-01" max="2023-12">
```
- Creates a month and year picker
- Format: YYYY-MM
- Use `min` and `max` attributes to set range

## Number
```html
<input type="number" id="quantity" name="quantity" min="1" max="100" step="1">
```
- Creates a numeric input field
- Use `min`, `max`, and `step` attributes to control range and increments
- Shows spinner controls on desktop

## Password
```html
<input type="password" id="pwd" name="pwd" minlength="8" maxlength="20">
```
- Creates a password input field
- Text is masked with dots or asterisks
- Use `minlength` and `maxlength` for validation

## Radio
```html
<input type="radio" id="small" name="size" value="small">
<label for="small">Small</label>
<input type="radio" id="medium" name="size" value="medium">
<label for="medium">Medium</label>
<input type="radio" id="large" name="size" value="large">
<label for="large">Large</label>
```
- Creates radio buttons for single selection
- All radio buttons in a group must have the same `name`
- Use `checked` attribute to pre-select

## Range
```html
<input type="range" id="volume" name="volume" min="0" max="100" value="50">
```
- Creates a slider control
- Use `min`, `max`, `value`, and `step` attributes
- Default range is 0 to 100

## Reset
```html
<input type="reset" value="Clear Form">
```
- Creates a reset button
- Clears all form fields to their default values
- Use sparingly as it can be destructive

## Search
```html
<input type="search" id="search" name="search" placeholder="Search...">
```
- Creates a search input field
- May show a clear button (×) when text is entered
- Semantically indicates search functionality

## Submit
```html
<input type="submit" value="Submit Form">
```
- Creates a submit button
- Submits the form when clicked
- Use `value` attribute to set button text

## Tel
```html
<input type="tel" id="phone" name="phone" placeholder="(123) 456-7890">
```
- Creates a telephone number input field
- Mobile keyboards show numeric keypad
- No built-in validation (format varies by country)

## Text
```html
<input type="text" id="name" name="name" placeholder="Enter your name" maxlength="50">
```
- Creates a single-line text input field
- Default input type if type is not specified
- Use `maxlength` and `minlength` for validation

## Time
```html
<input type="time" id="appt" name="appt" min="09:00" max="18:00">
```
- Creates a time picker
- Format: HH:MM (24-hour format)
- Use `min` and `max` attributes to set time range

## Url
```html
<input type="url" id="website" name="website" placeholder="https://example.com">
```
- Creates a URL input field
- Built-in URL validation
- Mobile keyboards may show .com button

## Week
```html
<input type="week" id="week" name="week" min="2020-W01" max="2023-W52">
```
- Creates a week picker
- Format: YYYY-WNN (year and week number)
- Use `min` and `max` attributes to set range

## Common Attributes

### Global Attributes (work with most input types):
- `id` - Unique identifier
- `name` - Name for form submission
- `value` - Default/current value
- `placeholder` - Hint text
- `required` - Makes field mandatory
- `disabled` - Disables the input
- `readonly` - Makes input read-only
- `autofocus` - Automatically focuses on page load
- `autocomplete` - Controls browser autocomplete

### Validation Attributes:
- `required` - Field must be filled
- `pattern` - Regular expression for validation
- `min` / `max` - Minimum/maximum values
- `minlength` / `maxlength` - Minimum/maximum character length
- `step` - Increment value for numeric inputs

### Example with Multiple Attributes:
```html
<input type="email" 
       id="user-email" 
       name="email" 
       placeholder="Enter your email" 
       required 
       autocomplete="email"
       pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$">
```

## Browser Support Notes

- Most input types are well-supported in modern browsers
- Older browsers may fall back to `type="text"` for unsupported types
- Always test across different browsers and devices
- Consider using polyfills for older browser support
- Mobile browsers often provide specialized keyboards for different input types

## Accessibility Considerations

- Always use `<label>` elements with inputs
- Use `aria-describedby` for additional descriptions
- Provide clear error messages for validation
- Ensure sufficient color contrast
- Test with screen readers
- Use semantic HTML5 input types for better accessibility

## Best Practices

1. Choose the most appropriate input type for your data
2. Always include proper labels
3. Use placeholder text as hints, not labels
4. Implement client-side and server-side validation
5. Provide clear error messages
6. Test on mobile devices
7. Consider user experience and accessibility
8. Use appropriate autocomplete attributes