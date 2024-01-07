---
{"dg-publish":true,"permalink":"/assets/notion-edu/preparatio/how-to-backup-your-data-from-notion/"}
---

# Research

- Why you should back up your data prepare to move to obsidian one day.
- Everyone loves Notion due to it’s flexibility. You can use it for almost anything. It’s accessibility. The ability to use it on a browser, desktop, phones, tablets and it all syncs together.
- But if you’re like me you’d like to keep the personal knowledge management system you build up over the years. In the case Notion one day goes down along with your data, you’d like a back up system that you can continue your work on like 10 years down the road. I would recommend obsidian as it is hosted on your own computer, future proof, and safe.
- I would recommend to export everything in your notion workspace into markdown and csv files every semester or quater and back it up in a cloud drive to make sure it is safe.
    - I usually back up both the markdown and html files to maintain my rich text formatting for later
        - There is also a way of converting these html files into pdfs for easy viewing even on your phones and I will link it in the cards and description
    - But we also need to download it right now to set it up in obsidian
- Once you got the file, extract it to a folder
    - Once you import it into obsidian, you can see that
        - Your url links still work
        - Simple Formatting such as Italic, Bold, Underline, Strikethrough, Headings, ordered and unordered lists
        - But it has some issues, such as
            - The files having unreasonably long names filled with random characters
            - The mentioned links are markdown links to the file instead of the obsidian internal link which is the cleaner way of writing notes
            - So we’ll use a program or script from github to
                - Which will solve these problems and a few other issues related to the conversion
                - Download and extract the files
            - You’ll also need to [download](https://nodejs.org/en/download/) nodejs to run the script
            - Now open command prompt and cd and the folder directory of the script
                - An easy way to do this is by clicking in the file explorer address bar and copying whats in it
                - once you’ve done that, type ‘node main’
                - it will prompt you to paste the directory of the notion markdown export. You can Use the same method.
                - The command will run and you will see when it finishes
            

- backup your notion into markdown every semester
- write your notes with markdown syntax in mind
    - Even mermaid graphs work
    - rich text colors doesn’t work
    - quote blocks, footnotes [^#] works
    - Page emoji or cover images won’t come with