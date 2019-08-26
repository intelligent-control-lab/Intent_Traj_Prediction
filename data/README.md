## Dataset for human-motion trajectory and intention prediction
We designed a simple card-making task with a goal to make a Baymax birthday card. 
<img src="https://github.com/intelligent-control-lab/Intent_Traj_Prediction/raw/master/demo/setup_card.png" width="600" >  
The actions and their relationships are illustrated in following figure.   
<img src="https://github.com/intelligent-control-lab/Intent_Traj_Prediction/raw/master/demo/Action_Relations.jpg" width="400" >  
They are: (1) Take the card; (2) Take the red sharpie; (3) Draw lines; (4) Take the card with Baymax printed on it (Take Baymax); (5) Take the scissors; (6) Cut out Baymax; (7) Take the glue stick; (8) Put glue on the back of the cut-out Baymax (Put glue on Baymax); (9) Stick Baymax on the card; (10) Take the black sharpie; (11) Write `Happy Birthday!` on the card (Write Words); (12) Bring the item back.  
In this task, one can separate the 12 actions into three groups with regard to their higher-level purpose, namely `Form the Base` (draw lines on the card using the red sharpie), `Stick Baymax On` (put glue on the back of Baymax after cutting it out, stick it onto the card with red lines), and `Write "Happy Birthday!}"` (with the pen). Within each group, every `reach and take` action must occur first, and the remainder of the actions must occur sequentially. 
We have grouped together the retraction motion from all the take actions (actions 1, 2, 4, 5, 7, and 10) into action 12 for convenience in intention labeling.  
In this task, all items are placed in fixed positions so that human intentions can be inferred purely from human trajectories.

In the collection of the dataset, a Kinect V2 camera was used to capture the trajectories of human subjects' right arms at an approximate frequency of 20Hz. The human subjects are asked to perform the 12 pre-defined actions. 50 trajectories for each action were obtained from actor A (80\% offline training, 20\% offline validation). Another actor B repeated each action 10 times (100\% testing). 
