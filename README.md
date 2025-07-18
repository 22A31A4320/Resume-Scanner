Resume Scanner — Project Documentation:

📌 1. Project Overview
In today’s competitive job market, candidates often apply for multiple roles and must ensure that their resumes align with the job description. Many employers use Applicant Tracking Systems (ATS) that scan resumes for specific keywords to shortlist candidates. Applicants whose resumes lack the right keywords, skills, or relevant experience often do not pass the first screening stage, regardless of their actual capabilities.

The Resume Scanner project addresses this problem. It is an AI-powered web application built with Python, Streamlit, and machine learning tools. It allows users to upload their resume as a PDF file, scans the content, compares it to a given job description, calculates a match percentage, and highlights missing keywords. The result is a clear, actionable report that helps candidates tailor their resumes to match job requirements better, improving their chances of making it through the initial screening process.

🎯 2. Purpose and Goals
The primary goal of this project is to help job seekers optimize their resumes for a specific job description. By giving instant feedback on keyword matches and relevance, the tool:

Helps applicants improve their chances of passing ATS filters.

Provides immediate insights without needing a career coach or expensive resume-writing services.

Encourages users to tailor each application for the role instead of sending generic resumes.

Familiarizes users with the importance of relevant skills and keywords in modern recruitment.

Demonstrates the practical use of Natural Language Processing (NLP) for everyday problems.

⚙️ 3. How It Works
The Resume Scanner is designed to be simple yet effective:

1️⃣ Upload Resume:
Users upload their resume as a PDF file through the Streamlit interface.

2️⃣ Text Extraction:
The app uses PyMuPDF (fitz) to extract raw text from the PDF. PyMuPDF is a fast, lightweight PDF parsing library in Python.

3️⃣ Text Cleaning:
The extracted text is cleaned — converted to lowercase, and special characters are removed using Python’s re module. This ensures that the text is in a uniform format for comparison.

4️⃣ Keyword Matching & Similarity Calculation:
The app uses the TF-IDF Vectorizer and Cosine Similarity from scikit-learn to measure how similar the resume text is to the job description. TF-IDF (Term Frequency-Inverse Document Frequency) highlights important words by weighing their frequency in the document relative to their overall rarity. Cosine similarity calculates the angle between the TF-IDF vectors of the resume and the job description — a common method in NLP to measure how similar two pieces of text are.

5️⃣ Results & Suggestions:
The app displays:

Match Percentage: A clear score out of 100 indicating how well the resume aligns with the job description.

Missing Keywords: A list of keywords present in the job description but missing from the resume. These are displayed as suggestions to help users refine their resumes.

Extracted Resume Text: So users can verify what content was actually scanned.

🔑 4. Core Features
✅ PDF Upload:
Simple drag-and-drop PDF uploader.

✅ Automatic Text Extraction:
Fast, accurate extraction using PyMuPDF.

✅ Cleaning & Preprocessing:
Removes noise for better matching.

✅ Similarity Score:
Calculates how relevant the resume is to the job description.

✅ Keyword Suggestions:
Highlights missing keywords for the user to add.

✅ Full Resume Preview:
Displays what the system read from the uploaded PDF.

✅ Streamlit UI:
An intuitive, modern web interface that works in the browser.

📂 5. Technology Stack
Component	Technology Used
Programming Language	Python
Web Framework	Streamlit
PDF Parser	PyMuPDF
NLP/ML	scikit-learn
Text Similarity	TF-IDF Vectorizer + Cosine Similarity
Public Access	LocalTunnel (optional)

🔧 6. Installation & Usage
Here’s how to set up and run the project:

1️⃣ Clone the Repository:

bash
Copy
Edit
git clone https://github.com/22A31A4320/Resume-Scanner.git
cd Resume-Scanner
2️⃣ Install Dependencies:
Create a virtual environment if you like, then run:

bash
Copy
Edit
pip install streamlit PyMuPDF scikit-learn
3️⃣ Run the App:

bash
Copy
Edit
streamlit run app.py
4️⃣ Optional Public Link:
Expose your local app to the internet using LocalTunnel:

bash
Copy
Edit
npx localtunnel --port 8501
📑 7. File Structure
bash
Copy
Edit
Resume-Scanner/
 ├── app.py                # Main application
 ├── requirements.txt      # Dependencies
 ├── README.md             # Quickstart guide
 ├── LICENSE               # MIT License
 ├── .gitignore            # Files/folders to ignore in version control
📊 8. Detailed Example
Sample Job Description:
“We are looking for a skilled Python developer with experience in machine learning, data analysis, and backend development. Strong knowledge of Python, pandas, scikit-learn, Flask/Django, and REST APIs is required.”

Sample Resume Text:
Suppose the uploaded resume includes “Python, data analysis, backend API design” but does not mention scikit-learn or Flask.

The app will:

Extract this text.

Calculate the match percentage (for example, 72%).

Highlight scikit-learn, Flask, Django, REST as missing keywords.

Suggest adding them where relevant.

📜 9. License
This project is licensed under the MIT License, which is simple and permissive. It allows anyone to freely use, modify, and distribute the software for any purpose, including commercial use, as long as the copyright notice is retained.

🤝 10. Contributing
Contributions are welcome!
You can:

Fork the repository.

Create a feature branch (git checkout -b new-feature).

Commit changes (git commit -m "Add feature").

Push (git push origin new-feature).

Open a pull request.

Possible improvements:

Allow uploading Word documents (.docx).

Support multiple job descriptions.

Visualize more detailed keyword analysis.

Add user authentication to store resumes.

Export matching reports as PDF.

✅ 11. Benefits and Real-World Use
The Resume Scanner is especially useful for:

Job seekers: Tailor resumes to pass ATS filters.

Career coaches: Use it as a tool in coaching sessions.

Recruiters: Provide feedback to candidates.

Students: Learn about keyword optimization in resumes.

By using modern NLP techniques, the app demonstrates a practical way to apply machine learning to solve real-world problems.

📬 12. Conclusion
In summary, the Resume Scanner project is a practical tool built using accessible open-source technologies to help job seekers succeed in a highly competitive job market. By combining PDF parsing, NLP techniques, and an easy-to-use Streamlit interface, it bridges the gap between raw resumes and job-specific requirements, giving users clear, actionable steps to improve their applications.

This project also showcases how simple machine learning concepts like TF-IDF and cosine similarity can have powerful real-life applications. It is a demonstration of how technology can be leveraged to create value for users with minimal setup and maximum impact.
