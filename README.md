# Markdown to Google Docs Converter

A Python script (Colab Notebook) that converts markdown meeting notes into a well-formatted Google Doc using the Google Docs API.

## Features

- Reads markdown text.
- Uses Google Docs API to create a new Google Doc.
- Automatically applies heading styles (H1, H2, H3).
- Maintains bullet hierarchy from markdown.
- Converts `- [ ]` text into interactive checkboxes in Google Docs.
- Highlights mentions (`@name`) in bold text.
- Styles footer in a distinct paragraph style.

## Setup Instructions

1. **Clone the repository**:

   ```bash
   mkdir AnsibleHealthOA
   cd AnsibleHealthOA
   git clone https://github.com/peimanfth/MdToDocs.git

   ```

2. **Using the notebook**:

- Download the notebook and upload it into colab.
- You can run the code block to start the script.
- pip dependencies needed to be added to the colab environment are automatically downloaded as part of the script. Therefore there is no need to install pip dependencies manually before executing the script.
- to authenticate your credentials you can either be log into your account when prompted by the API. You can also use the JSON file generated by Google Cloud Console in the colab environment to automatically authenticate.
- after authenticating the program parses the text using regular expresion and converts line by line. Then all the requests are batch and commited into the already created google docs file. You can see the succesful creation message or the corresponding error in case of failure.
- Next you can log into you google docs web page to check the uploaded file and its contents. You could also click on the link printed at the end of the script.
