 READit
This is a simple web application that allows users to load books, view their content, and analyze basic statistics such as the most and least used words. It also includes a search functionality to highlight specific words in the text.

Features
Load Books: Select from a predefined list of books to load and view their content.
Text Statistics:
Document Length (character count).
Total Word Count.
Most and Least Used Words (excluding stopwords).
Search Functionality: Highlight specific words in the loaded text and display the number of matches.
Stopword Filtering: Excludes common words (e.g., "a", "the", "and") from statistical calculations.
Project Structure
Copy
Edit
.
├── books/
│   ├── Book1.txt
│   ├── LOTR.txt
├── index.html
├── script.js
├── style.css
└── README.md
Files and Directories
books/: Directory containing the text files for the books.
index.html: Main HTML file for the user interface.
script.js: JavaScript file containing the logic for book loading, statistics generation, and search functionality.
style.css (optional): Custom CSS for styling the UI (if applicable).
README.md: This file, explaining the project.
How to Use
Clone the Repository:

bash

git clone https://github.com/your-repo/book-reader.git
Add Books:

Place your .txt files inside the books directory.
Update the links in the <ul> inside index.html to include new books:

Edit
<li><a href="#" onclick="loadBook('YourBook.txt', 'Your Book Title')">Your Book Title</a></li>
Open the Project:

Use a local server to run the project. If using VS Code, install the "Live Server" extension and right-click on index.html, then select "Open with Live Server."
Alternatively, use Python's HTTP server:
bash
Copy
Edit
python -m http.server
Open the browser at http://127.0.0.1:8000.
Interact:

Click on a book title to load its content.
View text statistics under the "Book Statistics" section.
Use the search bar to highlight specific words.
Implementation Details
JavaScript Functions
loadBook(filename, displayName): Loads the specified book from the books directory and displays its content.

getDocStats(fileContent): Analyzes the loaded text and computes:

Document length.
Word count.
Most and least used words.
filterStopWords(wordArray): Removes common stopwords from the word array to ensure accurate statistics.

performMark(): Highlights the occurrences of a user-specified keyword in the book text.

sortProperties(obj): Sorts an object by its values in descending order (used for word frequency sorting).

Example Book Entry
If you add a new book (ExampleBook.txt), update the <ul> in index.html like this:

html

<li><a href="#" onclick="loadBook('ExampleBook.txt', 'Example Book')">Example Book</a></li>
Customization
Add More Stopwords: Modify the getStopWords() function in script.js to include additional stopwords:

javascript

return ["a", "the", "and", "is", "in", "of", "to", "it", ...];
Change UI Styling: Edit the CSS within <style> in index.html, or create a separate style.css file for detailed styling.

Future Improvements
Add support for dynamic book uploads using a file input.
Include additional statistics (e.g., sentence count, reading time).
Improve the search functionality to allow case-sensitive searches.
