# Streamlit on Docker
Project docs: https://streamlit.io/docs/

<p align="center">
  <img src="img/streamlit.png" width="750" title="Example Streamlit App">
</p>

This Docker image is available on Docker Hub: 
## Pull
`docker pull tomerlevi/streamlit-docker`

## Running Streamlit docker built-in examples
You can learn how to use streamlit by exploring 3 scripts (packed inside the docker image):

`docker run -it -p 8501:8501 tomerlevi/streamlit-docker /examples/intro.py` <br/>
`docker run -it -p 8501:8501 tomerlevi/streamlit-docker /examples/plot_example.py` <br/>
`docker run -it -p 8501:8501 tomerlevi/streamlit-docker /examples/uber_nyc_data_explorer.py` <br/>


## Running your own streamlit script
`docker run -it -p 8501:8501 -v <local-scripts-folder>:/app tomerlevi/streamlit <relative-path-to-a-script>`

Example:
`docker run -it -p 8501:8501 -v ~/workspace/streamlit-scripts:/app tomerlevi/streamlit src/main.py`

Once streamlit is running, open your browser and navigate to: http://localhost:8501

*NOTE*: you can open the script you passed (`<relative-path-to-a-script>`) in your favorite text editor and edit it, streamlit will pickup all changes once you refresh your browser tab.


## Build 
Clone the repo:
`git clone git@github.com:MrTomerLevi/streamlit-docker.git`

Change dir into the project:
`cd streamlit-docker`

*Optional:*  You can add your required PyPi packages to the `requirements.txt`

Run docker build:
`docker build -t tomerlevi/streamlit-docker .`



