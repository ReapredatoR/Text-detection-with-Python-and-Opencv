This code exemplifies text detection in images using EasyOCR and OpenCV, focusing on English text, GPU acceleration, and a manually set confidence threshold.

A step-by-step explanation of the code

_Before running the code, I installed the required Python libraries._

- easyocr
- matplotlib
- opencv
- numpy

1. Importing Packages:

   - Import necessary Python libraries for image processing, text detection, and visualisation.

2. Read the Image Using OpenCV:

   - Load an image file named "2.jpg" from the "images" directory using OpenCV.

3. Text Detector Instance (EasyOCR):

   - Create an EasyOCR Reader instance specifically configured for English text detection.
   - Utilize GPU acceleration for faster processing, but note that this can be adjusted to `gpu=False` if GPU is unavailable.

4. Detecting Text and Assigning Values:

   - Use the EasyOCR Reader to detect text in the loaded image.
   - Assign the results, including bounding box coordinates, detected text, and confidence scores, to the variable `r_text`.

5. Results Display:

   - Print the detected text, bounding box coordinates, and confidence scores for each identified text region.

6. Setting a Threshold and Drawing Bounding Boxes:

   - Define a confidence threshold (0.25) to filter out text regions with lower confidence scores.
   - Iterate through the detected text regions and draw bounding boxes using the upper left corner (`bbox[0]`) and the bottom right corner (`bbox[2]`).

7. Displaying the Final Result:
   - Convert the image to RGB format (required by Matplotlib) and display the final result with the drawn bounding boxes.
