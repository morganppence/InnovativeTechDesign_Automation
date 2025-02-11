# InnovativeTechDesign_Automation
Create an AI driven automation

# About 
For this project I wanted to leverage AI to streamline the interview analysis process by using Google Apps Script to automatically sort and summarize information from PDFs. By integrating AI-driven natural language processing, the script efficiently extracts key insights, categorizes responses, and organizes data for easier review.  

# Summary of Project

I was inspired to go this direction becuase I think it could be helpful in my current academic life. Designed for professionals conducting user interviews, hiring managers, or researchers, this tool reduces the manual effort required to process large amounts of qualitative data. The result is a smarter, more efficient workflow that enhances decision-making and saves time.  


# Tools used
- Gemini 
- ChatGPT

# Key Improvements and Explanations:

- HTML Service: The code now includes a basic HTML file (index.html) with a file upload form. This is essential for the user to select the PDF. The HTML and Apps Script communicate using google.script.run.

- File Upload: The HTML form uses FormData to correctly send the file to the Apps Script server-side function.
Error Handling: Basic error handling is included to catch issues like incorrect file types or problems with PDF processing. The displayError function in the HTML shows these errors to the user.

- JSON Handling: The server-side script now returns the results (interview data and summary) as a JSON string. The client-side JavaScript then parses this JSON to display the data properly. This is much better than trying to inject HTML directly from the server.
Placeholder for PDF Parsing: The extractTextFromPDF function is a placeholder. You must replace this with code that uses a PDF parsing library or API. I've mentioned some options in the comments. This is the most crucial part to implement.

- Basic Information Extraction and Sorting: The extractInterviewInfo function is also a placeholder, but it provides a starting point. You'll need to customize the regular expressions or other logic to match the specific format of your interview PDFs. The example sorts the data by candidate name.
Basic Summarization: The summarizeInterviews function now does a simple keyword count. This is a very basic form of summarization. For more meaningful summaries, you'll need to use more advanced NLP techniques (e.g., sentiment analysis, topic modeling, etc.) using libraries like the Google Cloud Natural Language API.

- Clearer Comments: I've added more comments to explain each part of the code.

# Steps to Use:
1. Create Apps Script Project: In Google Drive, create a new Apps Script project.
2. Copy Code: Copy and paste the provided code into the Apps Script editor.
3. Replace Placeholders: Crucially, replace the

# What I Learned 

Working on this project provided valuable insights into AI-driven automation and the power of Google Apps Script in streamlining workflows.

- AI-Powered Text Processing – Leveraging AI to extract and summarize information from PDFs significantly reduces manual effort and enhances efficiency.  
- Google Apps Script Capabilities – I learned how to automate document handling, text parsing, and data organization within Google’s ecosystem.  
- Optimizing Data Structuring – I gained experience in categorizing and sorting qualitative data in a way that improves accessibility and usability.  
- Debugging and Iteration – I encountered and resolved challenges related to parsing accuracy, formatting inconsistencies, and script execution limits.  

This project reinforced the value of AI-driven automation in improving productivity and provided hands-on experience in integrating technology to solve real-world problems.  
