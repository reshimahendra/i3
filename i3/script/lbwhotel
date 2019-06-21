#/bin/bash
function finish {
    echo "kill port:8000 used by Django before finish"
    fuser -k 8000/tcp
}
echo "set virtual environtment"
#set -x
source $HOME/.local/bin/virtualenvwrapper.sh
workon lbwhotel
#set +x
echo "run django local server and watch sass"
python3 $HOME/projects/lbwhotel/manage.py runserver & scss --watch $HOME/projects/lbwhotel/theme-design/abian/scss/style.scss:$HOME/projects/lbwhotel/lotus/static/abian_theme/css/abian.css

# trap and clean script resources before finish
trap finish EXIT
