Installing open face using Anaconda:

Step 1. Install `miniconda` with:
* `wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh`
* `bash Miniconda3-latest-Linux-x86_64.sh` and follow instructions.
* Add a Python 2.7 environment with: `conda create --name openface python=2.7`
* Activate the new env with: `source activate openface`


Step 2. Install dependencies
* Add the `conda-forge` channel with: `conda config --add channels conda-forge`
* `conda install opencv numpy pandas scipy scikit-learn scikit-image dlib`

Step 3. Install Torch
* Deactivate the `openface` environment by opening a new terminal.
* Follow the instructions on [torch.ch/docs/getting-started.html](http://torch.ch/docs/getting-started.html#_), this will take a while.

Step 4. Install Torch dependencies
* Execute: `for NAME in dpnn nn optim optnet csvigo cutorch cunn fblualib torchx tds; do luarocks install $NAME; done`

Step 6: Install open face in `openface` environment using following commands:
* `source activate openface`
* `git clone https://github.com/cmusatyalab/openface.git ~/openface` 
* `cd openface` 
* `python setup.py install`
* `./models/get-models.sh

Open face is now installed. Test it with:
* `./demos/classifier.py infer models/openface/celeb-classifier.nn4.small2.v1.pkl ./images/examples/carell.jpg`

The output should be:

=== ./images/examples/carell.jpg === Predict SteveCarell with 0.97 confidence.
