jee6-parent
===========

maven parent pom project, it contains all jee 6 needed dependencies.

# Profiles #
The pom contains some profiles, whose aim is to simulate pom multiple inheritance. Each project inherits from the same parent, but as needed can activate a specific profile to enble a specifc behaviour.  
For instance the profile ejb-cdi contains the needed ejb-cdi dependencies, to active it you have to add a snippet like the following to the project pom:

		<profile>
			<id>ejb-cdi</id>
			<activation>
				<activeByDefault>true</activeByDefault>
			</activation>
		</profile>
		
The available profiles are:  

* ejb-cdi
* jpa
* jsf
* rest

