<h1>Autis-Aid </h1>
A Deep Learning based Alerting System for Autistic Children

<H2>Inspiration</H2>
Autistic children generally show erratic behavior and their responses are unpredictable and spontaneous, therfore such children must be taught under constant monitoring of care takers, specially trained teachers and parents. Hence the learning process for such students becomes cumbersome and sophisticated as the need of a mediator (teacher/care taker/parent) becomes a variable in the learning process. Autis-Aid aims to automate the process of real time monitoring of autistic and special aid children during their learning process.

<H2>What it does</H2>
With Autis-Aid we provide a system free of mediator where the response of these special students are continually monitored and captured during their learning process. Any kind of distressed behavior and response to any kind of educational material is notified to the care taker/teacher/parent in an automated manner. The system also provides platform for visualization of the students behavior.

<H2>What have we used</H2>
<ul>
  <li> Our solution use various CNN models for a multi-class classification inorder to predict distressed expressions like: anger, fear and sadness. The CNN model used for prediction was trained using transfer learning where we have used various pre-trained models like: VGG16, Xception etc. </li>
  
  <li> For the real time monitoring we have deployed this model in a flask app combined with a UI and functionalities to send notifications and monitor the behavior of the student during the whole learning process using interactive visualizations. </li>
</ul>

<H2>How we built it</H2>
<ul>
  <li> The web interface provides an option for the user to trigger the web cam in their device. Once the web cam is triggered the user can activate the functionalities of the app. </li>
  <li> From the web cam we take 1 frame in 100 frames for prediction. The prediction of the emotion is done using the saved model in h5 format. </li>
  <li> When a distressed emotion is detected the notification functionality is triggered which sends a notification to the care taker. </li>
  <li> The prediction results are also continuously stored in a database which is used for the interactive visualizations in the web interface. </li>
</ul>

<H2>Challenges we ran into</H2>
<ul>
  <li> The dataset used for the training was imbalanced so proper balancing and pre Preprocessing of the dataset had to be done before training the model.
A considerable amount of time was spent on finding the right training hyperparameters. </li>
  <li> In order to remove overfitting, image augmentation techniques were applied to the dataset. </li>
  <li> Getting the Web-part to work synchronously with the ML part was a bit challenging. </li>
</ul>

<H2>Accomplishments that we're proud of</H2>
<ul>
  <li> We were able to run the flask app in real-time by taking real-time video input from the camera feed. </li>
  <li> We were able to integrate the web part with the classifier model pretty well. </li>
</ul>

<H2>What we learned</H2>
<ul>
  <li> Learned the need for proper time management when working with neural networks. </li>
  <li> Real-time implementations are much harder when compared to textbook-level implementations. </li>
  <li> We learn how to code efficiently when provided with a stressful time constraint. </li>
</ul>

