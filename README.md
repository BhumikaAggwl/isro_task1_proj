# isro_task1_proj

Here’s a README.md file for your project:

#Automated Satellite Data Pipeline for Celestial Object Detection

This project processes astronomical imagery in FITS format, detects celestial objects, extracts meaningful features, and classifies the objects into categories such as stars, galaxies, and planets.

#Features
	•	Ingests and processes FITS files.
	•	Detects celestial objects based on image thresholding and clustering.
	•	Extracts object properties like centroid coordinates, size, and luminosity.
	•	Classifies objects into categories (e.g., stars, galaxies, planets).
	•	Outputs results to a CSV file for further analysis.
	•	Provides visualization of detected and classified objects.

#Installation

#Requirements
	1.	Python 3.8 or higher
	2.	Libraries:
	•	numpy
	•	pandas
	•	astropy
	•	scikit-image
	•	matplotlib

#Setup

Install the required Python packages:
```
pip install numpy pandas astropy scikit-image matplotlib
```
Clone the repository or copy the scripts to your local system.

#Usage

1. Process FITS File

Run the Python script to process a FITS file and save the results as a CSV file:
```
python process_fits.py <input_fits> <output_csv>
```
Example:
```
python process_fits.py hlsp_appp_hst_wfpc2_sfd-pu4k2ho01_f606w_v2_sci.fits classified_celestial_objects.csv
```
##2. Outputs
	•	A CSV file containing:
	•	Object_ID: Unique ID for each detected object.
	•	X: Centroid x-coordinate.
	•	Y: Centroid y-coordinate.
	•	Size: Object size (area in pixels).
	•	Luminosity: Total intensity of the object.
	•	Classification: The type of celestial object (Star, Galaxy, Planet, Unknown).
	•	A visualization showing the detected and classified objects.

#Pipeline Steps
	1.	Data Ingestion:
	•	Reads the FITS file using the astropy library.
	•	Extracts the image data for processing.
	2.	Image Processing:
	•	Applies thresholding to separate celestial objects from the background.
	•	Labels connected regions to identify individual objects.
	3.	Feature Extraction:
	•	Calculates:
	•	Centroid (x, y coordinates)
	•	Size (area in pixels)
	•	Luminosity (sum of pixel intensities)
	4.	Object Classification:
	•	Classifies objects based on size and luminosity:
	•	Star: Small size, high luminosity.
	•	Galaxy: Large size, medium/high luminosity.
	•	Planet: Small size, low luminosity.
	•	Unknown: Does not fit predefined thresholds.
	5.	Data Output:
	•	Saves results in a CSV file.
	•	Visualizes the results with overlaid classifications.

#Examples

Input FITS File

The pipeline processes raw FITS images like this:

###Output Visualization

The processed image displays detected and classified objects:

###Sample CSV Output

Object_ID	X	Y	Size	Luminosity	Classification
1	512.67	256.34	48	6000	Star
2	128.45	634.12	300	4000	Galaxy
3	400.12	300.50	45	2000	Planet

#Customization
	•	Adjust Classification Criteria: Modify thresholds in the classify_objects() function to better fit your data.
	•	Add More Features: Integrate machine learning models for more accurate object classification.

#License

This project is open-source and available under the MIT License.

###Contributions

Contributions are welcome! Please feel free to submit a pull request or open an issue for any enhancements or bug fixes.

###Acknowledgments
	•	FITS data format from NASA and the Hubble Space Telescope.
	•	Libraries:
	•	AstroPy
	•	Scikit-Image
	•	Matplotlib

Contact

For any queries, please contact: your_email@example.com

This README provides a comprehensive overview of the project, setup instructions, and usage guidelines. Let me know if you’d like further refinements!
