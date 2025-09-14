Atlanta Forest Mapping Project
How to Run This Project
Here’s how you can get the project up and running:
1. Get the code ready:
    -- Create a virtual environment in the project folder:
           python -m venv venv
           source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

2. Install the tools:
    -- Install the necessary Python libraries:
           pip install opencv-python scikit-learn matplotlib numpy

3. Start Jupyter:
    -- Launch the Jupyter Notebook server from your terminal:
            jupyter notebook
4. Run the project:
    -- Open the forest_mapping_project.ipynb file and click Kernel > Restart & Run All.

My Process and Results:
    I began with a 1993 aerial photo of Cherokee County from the UGA Aerial Photography Collection. Using OpenCV, I prepared the image by converting it to grayscale, cropping it to the center, and applying a slight blur to clean it up.
    For the classification steps, I used Scikit-learn to build the models. I started with two simple methods, a brightness cutoff (Thresholding) and an automatic pixel sorter (K-Means Clustering), before training a final Random Forest model on hand-picked examples of what forest and non-forest pixels looked like.
    Ultimately, all three methods successfully created a map where forests are shown in white and non-forests are black, as required. The results were quite similar because each model learned to separate the image's dark and light areas.  
    For a complete walkthrough of the code and a view of the final maps, please see the Jupyter Notebook file and the demo video.
