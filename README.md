# Avatar Generation from Real Images using Deep Learning

Objective : 

The objective of this project is to develop a deep learning-based system that can generate personalized avatar images from real photographs of individuals. The generated avatars should capture the essence of the person while applying a unique and artistic style.



CODEBASE OVERVIEW :

### Dependencies

- `streamlit`: A Python library for creating web applications with interactive elements.
- `numpy`: Fundamental package for scientific computing with Python.
- `PIL (Pillow)`: Python Imaging Library, used for opening, manipulating, and saving images.
- `api_tokens`: An external module (not included) that presumably contains API tokens for authentication. This is used to fecth the pretrained model from hugging face
- `torch`: PyTorch, a deep learning framework for building and training neural networks.
- `diffusers`: A package containing a model for image-to-image translation using diffusion models.

### AvatarGenerator Class

The `AvatarGenerator` class is the core component of the project. It is responsible for generating avatars from text prompts and real images. Here's a breakdown of its key methods and functionality:

- `__init__(self)`: The constructor initializes the avatar generation pipeline. It loads a pre-trained model called "nitrosocke/Ghibli-Diffusion" and sets various configuration options.

- `generate_avatar(self, text_prompt, image)`: This method takes a text prompt and an uploaded real image as input. It resizes the image, sets a random seed, and uses the diffusion model to generate an artistic avatar based on the text prompt and the real image. The generated avatar is saved as an image file and returned.

### Streamlit Web Application

The Streamlit web application serves as the user interface for this project. It allows users to interact with the `AvatarGenerator` class and generate avatars. Here's a summary of the app's functionality:

- Users can upload a real image using the "Upload an image" feature.
- Users can enter a text prompt that describes the desired style or characteristics of the avatar.
- Clicking the "Generate Avatar" button triggers the avatar generation process.
- The original uploaded image is displayed, followed by the generated avatar image.

## Setup Instructions

To set up and run this project locally, follow these steps:

1. Clone the GitHub repository:

   ```
   git clone <repository_url>
   cd <repository_directory>
   ```

2. Install the required dependencies. You can use `pip` to install them:

   ```
   pip install -r requirements.txt
   ```

3. Replace the access token in `api_tokens.py` file and provide the necessary API tokens for authentication .

4. Run the Streamlit application:

   ```
   streamlit run app.py
   ```

5. Access the application in your web browser at the provided URL (usually http://localhost:8501).

## Usage Guidelines

1. Upon accessing the web application, you will see the title "🧑🏽‍🎨 Avatar Generator."

2. Upload a real image by clicking the "Upload an image" button.

3. Enter a text prompt in the "Enter a text prompt" field. This prompt should describe the style or characteristics you want for the generated avatar.

4. Click the "Generate Avatar" button to initiate the avatar generation process.

5. The original uploaded image will be displayed, followed by the generated avatar image.

6. You can save the generated avatar image by right-clicking on it and selecting "Save image as."

## Project Repository

The codebase for this project, including the source code and this README file, can be found in the GitHub repository: [repository_url](link_to_repository).

Please use the access token of your hugging face account

For any questions or issues, feel free to contact the project maintainers or open an issue on the GitHub repository.

**Note:** This README assumes that you have the required dependencies and API tokens set up as specified in the project's setup instructions.