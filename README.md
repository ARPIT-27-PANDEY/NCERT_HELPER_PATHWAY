# Wellness App for Personalized Suggestions 🌿
This application is built using Pathway's API with Streamlit as the user interface. The goal of this app is to provide personalized wellness suggestions based on user input, addressing a variety of mental health and well-being concerns.

## Video Demo of the APP 🎥
<video src="(https://www.youtube.com/watch?v=Njbt-B1CSnE)" controls="controls"> </video>
LINK for the Video

## Description 📝
The Wellness App leverages Pathway’s powerful API to provide personalized wellness suggestions based on users' unique situations and needs. It combines advanced algorithms with real-time feedback to offer a tailored experience, supporting mental and physical well-being.

The Pathway API powers the app by enabling smart, personalized suggestions for a variety of wellness topics like stress, anxiety, and overall self-care. The real-time data pipeline integration allows the app to continuously learn from user inputs and provide accurate and actionable advice.

Built with Streamlit, this app offers a seamless user experience, allowing users to easily navigate the interface, input their current wellness concerns, and receive helpful suggestions instantly.

## Features 🎁
* Personalized Wellness Suggestions: Tailored to each user's specific mental health or physical well-being needs.
* User-Friendly Interface: Streamlit-powered for easy navigation and interaction.
* Pathway API Integration: Provides real-time, data-driven suggestions without requiring a separate database.
* Real-Time Feedback: The app learns and adapts to user inputs for improved accuracy.
* Cross-Platform Deployment: Easily deploy on any platform using Docker.
* Summary of Available Endpoints 📊
* The application provides a webserver with the following endpoints:

Default URL for backend: `http://0.0.0.0:8000/`
## Wellness Query and Suggestion Capabilities
/v1/get_suggestion: Retrieve personalized wellness suggestions based on user input.

/v1/get_feedback: Input real-time feedback to improve suggestions.

## Prerequisites 📋
Before running the app, make sure you have the following installed:

* Python 3.x
* Git
* Docker
## Installation 💻

`git clone https://github.com/your-repo-link/wellness-app.git`

Change into the project directory:

`cd wellness-app`

Add your Pathway API key to the .env file:

PATHWAY_API_KEY=<YOUR_API_KEY>

Build and run the Docker Image:

`docker-compose up`
Note: Building the image may take 15-20 minutes. ⏳

Access the app in your browser at http://localhost:8501.


To stop the program:

`docker-compose down`
## Future Improvements 🚀
* Add an in-app wellness assessment tool for a more detailed analysis.
* Support for audio or visual inputs to enhance interactivity.
* Advanced analytics to track wellness progress over time.
Made with 💛 by Vishesh Bhardwaj
