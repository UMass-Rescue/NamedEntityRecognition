# Named-entity recognition & detecting names of people

This model is designed accoding to the template in [UniversalModelTemaplate](https://github.com/UMass-Rescue/UniversalModelTemplate). The model passes all the test cases in this application, and should work in the context of the server.

In the model directory, the code in `model.py` detects named-entities, i.e. names of people, locations and organizations using tranformers in [Hugging Face](https://huggingface.co/transformers/usage.html).  In the `perdiction()` function in `model/model.py` file, set `only_person` to `True` to detect only names of people.

`config.py` has some metadata about the ML model, e.g. input type, model name, and tags. 
The requirements are added to `requirements.py` file in the model directory. 


## Debugging your Model

In the root directory of the project, run the command 
`docker-compose build debug` and then `docker-compose up debug`. Open a web browser and navigate to
[http://localhost:4650]('http://localhost:4650').

As you make changes to your model the results will appear on the web page showing the initialization
status and a prediction result on a test image.


## Testing your Model

In the root directory of the project, run the command `docker-compose build test` and then
`docker-compose up test`. You will see the results of the test cases in your terminal. If all
test cases pass, then your model will work in the server environment.
