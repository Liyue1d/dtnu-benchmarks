# dtnu-benchmarks

File 10-20.txt containts 500 DTNUs. Each DTNUs has between 10 to 20 controllables and 1 to 3 uncontrollables.

File 20-25.txt containts 500 DTNUs. Each DTNUs has between 20 to 25 controllables and 1 to 3 uncontrollables.

File 25-30.txt containts 500 DTNUs. Each DTNUs has between 25 to 30 controllables and 1 to 3 uncontrollables.

Each DTNU is written as:

-Set of controllables: A list which contains the ID of each controllable timepoint

-Set of uncontrollables: A list which contains the ID of each unontrollable timepoint

-Set of free constraints: A list which contains 'disjuncts' (i.e. A disjunct refers to several contraints linked with OR operators). A disjunct is a list which contains several 'conjuncts'. 
A conjunct is a list of the form: 
Either [timepoint1, timepoint2, lower_bound, upper_bound], and represents the constraint timepoint1 - timepoint2 \in [lower_bound, upper_bound]
Or either [timepoint, lower_bound, upper_bound] and represents the constraint timepoint \in [lower_bound, upper_bound]

-Set of contigency links: A dictionnary with multiple entry. Each key of the dictionnary is a controllable timepoint which triggers the activation of an uncontrollable timepoint. The associated value of the key is a list which containts, as first element, the ID of the uncontrollable timepoint which gets triggered, and as second element a list of time bounds, each of which the activated uncontrollable timepoint may occur in.
