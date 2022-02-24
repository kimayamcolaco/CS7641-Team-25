<!DOCTYPE html>
<html>
  
<h1>
<a id="intro" class="anchor" href="#intro" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>NBA Predictor</h1>
  
<body>

<h3>
<a id="intro" class="anchor" href="#intro" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Introduction & Background</h3>
<p>For our project, we aim to predict which teams will make the NBA playoffs and which teams are likely to win the championship based on mid-season performances as well as advanced statistical models. The NBA consists of 30 teams who are split into 2 conferences where 8 out of 15 teams in each conference advance to the playoffs. Our proposed model will help predict the final NBA standings for the regular season and help make predictions regarding the playoffs. The dataset we will primarily use is <a href="https://www.nba.com/stats/teams/boxscores/"> NBA Box Score </a> which contains box score stats for every game so far this NBA season as well as stats for previous seasons. We can filter by metrics in order to predict the winners.
</p>
<h3>
<a id="problem_definition" class="anchor" href="#problem_definition" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Problem Definition</h3>
<p>By creating this model, we are providing teams with predictions regarding the trajectory of how their team has played so far, and whether that team can make the postseason and help predict how the playoff bracket will unfold by running simulations of the playoff matchups. These models can also provide sports bettors and fans with important information to guide their wagers or pick teams to support. </p>
<h3>
<a id="methods" class="anchor" href="#methods" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Methods</h3>
<p>If you prefer to not use the automatic generator, push a branch named <code>gh-pages</code> to your repository to create a page manually. In addition to supporting regular HTML content, GitHub Pages support Jekyll, a simple, blog aware static site generator. Jekyll makes it easy to create site-wide headers and footers without having to copy them across every page. It also offers intelligent blog support and other advanced templating features.</p>
<h3>
<a id="results" class="anchor" href="#results" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>Potential Results and Discussion</h3>
<p>For this project, our goal is to build a machine learning model that takes in various NBA team stats and information and uses this data to predict the results of playoffs for the NBA. We may also consider data from previous playoffs and how that can be used to infer the outcomes of this playoff season. Our model should be able to compare 2 teams playing against each other and predict who will win that game, and be able to compare multiple teams and predict the overall standings of all teams for playoffs. This is essentially the NBA playoffs bracket predicted by our model. Alternatively, we could use ranges instead of definite placings to allow for a little more flexibility. (Predicting “Top 2”, “Bottom 2” rather than predicting an exact placing between 1 - 2.) This way, we could have a better starting point for our results, and can fine-tune our parameters based on what we believe we need. Our expected accuracy is approximately 70% for exact placings, and approximately 90% for ranges.
</p>
<h3>
<a id="refs" class="anchor" href="#refs" aria-hidden="true"><span aria-hidden="true" class="octicon octicon-link"></span></a>References</h3>
<p>Having trouble with Pages? Check out our <a href="https://help.github.com/pages">documentation</a> or <a href="https://support.github.com/contact">contact support</a> and we’ll help you sort it out.</p>
      </section>
    </div>

    <!-- FOOTER  -->
    <div id="footer_wrap" class="outer">
      <footer class="inner">
        <p class="copyright">NBA Predictor maintained by <a href="https://github.gatech.edu/CS7641-Group-25">CS7641-Group-25</a></p>
        <p>Published with <a href="https://pages.github.com">GitHub Pages</a></p>
      </footer>
    </div>

    

  </body>
</html>

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/kimayamcolaco/CS7641-Team-25/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
