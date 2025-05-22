# Ray Serve Translation Demo

This project demonstrates a Ray Serve application that provides translation services using the Hugging Face transformers library.

## Setup Instructions

1. Create a new conda environment:

```bash
conda create -n ray_examples_env python=3.10
conda activate ray_examples_env
```

2. Install the required packages:

```bash
pip install -r requirements.txt
```

## Running the Application

1. Start the Ray Serve application in one terminal:

```bash
serve run serve_quickstart:translator_app
```

2. Test the translation service using seperate terminal:

```bash
# Using Python client
python TranslationApp/model_client.py
```

## Project Structure

- `TranslationApp/`: Contains the translation service implementation
- `ComposiningApp/`: Contains the composed application code
- `requirements.txt`: Lists all required Python packages
- `.gitignore`: Specifies files to be ignored by git

## Dependencies

The main dependencies are:

- Ray Serve for serving the translation model
- Transformers for the translation model
- FastAPI for the web server
- Various utility packages for HTTP handling and async operations
