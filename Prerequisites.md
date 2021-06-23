**Miniconda3 Installation** 

Keep in mind that this installation is for a environment that doesn’t affect other packages that you may already have in your system. One advantage of doing this installation is that miniconda also installs pip to manage packages.

**Linux**

The installation steps for a Linux based are quite simple, you may need to install the develop tools corresponding to your linux OS (check https://www.garron.me/en/go2linux/gnu-gcc-development-tools-linux-fedora-arch-debian.html), 


**but we suggest you try first the installation as follows, you might be lucky!**

1. Download the installation file for python3.8 from: https://conda.io/miniconda.html. Most 

2. In the directory where the installation file is run

	  ~]$ bash Miniconda3-py39_4.9.2-Linux-x86_64.sh

3. Follow the installation directions. It will ask you where to install, the default is “/home”. 
   In the part where it ask you to write the Miniconda3 path in the bash profile write “no”.

4. After the installation is done close the terminal window and open it again. 

5. Next write in the terminal

	  ~]$ cd

    ~]$ source Miniconda3/bin/activate
	
   ~]$ conda list
  
  if the installation was right a list of packages should appear in the terminal window.

6. Installing necessary packages.

	  ~]$ conda install numpy
  
    ~]$     “         “     scipy
	
    ~]$     “         “     matplotlib
	
    ~]$     “         “     jupyter
	
    ~]$     “         “     sympy
  
  or conda install numpy scipy matplotlib jupyter sympy h5py
   
8. To check the installation of the packages run in the terminal 

    ~]$ python
    
    ~]$ import numpy
    
    ~]$ import matplotlib.pyplot as plt (this is the proper way to import matplotlib)
    
    ~]$ exit() (to exit python and return to the terminal)

9. Also check to run Jupyter notebooks. Type the following in the terminal:

  	~]$ jupyter notebook
  
     This will open a window in your web explorer (the default one). Now you are all set and ready. You may want to try and play, there is plenty of documentation  on the web. To exit jupyter just close the window, and the terminal. 
  
10. To exit the miniconda environment write

  	~]$ source deactivate 	



11. If when trying to import matplotlib you get the error: ImportError: No module named ‘tkinter' exit python and run
	
  	~]$ conda instal tkinter 
	
	or
	
  	~]$ pip install tkinter
  
12. in python run 

  	>>import matplotlib

    >>matplotlib.use('Agg')
	
    >>import matplotlib.pyplot as plt

	to choose the default plot window.

	**MacOS:**

  If you are new in Mac OS X but are experienced in Linux, you will be happy to use the Terminal in a way quite similar to Ubuntu; but first, you will have to spend two or three hours installing the basics. (If you already have xcode installed, skip steps 1-3)

You should install the following packages respecting the order in the list. 

1. Install Xcode from AppStore (it is free)

2. Install Command Line Tools

	  ~]$  xcode-select —install

3. Agree the terms of licence

  	~]$ sudo xcodebuild -license

4. Download the installation file for python3.8 from: https://conda.io/miniconda.html. Most 

5. In the directory where the installation file is run

	  ~]$ bash Miniconda3-latest-MacOSX-x86_64.sh

6. Follow the installation directions. It will ask you where to install, just type "yes" to select the default.  In the part where it ask you to write the Miniconda2 path in the bash profile write “no”.

7. After the installation is done close the terminal window and open it again. 

8. Next write in the terminal

  	~]$ cd
	
  	~]$ source Miniconda3/bin/activate
	
	  ~]$ conda list
  
  if the installation was right a list of packages should appear in the terminal window

9. Installing necessary packages.

  	~]$ conda install numpy scipy matplotlib jupyter sympy h5py

10. To check the installation of the packages run the following lines in the terminal 

    ~]$ python
	
    ~]$ import numpy
	
    ~]$ import matplotlib.pyplot as plt 
	
    ~]$ exit() (this way you exit python)

11. To run Jupyter notebooks run in the terminal

	  ~]$ jupyter notebook
    
    
     This will open a window in your web explorer (the default one). And you are all set and ready. You may want to try and play. 
     
     There is plenty of documentation  on the web. 
     
     To exit jupyter just close the window, and the terminal. 
  
12. To exit the miniconda environment write

    ~]$ source deactivate 	
  
	**Windows** 

 We strongly advise not to use windows, because we will not be able to help you if you have troubles, but if you insist you should follow the instructions in https://conda.io/docs/install/quick.html#windows-miniconda-install, and good luck!
