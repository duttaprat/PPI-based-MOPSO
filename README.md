# PPI-based-MOPSO
A Multi-objective based PSO Approach for Inferring Pathway Activity utilizing Protein Interactions

## This is the readme file that contains the guidelines and information about the compilation of the code of the following paper

**Paper Name:-** [A Multi-objective based PSO Approach for Inferring Pathway Activity utilizing Protein Interactions]()

- **Authors:** Pratik Dutta<sup>1</sup>, Sriparna Saha<sup>1</sup> and Sukanya Naskar<sup>2</sup>.
- **Affiliation:** <sup>1</sup>Department of Computer Science and Engineering, Indian Institute of Technology Patna; <sup>2</sup>Department of Information Technology, Indian Institute of Engineering Science and Technology Shibpur.  
- **Accepted:(26/06/2020):** [Multimedia Tools and Applications, Springer](https://www.springer.com/journal/11042/)





Requirements : - Python 2.7, Numpy

<b>Multi-Objective Particle Swarm Optimization</b> , as the name suggests deals with multiple objective functions alongside the PSO method to find the non-redundant particles from a population of given particles.

This code is an implementation of MultiObjective Particle Swarm Optimization algorithm based on Crowding Distance values.

<b>MOPSO_MAIN</b> contains the main function to execute the process.

At the very beginning , swarm size , archive size and number of iterations have been declared.

Then, the positions and velocities of each particle with respect to their individual dimensions have been initialised by calling the function init_PARTICLE_VALUES.initialise_PARTICLE_VALUES() and init_VELOCITY.initilaise_velocity() respectively.

Next , fitness of each particle in the population is initialised based on the three objective functions --
	
	1. WEIGHTED T SCORE
	2. WEIGHTED Z SCORE
	3. PROTEIN PROTEIN INTERACTION SCORE

The store_pBest.p_Best() function stores the personal best of each particle in the population.

In the next step, nondominated particle values are initialised in the archive by the init_NONDOMINATED_SOLUTION.initialise_nondom_sol() function.

The DELETE_PARTICLE.delete_particle() function is used to delete dominated particles present in the archive.

If the number of nondominated solutions exceed the given archive size then the function CROWDING.crowding_distance() helps to compute the crowding distances of the particles present in the archive to replace particles in the archive(if any)

Computation of crowding distance consists of three steps --

	1.Fitness Values sorting
	2.Computation of Crowding Distances
	3.Sorting of particles present in the crowd

Correspondingly, the Archive is again updated to insert new non-dominated particles in the archive

The Velocity , Position, personal Best Values of each particle in the population is updated subsequently.



## Contribution
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


