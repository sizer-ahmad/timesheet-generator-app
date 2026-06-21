# Timesheet Generator

The **Timesheet Generator** is a lightweight, browser-based utility designed for the **Deltapath - Enosis QA Automation Team**. It parses weekly markdown timesheet entries, performs automated calculations for daily and weekly durations, and exports the result as a professionally styled, formatted Excel (`.xlsx`) file.

---

## Key Features

- **Zero-Server Architecture**: Runs entirely in your browser. Your data never leaves your machine.
- **Intelligent Parsing**: Uses a Virtual DOM tree walker to extract tasks, projects, and resources from your markdown documents, ignoring irrelevant sections.
- **Automated Calculations**: Automatically injects "Daily Total" rows and a grand "WEEKLY TOTAL" row.
- **Dark / Light Mode**:
  - Dark mode is set as the default.
  - Active icon is highlighted; inactive icon is faded for clear visual feedback.
  - Selected theme persists across page reloads via `localStorage`.
- **Live Stats Panel**: Displays **Resources Found**, **Total Duration**, and **Time Period** (`DD-Mon-YY to DD-Mon-YY` format) after processing.
- **Rich Excel Styling**:
  - Bold, black-fill headers with white text.
  - Wrap-text and middle-alignment applied to all rows.
  - Color-coded "Total" rows for easy reading.
- **Smart Filename Generation**: Automatically generates files named `Deltapath_Enosis_QA_Timesheet_YYMMDD_YYMMDD.xlsx` where the start date is always the **Monday** and end date is the **Sunday** of the data's week — regardless of which specific days have entries.
- **File Support**: Direct support for uploading `.md` or `.txt` files in addition to standard copy-pasting.

---

## How to Use

1. **Open the Application**: Go to the app: [link](https://sizer-ahmad.github.io/timesheet-generator-app/).
2. **Input Data**:
   - **Option A**: Paste your weekly markdown content directly into the text area.
   - **Option B**: Click "Upload File" to select a `.md` or `.txt` file from your computer.
3. **Process**: Click the **Parse & Process Data** button. The app will validate your structure and display a live preview of the generated table.
4. **Review Stats**: Check the **Resources Found**, **Total Duration**, and **Time Period** cards to confirm the data was parsed correctly.
5. **Download**: If the data is correct, the **Download Formatted Excel** button will activate. Click it to save your generated report.

---

## Required Markdown Format

To ensure the parser identifies your data correctly, please use the following structure:

```markdown
## Monday (June 15, 2026)

### Resource 1: Name

| Activity      | Description                | Time Spent |
| :------------ | :------------------------- | :--------- |
| Development   | Task#01 - Task Description | 4          |
| Communication | Meetings                   | 0.5        |

### Resource 2: Name

| Activity      | Description                | Time Spent |
| :------------ | :------------------------- | :--------- |
| Development   | Task#02 - Task Description | 3          |
| Communication | Meetings                   | 0.5        |

## Tuesday (June 16, 2026)

...
```

- **Header Format**: Days must follow `## DayName (Date)`.
- **Resource Format**: Resource names must follow `### Resource Name`.
- **Table Format**: Must include a column containing `Time Spent`, `Hrs`, or `Time`.

---

## Technologies Used

| Library                                                  | Purpose                                                        |
| :------------------------------------------------------- | :------------------------------------------------------------- |
| [Tailwind CSS](https://tailwindcss.com/)                 | Responsive, modern user interface with dark/light mode support |
| [ExcelJS](https://github.com/exceljs/exceljs)            | Generating styled, professional Excel spreadsheets             |
| [FileSaver.js](https://github.com/eligrey/FileSaver.js/) | Triggering the file download locally                           |
| [Lucide Icons](https://lucide.dev/)                      | Clean, scalable iconography                                    |

---

## Support & Credits

Developed for the internal use of the **[Deltapath](https://www.deltapath.com/) - [Enosis](https://www.enosisbd.com/) QA Automation Team © 2026**
