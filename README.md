Installing open face using Anaconda:

Step 1: The first step is the installation of dlib using one of the following methods:
  1. Install dlib library using https://github.com/menpo/conda-dlib
  2. Alternatively the following link can be used: https://anaconda.org/menpo/dlib
    * The later approach provide the user with a command excecutable in the terminal.


If you complete all steps, dlib will be installed in _test environment by using the first approach.
By using the second approach the dlib can be installed in arbitrary virtual environment.

Step 2: Activate _test environment using this command:

$ source activate _test

Step 3: Install opencv, numpy, pandas, scipy, scikit-learn, and scikit-image packages using Anaconda in your _test environment.

(_test environment should be activated when you are installing the packages and the python path should be something like:

$ which python ~/anaconda/envs/_test/bin/python)

Step 4: After installing all packages you should deactivate _test environment using this command: <br />
source deactivate _test

Step 5: Install torch using:

http://torch.ch/docs/getting-started.html#_

And install all necessary packages using this command:

$ for NAME in dpnn nn optim optnet csvigo cutorch cunn fblualib torchx tds; do luarocks install $NAME; done

Step 6: Install open face in _test environment using following commands:

$ source activate _test $ git clone https://github.com/cmusatyalab/openface.git ~/openface $ cd openface $ cd sudo python setup.py install $ models/get-models.sh

Open face is installed in your machine. You can test it using:

$ ./demos/classifier.py infer models/openface/celeb-classifier.nn4.small2.v1.pkl ./images/examples/carell.jpg

The output would be:

=== ./images/examples/carell.jpg === Predict SteveCarell with 0.97 confidence.
