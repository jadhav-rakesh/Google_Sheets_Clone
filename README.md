# Spreadsheet Application - Functionalities Overview  

## 1. Cell Navigation & Selection  
- **Arrow Key Navigation**: Moves the selected cell using arrow keys.  
- **Shift + Arrow Keys**: Expands the selection range while holding Shift.  
- **Enter Key Handling**:  
  - If not in editing mode, it opens the input field for the selected cell.  
  - If already in editing mode, it moves down to the next cell and returns to **NORMAL** mode.  

## 2. Cell Input & Editing  
- Displays an input field when a user starts typing.  
- Dynamically adjusts the input box position and size based on cell dimensions.  
- Changes `mode` based on user actions:  
  - **NORMAL**: Default mode (navigation, selection).  
  - **TYPING**: When editing a cell.  
  - **SEARCHING**: When a formula is being entered (`=`, `+`, etc.).  

## 3. Formula Handling & Dependency Tracking  
- Detects formulas (e.g., `=SUM(A1:B2)`) and highlights dependent cells.  
- Extracts cell references from formulas using regex.  
- Handles cell ranges (`A1:C3`) and expands them into individual cell dependencies.  
- Tracks formula dependencies and updates affected cells when values change.  

## 4. Deleting Cell Content & Managing Dependencies  
- Deletes content from a single cell or a selected range.  
- Removes formulas linked to the deleted cells.  
- Updates **dependent formulas** to reflect changes.  

## 5. Grid Rendering & UI Updates  
- Refreshes the spreadsheet grid after any major action (navigation, editing, deletion).  
- Visually highlights cells when entering a formula.  
- Draws a blue outline around the active cell when typing.  

## 6. Event Listeners for User Input  
- Listens for keyboard events (`keydown`) to handle navigation, selection, editing, and deletion.  
- Detects when a formula is being entered and switches to **SEARCHING** mode.  
- Prevents default browser actions for keys like `Arrow keys`, `Enter`, and `Backspace` when applicable.  

## 7. Spreadsheet Data Management  
- Stores cell values in a `spreadsheetData` structure.  
- Maintains a mapping of formulas (`formulaInCell`) and their dependent cells (`executionsDependentOnCell`).  
- Converts between **cell names** (e.g., `"B2"`) and **row/column indices**.  

---

## 🚀 Overall Purpose  
The code implements a **basic spreadsheet application** with support for:  
✅ Cell navigation & selection  
✅ Data entry & inline editing  
✅ Formula handling & dependency tracking  
✅ Deletion & dynamic updates  
✅ Interactive UI with real-time grid updates  

Would you like help with adding features like **copy-paste, undo-redo, or advanced formulas**? 🚀  
