# Protein-protein-interaction-based-multi-objective particle-swarm-optimization

Author :- Pratik Dutta, Sriparna Saha and Sukanya Naskar


Multi-Objective Particle Swarm Optimization , as the name suggests deals with multiple objective functions alongside the PSO method to find the non-redundant particles from a population of given particles.

This code is an implementation of MultiObjective Particle Swarm Optimization algorithm based on Crowding Distance values.

MOPSO_MAIN contains the main function to execute the process.

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

After this , the particle Fitness Valius is again updated.

Correspondingly, the Archive is again upddated to insert new non-dominated Particles in the archive

The Velocity , Position, personal Best Values of each particle in the population is updated subsequently.

