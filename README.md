# Ray Serve Examples

This repository contains multiple examples demonstrating different aspects of Ray Serve, including a translation service and a composed application example.

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

## Translation Service Example

The translation service example demonstrates how to serve a Hugging Face transformer model using Ray Serve.

### Running the Translation Service

1. Start the Ray Serve application in one terminal:

```bash
cd <PATH>/RayServeExamples/RayServeDemo/TranslationApp
serve run serve_quickstart:translator_app
```

2. Test the translation service using a separate terminal:

```bash
# Using Python client
python TranslationApp/model_client.py
```

## Compositions App Example

The Composing App example demonstrates how to create complex applications by combining multiple Ray Serve deployments. This example showcases:

1. **Multiple Deployments**: How to create and chain multiple deployments together
2. **Deployment Composition**: Techniques for combining different services into a single application
3. **Routing and Load Balancing**: How Ray Serve handles requests between different deployments
4. **State Management**: Best practices for managing state across deployments

### Running the Composing App

1. Start the Ray Serve application:

```bash
cd <PATH>/RayServeExamples/RayServeDemo/CompositionsApp
serve run serve_quickstart_composed:app
```

2. Test the composed application using the provided client:

```bash
python ComposiningApp/composed_client.py
```

## Troubleshooting
- Incase ray[serve] is not install execute `pip install ray[serve]`
- Incase ray is not installed execute `pip install ray`
- Always run the client call from the different terminal 
- If you are running the ray on the local system in order to execute the command on ray cluster use `ray start --head` and it will start the local ray cluster
- In order to stop the ray cluster use `ray stop`


## Project Structure

- `TranslationApp/`: Contains the translation service implementation
- `ComposiningApp/`: Contains the composed application code with multiple deployments
- `requirements.txt`: Lists all required Python packages
- `.gitignore`: Specifies files to be ignored by git

## Dependencies

The main dependencies are:

- Ray Serve for serving the models and managing deployments
- Transformers for the translation model
- FastAPI for the web server
- Various utility packages for HTTP handling and async operations

## Best Practices

- Use clear naming conventions for deployments
- Implement proper error handling
- Use async/await for better performance
- Consider deployment scaling based on load
- Use proper logging for debugging

## Contributing

Feel free to contribute additional examples or improvements to the existing examples. Please follow the existing code style and include proper documentation for any new features.
