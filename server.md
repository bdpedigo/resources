to start a local-server tunnel
ssh -N -L localhost:8810:localhost:8810 <user>@<comp>.neurodata.io

start a jupyter notebook 
jupyter notebook --no-browser --port=8810

rsync -avzhe ssh <localdir> <user>@<comp>.neurodata.io:/data/...
