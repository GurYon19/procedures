# saving and working requirements for projects

each project should have env.yml to install the packages faster <br />
# create env yml:<br />
conda env export --my_env - --file environment.yml <br />
create conda env using yml: conda env create --file environment.yml ot conda env create -f .\environment.yml <br />


 for more info: <br />
 https://carpentries-incubator.github.io/introduction-to-conda-for-data-scientists/04-sharing-environments/index.html
https://docs.conda.io/projects/conda/en/latest/_downloads/843d9e0198f2a193a3484886fa28163c/conda-cheatsheet.pdf


##older stuff: 
using conda:<br />
save requirements.txt: conda list -e > conda_requirements.txt<br />
create conda env: conda create --name --file conda_requirements.txt<br />

using pip:<br />
save requirements: pip list --format=freeze > pip_requirements.txt<br />
install rquirements : pip install -r pip_requirements.txt<br />


## To install from  conda_requirements to conda env 
create conda env using : conda create --name <env name> <br />
install pip for conda using : conda install pip <br />
Windows <br />

FOR /F "delims=~" %f in (conda_requirements.txt) DO conda install --yes "%f" || conda install -c conda_forge --yes "%f"<br />

Bash<br />

while read requirement; do conda install --yes $requirement; done < conda_requirements.txt<br /> <br />

