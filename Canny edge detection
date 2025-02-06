import cv2
import os

# Input and output directories
input_folder = "DRIVE_Dataset/"
output_folder = "Canny_output/"
os.makedirs(output_folder, exist_ok=True)

# Process all images
for filename in os.listdir(input_folder):
    if filename.endswith(".tif") or filename.endswith(".jpg"):
        image = cv2.imread(os.path.join(input_folder, filename), cv2.IMREAD_GRAYSCALE)

        # Apply Canny Edge Detection
        edges = cv2.Canny(image, 50, 150)

        # Save the result
        cv2.imwrite(os.path.join(output_folder, filename), edges)

print("Canny Edge Detection applied to all images.")
