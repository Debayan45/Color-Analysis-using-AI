# Color-Analysis-using-AI
Project Title:
Color Analysis using AI for Dress Recommendation

🧩 Project Overview:
This project takes a user-uploaded image, detects their skin tone, eye (pupil) color, and hair color using image processing techniques, and then recommends suitable dress colors by sending this data to an external API.

✅ Key Components and Technologies Used:
1. Python (Programming Language)
The entire logic is written in Python due to its rich ecosystem of libraries for image processing, machine learning, and data handling.

2. OpenCV (cv2) — Image Processing
Purpose: Reading and analyzing images.

What It Did:

Converted image to different color spaces (like HSV for skin detection, grayscale for eye detection).

Detected facial regions and eyes using Haar Cascade classifiers.

Extracted the top portion of the image to approximate hair color.

3. NumPy — Array Manipulation
Purpose: Efficiently handle image data.

What It Did:

Manipulated pixel arrays (which are large matrices).

Removed black or zero-value pixels for accurate color detection.

4. scikit-learn (KMeans) — Dominant Color Extraction
Purpose: Find the most prominent color in a region (like skin, eyes, or hair).

What It Did:

Flattened image regions into a 2D pixel list.

Used the KMeans clustering algorithm to identify the dominant color.

5. Matplotlib — Data Visualization
Purpose: Display the results visually.

What It Did:

Showed color swatches of detected skin tone, eye color, and hair color.

Helped visually confirm the accuracy of color extraction.

6. Google Colab + google.colab.files — File Upload
Purpose: Let users upload images for analysis.

What It Did:

Used the files.upload() function to allow image uploads directly in the notebook interface.

7. Requests — API Integration
Purpose: Connect to an external system for color recommendations.

What It Did:

Sent extracted RGB values for skin, eye, and hair to a mock or real API.

Received a list of suggested dress colors based on those features.

🧠 Optional/Backend (If extended further):
Flask or FastAPI can be used to build the backend API that receives RGB inputs and returns dress suggestions using predefined rules or a trained model.

Database (optional): Could be used to store skin-tone profiles and fashion palettes.

💡 How It Works (In Simple Steps):
The user uploads an image.

The system detects skin, eye, and hair regions.

It extracts the dominant RGB color from each region.

These RGB values are sent to an API.

The API returns suggested dress colors based on aesthetic compatibility.

The results are shown as readable text and visual color patches.

