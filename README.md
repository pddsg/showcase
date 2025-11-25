### Showcase Repository

This repository represents a small sample of hand-picked scripts and projects I've developed in a manufacturing and QC environment. The original library is much larger but kept private for IP reasons. You'll find a mix of JMP scripting language code with traces of Python and SQL added to the toolkit. These scripts are used for data analysis and dashboarding of QC as well as manufacturing sensor data.

There's a Jupyter notebook that goes through some Python examples. The JMP scripts often have SQL, and in one case Python, tucked inside. The [Bulk Oil Stability Calculator](https://github.com/pddsg/showcase/blob/main/Bulk%20oil%20stability%20calculator.jrn) and [AKBM Google Cloud View Opener](https://github.com/pddsg/showcase/blob/main/AKBM%20Google%20Cloud%20view%20opener.jmpaddin) are best experienced in connection with a JMP license. Several scripts in this repository are actively used in [Aker BioMarine](https://www.akerbiomarine.com/) at the time of writing, but the stability calculator is possibly the most ambitious and impactful piece of software here.

Feel welcome to browse around. This is a fair assessment of how I’ve been refining my data analysis and modelling skills to shape myself from industrial analytical chemist to citizen data scientist.

There are always too many low-hanging fruits. And yes, I use AI for Python and SQL, because AI is a good teacher. For JSL I rely heavily on the [JMP User Community](https://community.jmp.com/) - here's [my user profile](https://community.jmp.com/t5/user/viewprofilepage/user-id/15435).

## Projects
### JSL
- **[akbm_bq_view_opener.jmpaddin](https://github.com/pddsg/showcase/blob/main/jsl_addin/akbm_bq_view_opener.jmpaddin)** – simplifying access to business critical views in Google BigQuery.
- **[algae_oil_trending.jsl](https://github.com/pddsg/showcase/blob/main/jsl_scripts/algae_oil_trending.jsl)** – trending and statistical analysis of algae oil in-process and QC data.
- **[bulk oil stability calculator.jrn](https://github.com/pddsg/showcase/blob/main/jsl_scripts/bulk%20oil%20stability%20calculator.jrn)** – a tool for assessing shelf-life of products of varying quality, stored under varying conditions.
- **[capsule_trending.jsl](https://github.com/pddsg/showcase/blob/main/jsl_scripts/capsule_trending.jsl)** - trending and statistical analysis of capsule QC data.
- **[dryer_pressure_readings.jsl](https://github.com/pddsg/showcase/blob/main/jsl_scripts/dryer_pressure_readings.jsl)** - trending and inspection of system critical pressure readings and their fluctuations over time.
- **[extraction_tank_stirring.jsl](https://github.com/pddsg/showcase/blob/main/jsl_scripts/extraction_tank_stirring.jsl)** - trending and inspection of agitation used in process tanks.
- **[smb_cycle_time_hist.jsl](https://github.com/pddsg/showcase/blob/main/jsl_scripts/smb_cycle_time_hist.jsl)** - plotting of changes in system settings, previously frequently undocumented and not analyzed as a function of time.
- **[tag_metadata_py.jsl](https://github.com/pddsg/showcase/blob/main/jsl_scripts/tag_metadata_py.jsl)** - retrieving flattened table of sensor metadata (i.e., unnesting nested tables).
### Python
- **[area_under_curve.ipynb](https://github.com/pddsg/showcase/blob/main/jupyter_notebooks/area_under_curve.ipynb)** - integration of transient signals in connection with an investigation of production anomalies.
- **[ethanol_peaks_auc.ipynb](https://github.com/pddsg/showcase/blob/main/jupyter_notebooks/ethanol_peaks_auc.ipynb)** - quantifying process inputs from flow meter readings.
- **[extraction_yield_wip.ipynb](https://github.com/pddsg/showcase/blob/main/jupyter_notebooks/extraction_yield_wip.ipynb)** - process yield calculations. Work in progress.
- **[flattening_nested_dictionaries.ipynb](https://github.com/pddsg/showcase/blob/main/jupyter_notebooks/flattening_nested_dictionaries.ipynb)** - used for developing Python eventually used in <code>tag_metadata (py).jsl</code>.

## Example screenshot from [<code>capsule_trending.jsl</code>]()
<img width="771" height="392" alt="image" src="https://github.com/user-attachments/assets/4a0bacfa-dc05-4a18-b9d7-d07b6b303cf5" />
<br>What you see here are multiple graphs showing the overfill of individual components relative to their specification limits. Each line corresponds to one product batch, and the products are capsules from various contract manufacturers. 
<br>The individual components in these capsule batches are shown along the x axis, and the overfills for each component are shown as relative percentages along the y axis. The results are sorted from left to right in order of increasing, average relative overfill.
<br>Data points below the horizontal zero line are obvious problems, because these batches contain too little of the corresponding component shown on x. However, areas of excessive overfill to the right are also immediately identifiable and could aid refinement of product specifications or reduction of excessive overfills for some products. 
<br>The underlying script also allows:
- Trending over time
- Comparison between manufacturers
- Drilling down to individual batches
- Ad-hoc loading of *all* QC data of any individual batch directly from the data warehouse via a built-in point & click trigger.


