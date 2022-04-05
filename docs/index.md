<html>
  
<h1>
<a id="intro" class="anchor" href="#intro" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>NBA Predictor</h1>
  
<body>

<h2>
<a id="intro" class="anchor" href="#intro" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Introduction & Background</h2>
<p>For our project, we aim to predict which teams will make the NBA playoffs and are likely to win the championship based on mid-season performances as well as advanced statistical models. The NBA consists of 30 teams split into 2 conferences where 8 out of 15 teams in each conference advance to the playoffs. Our proposed model will help predict the final NBA standings for the regular season and make predictions regarding the playoffs. The dataset we will primarily use is <a href="https://www.nba.com/stats/teams/boxscores/"> NBA Box Scores </a>  which contains box score stats for every game so far this season as well as for previous seasons.
</p>
  
<p align="center">
    <img height="300px" src="assets/logo.jpg">
    <img height="300px" src="assets/teams.jpg">
</p>
<h2>
<a id="problem_definition" class="anchor" href="#problem_definition" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Problem Definition</h2>
<p>By creating this model, we provide predictions regarding the trajectory of how teams have played so far, and whether they can make the postseason and help predict how the playoff bracket will unfold by running simulations on playoff matchups. The model can also provide bettors and fans with important information to guide wagers or pick teams to support.  </p>

<p align="center">
    <img height="300px" src="assets/structure.jpg">
</p>
  
<h2>
<a id="data_collection" class="anchor" href="#data_collection" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Data Collection</h2>
<p>For the unsupervised learning part of the project, we sourced the data from CSV files from ProBasketballReference and used a python script to clean and parse this data. We then used Pandas to read the CSV file and picked relevant features. </p>

<p>Our test data was sourced from the 2020-2021 NBA season so we could test how accurate our models would be at predicting the NBA playoff teams, by comparing our results to actual playoff results from this season. The complete dataset is shown in the table below. To run our model, we focussed on the team that actually made the playoffs (represented by an *) and used this to clean our dataset to get only the relevant statistics. </p>
  
<p align="center">
    <img height="300px" src="assets/stats.jpg">
</p>

<p>We then selected key features that would be most relevant to assessing a team’s performance and plotted these values for each of the teams in our focussed dataset. The bar graphs below show the plot for wins (W), total points (PTS), 3 points (3P) and assists (AST) as well as our analysis of the same. </p>

<h3><a id="wins" class="anchor" href="#wins" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Wins (W)</h3>
<p align="center">
    <img height="300px" src="assets/wins_graph.jpg">
</p>
  
<p> From the graph above, based on the number of games won, we can infer that the Lakers, Hawks, Grizzilies, Jazz, Blazers, Knicks, 76ers, Nuggets, Nets, Bucks, Clippers, and Suns could make the playoffs. These teams seem to win more games than the other teams. </p>

<h3><a id="pts" class="anchor" href="#pts" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Total Points (PTS)</h3>
<p align="center">
    <img height="300px" src="assets/pts_graph.jpg">
</p>
  
<p> The variance in the graph above is low, but the Jazz, Blazers, Wizards, Pacers, 76ers, Nuggets, Nets, Bucks, Clippers, Pelicans, and Suns seem to score more points than other teams, indicating they are playoff caliber teams. </p>

<h3><a id="3ps" class="anchor" href="#3ps" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>3 Pointers (3P)</h3>
<p align="center">
    <img height="300px" src="assets/3p_graph.jpg">
</p>
  
<p> Based on the chart above, we can infer that the Jazz, Blazers, Raptors, Nuggets, Nets, Mavericks, Bucks, Celtics, Clippers, Warriors, and Suns score more 3-pointers than other teams. Usually, playoff-caliber teams have better 3-pointers made than the non-playoff teams. </p>

<h3><a id="ast" class="anchor" href="#ast" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Assists (AST)</h3>
<p align="center">
    <img height="300px" src="assets/ast_graph.jpg">
</p>
  
<p> Based on the chart above, we can infer that the Warriors, Pacers, Suns, Rockets, Bulls, Grizzlies, 76ers, and Nets have higher assist percentages than other teams. Usually, playoff-caliber teams do better in this statistic. </p>
  
