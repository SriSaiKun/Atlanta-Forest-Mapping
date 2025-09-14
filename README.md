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
    I started with a 1993 aerial photo of Cherokee County from the UGA Aerial Photography Collection. For the image preparation, I used OpenCV to convert the photo to grayscale, crop it to the center, and add a slight blur to clean it up.
    For all the classification steps, I used Scikit-learn to build the models. I began with two simple methods—a brightness cutoff (Thresholding) and an automatic pixel sorter (K-Means Clustering)—before training a final Random Forest model on hand-picked examples of forest and non-forest pixels. areas looked like in the image.
    In the end, all three methods worked well and created a map where forests are shown in white and non-forests are shown in black, as required. The results from each were pretty similar since they all learned to separate the image's dark and light spots.
    For a full walkthrough of the code and to see the final maps, please check out the Jupyter Notebook file and the demo video.
