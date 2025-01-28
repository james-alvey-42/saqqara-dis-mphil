# DIS MPhil Project 2024-25

Github: https://github.com/james-alvey-42/saqqara-dis-mphil/tree/template-powerlaw
Branch: dis-mphil
Paper: https://arxiv.org/pdf/2309.07954

## Suggested Install Steps

- Create a fresh python environment (try 3.9/3.10 first)
- Follow the pip install instructions on the github README
- Be careful to check versions of pytorch lightning, torch, bilby, and swyft

## Possible introductoory tasks/questions

These are in no particular order, they are really just meant as suggestions to get you going and understanding the code/data structures etc.

- Run through the introductory `Example_notebook.ipynb` in the saqqara folder
- Look at the example config file and the README to understand the inputs (`examples/config_files/template_powerlaw.ini`)
- Try running the `generate_observation.py` script with a suitable config file
- How do you load and plot an observation?
- Where is the simulation data stored? How do you load it? (Hint: Zarrstore is used extensively, try making some plots of the simulation output)
- What is the data shape? How many simulations are there? What are the storage requirements?
- Where is the observation stored for the MCMC sampling? Check that it corresponds to the base observation
- Try running the `likelihood_based/sampling.py` code with the example config
- What output does this produce?
- Can you plot the outputs? (Hint: Load them with np.load, then look into the chainconsumer package)
- Where is the likelihood coded up? Can you find the corresponding expression in a paper?
- Where is the network architecture implemented?
- Can you find any tutorials for the swyft package online?
- What happens if you change the method flag from tmnre to anre?
- What GPU resources do you have available? Estimate the amount of compute you will require
- Write out a schematic for what the tmnre.py script does (i.e. what steps are involved)
- How do you reload a trained network?
- What do the different config options in the [DATA OPTIONS] section do to the observations?
- What sort of values for the validation loss do you observe? How many epochs does it take on simple problems?
- Estimate the storage requirements for the full run (given the config, ask when ready)
- How do you plot the logratio output? (Hint: swyft.corner)
- How can you compare the output of the sampling code and the SBI code?
- How do you load and plot a logratios object? (Hint: they are both pickle files, use e.g. `pd.read_pickle`)
- What is the difference between the tmnre and anre options in the implmeentation?

## Project Goal

The main goal of this project is to reproduce something similar to the black dashed and solid contours in Fig. 1 of https://arxiv.org/pdf/2309.07954. NOTE: There is no need to generate any transients (orange contours and excess in the inset figure). Also no need to study a different case study compared to the one in the paper (i.e. don't need to change the injection parameters).
