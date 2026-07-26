# Navbar & Notification System

A clean, modern navigation component with sliding sidebars and a minimal notification toast system.


## Technologies Used

- HTML5
- CSS3 (transitions, flexbox, custom properties)
- Vanilla JavaScript (ES6)

## Notification API

```javascript
// Basic notification with default type (none)
notification.trigger('Hello World!')

// Info type
notification.trigger('This is an info message', 'info')

// Success type
notification.trigger('Operation completed successfully!', 'success')

// Error type
notification.trigger('Something went wrong!', 'error')

// None type (explicit)
notification.trigger('Plain notification', 'none')

// Multiple notifications in sequence
notification.trigger('First toast', 'info')
setTimeout(() => {
  notification.trigger('Second toast', 'success')
}, 500)
setTimeout(() => {
  notification.trigger('Third toast', 'error')
}, 1000)

// Long message
notification.trigger('This is a very long notification message that will still display properly', 'info')

// Empty message fallback
notification.trigger('', 'success')

// Invalid type falls back to 'none'
notification.trigger('Invalid type test', 'warning')