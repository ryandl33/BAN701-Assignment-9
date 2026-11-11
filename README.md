# Sci-Fi Character Generator
BAN701 – Assignment 9: Dual-Approach Feature Development

## Project Description
A Python program that generates random sci-fi characters for tabletop games. Each character gets a name, pronouns, background details, stats, and a random portrait image path. Characters can be exported to an Excel file.

## Features on main
- Random name and pronouns, background details, stats, saves, and HP
- Generate 1–100 characters at a time with input validation
- Random portrait assignment (manual-feature branch)
- Excel (.xlsx) export (ai-feature branch)

## Feature Specifications

### Manual feature: Random Portrait Assignment
- **Purpose:** Give every character a portrait file path.
- **Expected behavior:** Finds the `images/` folder next to the script, searches all subfolders for .jpg/.jpeg/.png files, and picks one at random.
- **Test cases:**
  1. Generate 1 character. Its `image_path` is a valid image path.
  2. Generate 25 characters. Each has a valid `image_path` and the program doesn't error.

### AI feature: Excel Export
- **Purpose:** Let the user save the session's characters to a spreadsheet.
- **Expected behavior:** Menu option 2 writes all generated characters to a formatted .xlsx file in the Downloads folder, with a header row and auto-sized columns.
- **Test cases:**
  1. Generate 3 characters, choose option 2. A file with 3 rows plus a header opens in Excel.
  2. Choose option 2 before generating anything. The program prints a message and creates no file.

## Feature Development Comparison
(150–250 words. Replace the brackets with your real answers.)

On the manual branch I built [how you built the portrait feature, e.g. used os and glob to scan the images folder]. On the AI branch I gave Claude [what you gave it] and it produced an Excel export using openpyxl.

The AI feature [worked / did not work] on the first attempt. [What you changed or rejected, e.g. I resolved a merge conflict where both branches changed the export code. I kept the AI's simpler export and dropped the older version that embedded images.]

[Which approach gave you more confidence and why, e.g. I trusted the manual feature more because I wrote and understood each line, while I had to read and test the AI code line by line before accepting it.]

## How to Run the Program
1. Install Python 3 and the dependency: `pip install openpyxl`
2. Download or clone this repository, keeping the `images/` folder next to `main.py`.
3. Run: `python main.py`
4. Choose a menu option. Exports are saved to your Downloads folder.
