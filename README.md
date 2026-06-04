# Lab 9 - JavaScript Error Handling, Monitoring, & JS Docs

**Name:** Ajay Anubolu


**Deployed GitHub Pages URL:** https://ajanubolu.github.io/Lab9_Starter/

## What this demonstrates

Open the browser DevTools console (F12) and interact with the page.

### Step 2 - Console methods
Each button in the bottom section calls one `console` method on some sample
data: `console.log`, `console.error`, `console.count`, `console.warn`,
`console.assert`, `console.clear`, `console.dir`, `console.dirxml`,
`console.group` / `console.groupEnd`, `console.table`, `console.time` /
`console.timeEnd`, and `console.trace`.

### Step 3 - try / catch / finally + throw
The Error Calculator validates its inputs and **throws** on bad input (empty
fields, non-numeric input, or divide-by-zero). The throw is handled in a
`try / catch / finally` block: the `catch` reports the error in the output box
and to the console, and the `finally` block always logs that the attempt
completed.

### Step 4 - Custom errors
`CalculatorError extends Error`, and `DivideByZeroError extends CalculatorError`.
The `catch` block uses `instanceof` to give a different message per error type.

### Step 5 - Global error handler + 3rd party monitoring
The **"Trigger a Global Error"** button calls an undefined function, which
throws *outside* any try/catch. It is caught two ways:
- `window.onerror` (the classic approach from the professor's ajaxref demo)
- `window.addEventListener('error', ...)` (the modern approach)

Both log the caught error to the console. **TrackJS** is integrated via the
agent script in `<head>`.

## TrackJS
TrackJS is configured with a live token (application `lab-9-starter`). Errors
triggered on the deployed site are reported to the TrackJS dashboard. See
`trackjs-screenshot.png` for the captured error report (username + error list).

