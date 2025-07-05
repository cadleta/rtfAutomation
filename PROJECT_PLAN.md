# Project Plan: rtfAutomation

This project will convert plain numbered text into a formatted RTF/HTML snippet that retains styling when pasted into Microsoft Word.

## Goals
- Accept unformatted text containing numbered sections.
- Apply formatting rules:
  - `#. Title` -> number + title bolded and left-aligned.
  - `#.#.` -> numbers bolded, line indented 0.25"
  - `#.#.#.` -> numbers bolded, line indented 0.5"
- Allow user to copy formatted text and paste into Word with formatting preserved.

## Implementation Choices
- **Language:** JavaScript with HTML/CSS for a lightweight client-side solution. No server dependencies required.
- **Interaction:** Single-page web application where users paste raw text in one textarea and receive formatted HTML output in another.
- **Export:** The formatted output will be rendered in the browser. Users can highlight and copy directly into Word, which preserves formatting via HTML copy/paste.

## Steps
1. Build an HTML page with an input area and an output container.
2. Implement a JavaScript parser that reads each line, determines the numbering depth, and wraps text in `<strong>` tags with appropriate CSS classes for indentation.
3. Style the output with CSS to match the indentation requirements.
4. Provide a "Copy" button that copies the HTML fragment to the clipboard.
5. Document usage instructions in the README.

This approach keeps the project simple, requires no backend, and works offline in modern browsers.