<h2>
<a id="methods" class="anchor" href="#methods" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Methods</h2>

 <h3><a id="unsupervised" class="anchor" href="#unsupervised" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Unsupervised Learning</h3>
  <p>Our first method was to perform Principal Component Analysis (PCA) to reduce the dimensions of our data and pick out the optimal features that maximize the variance of our data. After running PCA on the dataset, we plot a heatmap or correlation matrix (see result analysis section) to get a vision of the most impactful features and the less impactful features from our dataset. </p>

<p>After running PCA, we performed Gaussian Mixture Model (GMM) on the dataset and separated the data into 2 clusters: playoff teams and non-playoff teams. The idea with the Gaussian Mixture Model is to create 2 clusters and decide the playoff and the non-playoff clusters based on the means of the data received from our feature selection using PCA. </p> 
<p>However, there can only be 16 playoff teams, no more, no less. In the case that the playoff cluster has more than 16 teams, we can use the responsibility measures (assignments) of each data point and move the data points (teams) that have the least responsibility assignment of all the points in the cluster, out of the cluster until there are only 16 teams remaining. We can do this because the points belong the least to this cluster than other points in the playoff cluster.</p>
<p>In the case that the playoff cluster has less than 16 teams, we can move the least assigned data points (teams) in the non-playoff teams cluster to the playoff cluster until there are 16 teams.</p>
<p> The next section contains further details on our results and analysis of this model. </p>
  
<h2>
<a id="results" class="anchor" href="#results" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Potential Results and Discussion</h2>
<h3><a id="unsupervised" class="anchor" href="#unsupervised" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Unsupervised Learning</h3>
<p>After the data collection portion which consisted of gathering the data, filtered based on teams that made the playoffs as our test data and plotting the bar graphs for teams based on important features, we could move on to our first model- Principal Component Analysis (PCA). </p>
 <p> After running PCA on the data, we concluded that 3 principal components contribute to 93% of the variance of our dataset signaling that those components are well descriptive to signify a teams playoff status. </p>
<p align="center">
    <img height="300px" src="assets/pca_plot.jpg">
</p>
 <p> We then plotted a heatmap to signify which components are most indicative in signifying a playoff team.  </p>
<p align="center">
    <img height="300px" src="assets/heatmap.jpg"></p>
 <p> The following data below is the principal_components of our dataset and the relevant features associated with each component.   </p>
<p align="center">
    <img height="300px" src="assets/component_data.jpg">
</p>
 <p> There are many ways to select features from the principal components. In this case, the features were selected from each of the three principal components where the features contributed at least 10% or more to each component. In other words, feature 22 contributed 68% to component 1 and we keep selecting features starting 22 to 24 since 1 only contributes 6% to the first component. Once the condition is violated, we move on to the second component and repeat. We do this for all components and the selected features are shown below.  </p>

<h2>
<a id="refs" class="anchor" href="#refs" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>References</h2>
  <p>1. Mikołajec, Kazimierz et al. “Game Indicators Determining Sports Performance in the NBA.” Journal of human kinetics vol. 37 145-51. 5 Jul. 2013(<a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3796832/">link</a>)
  </p>
  <p> 2. Thabtah, F., Zhang, L. & Abdelhamid, N. NBA Game Result Prediction Using Feature Analysis and Machine Learning. Ann. Data. Sci. 6, 103–116 (2019) (<a href="https://doi.org/10.1007/s40745-018-00189-x">link</a>)
  </p>
  <p> 3. Jingru Wang and Qishi Fan 2021 J. Phys.: Conf. Ser. 1802 032036 (<a href="https://iopscience.iop.org/article/10.1088/1742-6596/1802/3/032036">link</a>)
  </p>

<h3>
<a id="timeline" class="anchor" href="#timeline" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Proposed Timeline</h3>
  <p>View our proposed project timeline <a href="https://gtvault-my.sharepoint.com/:x:/g/personal/kcolaco3_gatech_edu/Ed745itnB4BNrrMAhuP-s-cBbbwPmu2WzhvwIJb2FZzEMQ?e=TfflJm/"> here </a></p>
  </body>
</html>
