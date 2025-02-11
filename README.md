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





# A second automation I tried to work on: 

An automation that sends a daily motivational quote to your email:

# Explanations:

User's Email: The script now gets the user's email address using Session.getActiveUser().getEmail(). This ensures the quote is sent to the correct person.
Quote Sources:
Array of Quotes: The code provides a simple array of motivational quotes. This is easy to use for a small number of quotes. Add as many quotes as you want to the quotes array.
Quote API (Commented out): I've included an example of how to use a quote API. This is a better approach for a larger and more varied selection of quotes. You'll need to find a suitable quote API (many free ones are available) and replace the example API URL with the correct one. Be sure to uncomment this section if you want to use an API.
Error Handling for API: The API example includes a try...catch block to handle potential errors when fetching quotes from the API. This prevents the script from crashing.
Email Sending: The MailApp.sendEmail() function is used to send the email with the quote.
Time-Driven Trigger:
The createDailyTrigger() function sets up a time-driven trigger. This is essential for sending the quote automatically every day. You only need to run this function once to create the trigger.
The trigger is set to run every day at 8:00 AM (you can change the hour).
Crucially: The createDailyTrigger() function now deletes any existing triggers for the sendDailyQuote function before creating a new one. This prevents duplicate triggers from being created if you run createDailyTrigger() multiple times, which would result in multiple emails being sent.
Test Function: The testSendQuote() function allows you to test sending the quote immediately without waiting for the daily trigger. This is very useful for development and debugging.
Clearer Comments: More comments have been added to explain the code.


# How to Use:

Open Apps Script: Go to script.google.com or open a Google Sheet and go to "Tools" > "Script editor".

Copy and Paste: Copy and paste the code into the script editor.

Choose Quote Source: Decide whether you want to use the array of quotes or a quote API. If using an API, uncomment the API code and replace the example URL with the correct one.
Save the Script: Save the script (File > Save). Give it a name (e.g., "DailyQuoteSender").

Run createDailyTrigger(): This is the most important step. Run the createDailyTrigger() function once. Authorize the script when prompted. This will set up the daily trigger.
(Optional) Test: Run the testSendQuote() function to test if the email is being sent correctly.

Check Your Email: Check your email at the scheduled time (e.g., 8:00 AM) to see if you receive the daily quote.
Important:


Authorization: When you run createDailyTrigger() for the first time, you'll need to authorize the script to access your email and set up triggers.

Triggers: You only need to run createDailyTrigger() once. After that, the trigger will run automatically every day. If you run createDailyTrigger() again, it will delete the existing trigger and create a new one, but this is usually unnecessary.

Quote API: If you use a quote API, make sure it's reliable and has a good selection of quotes. Test the API URL in your browser first to make sure it's working.


