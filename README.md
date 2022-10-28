# Tensorflow-m1-mac
how to install tensorflow on your m1 mac. Making this tutorial as I experienced hell when i tried to install tensorflow


# step 1: install miniconda

- First we need to remove anaconda if we have it installed already 
```
conda install anaconda-clean
anaconda-clean
```
- After doing that you can run either of these 3 commands depending on where the anaconda3 folder is stored
```
rm -rf anaconda3
rm -rf ~/anaconda3
rm -rf ~/opt/anaconda3
```

- Download miniconda package manager 
Here is the link: https://docs.conda.io/en/latest/miniconda.html
![Screenshot 2022-10-24 at 1 01 16 PM](https://user-images.githubusercontent.com/56480632/197451872-e15dd5a4-e354-42a8-a82f-6bb18bf9dc29.png)
After downloading, just follow the instructions displayed. 

# step 2: verify python installation
- Checking python platform information
Go to your terminal and type in `python3`
and then run the code below
```
import platform
platform.platform()
```
You should have the same result as the screenshot below otherwise you have to reinstall python
<img width="646" alt="Screenshot 2022-10-24 at 1 06 31 PM" src="https://user-images.githubusercontent.com/56480632/197452213-3e4b50ed-2b85-4656-ad4b-15365f527d5e.png">

# step 3: install xcode
- You should also install xcode tools, to do that run the command below
`xcode-select --install`

# step 4: Install jupyter and environment
- Download the `tensorflow-apple-metal-conda.yml` file and save the file to your Downloads folder
- After that change into the Downloads folder by doing `cd Downloads`
- Run this command `conda deactivate`
- After that do the following installations: 
  - `conda install -y jupyter`
  - Run the command `conda env create -f tensorflow-apple-metal-conda.yml -n tensorflow`
- Now we need to activate and register our environment 
  - `conda activate tensorflow`
  - `python -m ipykernel install --user --name tensorflow --display-name "Python 3.9 (tensorflow)"`

# step 5: Testing
- To test the environment run the jupyter notebook by going to terminal and typing `jupyter notebook`
- open a new jupyter notebook file and change the kernel to tensorflow
- type in the following python code to test: 
  ```
  import tensorflow as tf
  tf.__version__
  ```

Congratulations, you have now installed tensorflow 🎉
