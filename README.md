# Interactive Urban Floor Screen Installation: Dynamic Shape Adaptation to Human Interaction

Optional project of the [Streaming Data Analytics](http://emanueledellavalle.org/teaching/streaming-data-analytics-2023-24/) course provided by [Politecnico di Milano](https://www11.ceda.polimi.it/schedaincarico/schedaincarico/controller/scheda_pubblica/SchedaPublic.do?&evn_default=evento&c_classe=811164&polij_device_category=DESKTOP&__pj0=0&__pj1=d563c55e73c3035baf5b0bab2dda086b).

Student: Tommaso Bucaioni

This project explores the intersection of urban design, interactive technology, and computer vision by creating a large, interactive floor screen that responds dynamically to human movement. Utilizing overhead cameras, the installation detects when individuals step onto the screen, triggering a visual response that tracks their movement with geometric shapes.

**Components of the solution:**
- Human Detection Component: implementing, using transfer learning from YOLO or other pre-trained Neural Networks, an advanced computer vision solution to accurately detect and track individuals on the screen.
- Stream Processing Component: Utilizing a stream processor to manage the flow of data between the cameras and the screen, ensuring real-time responsiveness to human interaction.
- Shape Adaptation Component: Developing a Web Application that, based on the results of the Stream Processing Component dynamically draws and adjust shapes around detected individuals, with the geometry changing based on the proximity and movement of people.

**Detailed Description of the expected experience:**
- When the camera detects a person, Web App draws a square around the person. If the person moves on the screen the square follows her. 
- If two people walking on the screen get so close that their respective square touches, the Web App draws a pentagon around the two people.
- If they now walk together, the pentagon follows them. 
- If they get close enough to other people, the pentagon can become a polygon with more edges (3 + the number of people moving together). 
- If they separate, the pentagon splits into two squares. If a person steps off the screen, her square disappears.

The project will utilize AI frameworks such as Edge Impulse or Roboflow, python or javascript libraries, and a stream processor among those illustrated in the course. The project aims to orchestrate the interaction between the detection system and the screen's visual output.

**Evaluation Metrics:** \
The project will be assessed based on:
- Accuracy of human detection and tracking.
- Responsiveness and fluidity of shape adaptation and movement on the screen.
- Efficiency of the event processing system in handling real-time interactions.

**Benchmarks:** \
Testing will involve simulated and live interactions in varied scenarios:
- Single and Multiple Interactions: Observing the system's response to individual and group movements, including the dynamic transformation of shapes.
- Complex Movement Patterns: Evaluating how well the system adapts to complex human interactions, such as merging and splitting groups.

**Dataset:** \
A collection of images can be found [here](https://studio.edgeimpulse.com/public/357387/live).

The expected result is a dockerized application that demos the complete pipeline and analyzes the solution against the evaluation metrics. The project aims to conclude with a reflective discussion on the implications of integrating such interactive technologies in urban spaces, focusing on enhancing public engagement and the potential for future developments.


## Note for Students

* Clone the created repository offline;
* Add your name and surname into the Readme file;
* Make any changes to your repository, according to the specific assignment;
* Add a `requirement.txt` file for code reproducibility and instructions on how to replicate the results;
* Commit your changes to your local repository;
* Push your changes to your online repository.
