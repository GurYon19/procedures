# saving and working requirements for projects
using conda:<br />
save requirements.txt: conda list -e > requirements.txt<br />
create conda env: conda create --name --file requirements.txt<br />

using pip:<br />
save requirements: pip list --format=freeze > requirements.txt<br />
install rquirements : pip install -r requirements_<br />
