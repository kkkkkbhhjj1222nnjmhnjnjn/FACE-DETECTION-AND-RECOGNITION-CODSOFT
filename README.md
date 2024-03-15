# FACE-DETECTION-AND-RECOGNITION-CODSOFT

This Python code performs face detection and recognition on an input image using the OpenCV and face_recognition libraries. Here's a description of its key components:

1. Library Imports: The code imports the necessary libraries: cv2 for computer vision tasks and face_recognition for face detection and recognition.

2. Image Loading: It specifies the path to the input image (img_path) and loads the image using OpenCV's cv2.imread() function into the variable img.

3. Face Recognition Model: The code initializes empty lists encodings and names to store the face encodings and corresponding names of known faces, respectively. These will be populated with known face data later for recognition.

4. Screen Size: Sets the screen size for displaying the processed image.

5. Image Preprocessing: Converts the input image from BGR format to RGB format, which is required for face recognition.

6. Face Detection: Utilizes the face_recognition.face_locations() function to detect faces in the image. It returns a list of tuples containing coordinates (top, right, bottom, left) of each detected face.

7. Face Encoding: Extracts face encodings using face_recognition.face_encodings() function, which generates a 128-dimensional numerical representation of each detected face.

8. Face Recognition: Iterates over each detected face, drawing a rectangle around it using OpenCV's cv2.rectangle() function. Then, it compares the face encodings with the known face encodings stored in the encodings list. If a match is found, it retrieves the corresponding name from the names list.

9. Text Overlay: Adds text overlay with the name of the recognized person near each detected face using cv2.putText().

10. Display: Displays the processed image with face detection and recognition results using cv2.imshow().

11. Window Management: Waits for a key press to close the window displaying the processed image and then releases all resources using cv2.destroyAllWindows().

Overall, this code provides a simple demonstration of face detection and recognition in an image, where known faces are matched and labeled accordingly.