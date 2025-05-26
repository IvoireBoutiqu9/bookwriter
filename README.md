# Instant book generation using OpenAI's Large Language Models

Bookwriter is an app that lets you generate an entire book (structure and content) using OpenAI's text generation API.\
Currently this app uses gpt-3.5-turbo, the same model that powers chatGPT.\
First the outline of the book is generated (chapters, sections and subsections), and then each subsection is expanded into "parts".\
The content of each part is then generated, yielding a complete book.

# Before using the app

You need to provide your OpenAI API key by creating a file named ".env" at the root of the repo.\
The content of the file should be as follows:
```
REACT_APP_OPENAI_API_KEY='sk-proj-zNWyd2se7DimPa4vcunAAb7EJ5HCctKBLPq-_hW7ONnCRSp6IJyxIGdCsmR0F1'
```

# Start the app

Run `npm start` to launch the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

# First step: Description of the book

![Book description input](/description.png)

Enter what would be the title of your book, and a short description of it.

# Second step: Generation of the outline

![Outline generation and parsing](/outline_generation.png)

Here you can generate the outline of the book.\
The result of the generation is displayed on the top. You can edit the text manually or re-generate over.\
Once you're satisfied, click "parse" to make the app parse the text.\
Please note that:
- Chapters must be in the form "Chapter XX. Title of the chapter"
- Sections must be in the form "\tSection Y. Section name" (notice the \t representing a single tab character)
- Subsections must be in the form "\t\t-Title of subsection" (notice the 2 tabs \t this time)

This format was chosen because it seems to work best for GPT 3.5

# Third step: Parts and contents of the book

![Parts and content generation](/content_generation.png)

Select a an item/subsection on the left panel and generate appropriate parts on the right.\
You can manually remove some parts of re-generate them all.\
Once you have selected a part, you can generate the content associated with it.

# License

GNU General Public License v3.0
