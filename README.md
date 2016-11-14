This notebook implements a spectral analysis of nuclear magnetic resonance (NMR) and nuclear quadrupole resonance (NQR) spectra for a crystal structure with arbitrary spin number. Here a single spin sensor (i.e. an individual nitrogen-vacancy (NV) center in diamond) is used to probe nuclear spins within the crystal. 

The analysis below follows the procedure developed in "Nanoscale Magnetic Resonance Spectroscopy of an Atomically Thin Material Using a Single Spin Qubit" by Lovchinsky et. al., 2016.

Notes:

	1). Update the file 'parameters_hBN.txt' with the desired spectrum parameters. 
		The required parameters are:

		spin: the quantum number of the nuclear spin
		Ngyro: gyromagnetic ratio of nuclear spin 
    		NVang: angle of NV axis
		Npi: number of applied pi-pulses on electronic spin
		density: target spin density

		The function 'initializeParameters' reads these values into a Python dictionary. 

	2). You also need to make sure the necessary constants are included in the file 'constants.txt'. 
		The required constants are:

		hbar: reduced Planck?s constant [m^2 kg s^-1]
    		Egyro: gyromagnetic ratio of electronic spin sensor 
		mu_B: Bohr magneton [J T^-1]
		u_0: permeability of free space [T m A^-1]
		
		The function 'initializeConstants' reads these values into a Python dictionary. 
    
  	3). The file 'hBNdata.txt' contains the experimental spectrum.

	4). The file 'hBN_multispectra.txt' contains extracted parameters for several bulk, bilayer
    		and monolayer measurements.

	5). The file 'priors_hBN.txt' contains the priors on fit parameters.
