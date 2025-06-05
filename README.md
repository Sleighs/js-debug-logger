# Debug Logger in Javascrypt/Typescript

### Debug logging utility with call stack tracking and configurable output
 

## Example usage:

### Create a logger instance
`const debug = new DebugLogger({
  debugMode: true, // Enable/disable debug logging
  prefix: '[MyApp]' // Custom prefix for log messages
});`

### Usage examples
`function someFunction() {
  debug.log('This is a debug message');
  try {
    // Some code that might throw
    throw new Error('Something went wrong');
  } catch (error) {
    debug.error('An error occurred', error);
  }
  debug.warn('This is a warning message');
}`

### Console Output Examples:
`[MyApp] [someFunction @ script.js:5] This is a debug message`
`[MyApp] [someFunction @ script.js:11] An error occurred: Error: Something went wrong`
`[MyApp] [someFunction @ script.js:14] This is a warning message`



## To Use
### CommonJS (Node.js)
`const DebugLogger = require('./debug-logger');`

### ES Modules
`import DebugLogger from './debug-logger';`

### Browser (global)
`const debug = new window.DebugLogger();`
