# Group 1 MIST 4610 Project 1
## Group Name:
Sp24_47114_Group1

## Group Members:
Bhavik Maniklal:  [@BhavikManiklal](https://github.com/BhavikManiklal ) 

Isabella Kiser:  [@isabellekiser](https://github.com/isabellekiser)

Jaiden Timmons:  [@jaidentimmons](https://github.com/jaidentimmons)

Ryan Schoessling:  [@rschoess3](https://github.com/rschoess3)

Tyler Marcinczyk:  [@TylerMar1](https://github.com/TylerMar1)

Will Cobb: [@wjc56122](https://github.com/wjc56122)


## Problem Description: 

At Community FC, our primary challenge revolves around the complex coordination needed to manage our soccer club efficiently. From member management and team organization to league administration, facility scheduling, financial transactions, and merchandise sales, there's a multitude of interconnected elements that require seamless integration.

Coordinating member profiles, team assignments, league participation, facility bookings, financial transactions, and merchandise inventory demands meticulous attention to detail and effective communication among staff, coaches, players, and parents.

To tackle this challenge, we require a relational database system that can streamline these processes, providing real-time visibility into club operations and facilitating smooth coordination across all facets of our organization. This solution will enable us to enhance member experiences, optimize resource utilization, and uphold Premier FC's commitment to excellence in our local soccer community.


## Client Scenario Overview:

Community FC, under the dynamic leadership of the owner, has established itself as a cornerstone of local soccer culture, offering extensive programs that cater to various age groups, skill levels, and interests. The club operates with a mission to nurture talent, promote physical well-being, and foster a sense of community through soccer. Its offerings include youth and adult leagues, training camps, weekend tournaments, and special events like workshops and clinics with professional players.

The club's facilities are top-notch, featuring multiple soccer fields, a clubhouse with locker rooms and a gym, and a merchandise shop. Community FC prides itself on its inclusive environment, welcoming members from various backgrounds to participate in its programs.

## Data Model

![updatedDataModel](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/b25e9a7d-0bc4-474f-b97f-7782484e9b8d)


## Explanation of data model:

Our data model is based on the structure of a hypothetical professional soccer club. The Member entity represents individual members of the club. A member can be a player, coach, athletic trainer, etc. This is represented by the “role” attribute within member. A member is further detailed by the entity Membership which is related to Member with a many to one relationship. A member may have multiple membership types if they have multiple duties with the club. 

Member is also related to Transaction with a one to many relationship which shows that a member can make multiple transactions with the club. Our soccer club also sells merchandise. Transaction is related to the Merchandise entity through a many to one relationship. This represents that a piece of merchandise can be sold in multiple transactions.

Our soccer club has many different teams ranging from the highest level professional teams to many developmental teams where we have players that we believe will one day be good enough to play on our top team. The Team entity is related to Member with a many to many relationship through the associative entity MemberTeam. MemberTeam represents the different team members on each team.

Since we have multiple teams with different skill levels, naturally they play in different leagues. The League entity is related to team through a one to many relationship. This is because a a league hold host to many different teams, but a team can only play in one league.

Each team has a number of different matches they play throughout the season. This is why Team is related to the Matches entity through a many to many relationship with the associated entity TeamMatches. TeamMatches represents the individual matches and which team played in the match.

Our players will only get better if they practice their craft. This is why we host multiple training sessions per week. Team is connected to the TrainingSession entity by a one to many relationship. This represents how one team has many different training sessions. These training sessions take place in one of our state of the art facilities. The Facility entity is connected to TrainingSession by a one to many relationship because a facility can host many different training sessions.

Since our facilities are so nice, we also host matches in these facilities. This is why Facility has a one to many relationship with the Matches entity. One facility will host many matches.

Being such a popular soccer club, we have many spectators at every game. The spectators have to buy tickets to gain admission to the matches. This is why there is a one to many relationship between Matches and the Ticket entity. One match will have many tickets.


## Data Dictionary:

 ![facility table](https://github.com/isabellekiser/Soccer-Team/assets/149964200/7c653ca1-baa1-47d7-939e-9fc8659a3bac)
 ![league table](https://github.com/isabellekiser/Soccer-Team/assets/149964200/323a022f-6323-4773-ba2c-74be7007c44e)
 ![Matches table](https://github.com/isabellekiser/Soccer-Team/assets/149964200/c9423233-45d4-4ebb-bac0-8870db6f7354)
 ![member table](https://github.com/isabellekiser/Soccer-Team/assets/149964200/723b2a7f-c405-41ca-9f8d-af394346bc80)
 ![membership](https://github.com/isabellekiser/Soccer-Team/assets/149964200/693112a9-098b-4c38-a58e-179d7800a526)
 ![memberteam](https://github.com/isabellekiser/Soccer-Team/assets/149964200/49d3644e-f895-4fc2-9772-ea213566af57)
 ![merchandise](https://github.com/isabellekiser/Soccer-Team/assets/149964200/57f318a3-1e06-4688-9380-3c50bd3224f2)
 ![teammatches](https://github.com/isabellekiser/Soccer-Team/assets/149964200/90482a3b-b63f-4bdb-947c-0a0099d2e614)
 ![ticket](https://github.com/isabellekiser/Soccer-Team/assets/149964200/041dde10-9805-45e5-917b-72d627dfc7a4)
 ![training session](https://github.com/isabellekiser/Soccer-Team/assets/149964200/c238d21b-eb68-45d6-9659-c365abccb6dd)
 ![transaction](https://github.com/isabellekiser/Soccer-Team/assets/149964200/080d167a-cc50-40d8-aa7f-1e323001dad9)
 ![team](https://github.com/isabellekiser/Soccer-Team/assets/149964200/e406d8ea-69ca-4ccb-8b92-74c8a9fc2be0)

## Data Queries

![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/71b37faf-1a65-4afa-afb4-1c890e870d5b)


### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/ca83e122-cdeb-4c96-8b29-1e80375ca5ad)

### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/60a5fbc8-33e5-4641-a902-66eb27098781)

### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/2e820d20-9b3a-4217-86f4-3f20e7732e58)

### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/e258344e-6700-4ecf-b01a-26be769c39e1)

### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/c127858d-06ee-4cc5-97a4-459b4ff03d7d)

### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/b693c20d-8510-44c6-a000-269696a608f3)

### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/01fecfe5-2413-4d74-8534-06e8db16fab1)

### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/cc3b331e-ddcb-4f2d-b4d1-bec65d6d768b)

### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/c32b8be3-895d-4200-a420-f5bc098362a8)

### ![image](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/67de1749-30bf-42d6-8e65-10e06bab971b)






## Database information:
Name of the database: Sp24_47114_Group 1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();









