Group Name:
Sp24_47114_Group1

Group Members:
Bhavik Maniklal, Isabella Kiser, Jaiden Timmons, Ryan Schoessling, Tyler Marcinczyk, Will Cobb

Problem Description: 

At Community FC, our primary challenge revolves around the complex coordination needed to manage our soccer club efficiently. From member management and team organization to league administration, facility scheduling, financial transactions, and merchandise sales, there's a multitude of interconnected elements that require seamless integration.

Coordinating member profiles, team assignments, league participation, facility bookings, financial transactions, and merchandise inventory demands meticulous attention to detail and effective communication among staff, coaches, players, and parents.

To tackle this challenge, we require a relational database system that can streamline these processes, providing real-time visibility into club operations and facilitating smooth coordination across all facets of our organization. This solution will enable us to enhance member experiences, optimize resource utilization, and uphold Premier FC's commitment to excellence in our local soccer community.


Client Scenario Overview:

Community FC, under the dynamic leadership of the owner, has established itself as a cornerstone of local soccer culture, offering extensive programs that cater to various age groups, skill levels, and interests. The club operates with a mission to nurture talent, promote physical well-being, and foster a sense of community through soccer. Its offerings include youth and adult leagues, training camps, weekend tournaments, and special events like workshops and clinics with professional players.

The club's facilities are top-notch, featuring multiple soccer fields, a clubhouse with locker rooms and a gym, and a merchandise shop. Community FC prides itself on its inclusive environment, welcoming members from various backgrounds to participate in its programs.

Data Model

![updatedDataModel](https://github.com/BhavikManiklal/Soccer-Team-Group-1/assets/150094078/b25e9a7d-0bc4-474f-b97f-7782484e9b8d)


Explanation of data model:

Our data model is based on the structure of a hypothetical professional soccer club. The Member entity represents individual members of the club. A member can be a player, coach, athletic trainer, etc. This is represented by the “role” attribute within member. A member is further detailed by the entity Membership which is related to Member with a many to one relationship. A member may have multiple membership types if they have multiple duties with the club. 

Member is also related to Transaction with a one to many relationship which shows that a member can make multiple transactions with the club. Our soccer club also sells merchandise. Transaction is related to the Merchandise entity through a many to one relationship. This represents that a piece of merchandise can be sold in multiple transactions.

Our soccer club has many different teams ranging from the highest level professional teams to many developmental teams where we have players that we believe will one day be good enough to play on our top team. The Team entity is related to Member with a many to many relationship through the associative entity MemberTeam. MemberTeam represents the different team members on each team.

Since we have multiple teams with different skill levels, naturally they play in different leagues. The League entity is related to team through a one to many relationship. This is because a a league hold host to many different teams, but a team can only play in one league.

Each team has a number of different matches they play throughout the season. This is why Team is related to the Matches entity through a many to many relationship with the associated entity TeamMatches. TeamMatches represents the individual matches and which team played in the match.

Our players will only get better if they practice their craft. This is why we host multiple training sessions per week. Team is connected to the TrainingSession entity by a one to many relationship. This represents how one team has many different training sessions. These training sessions take place in one of our state of the art facilities. The Facility entity is connected to TrainingSession by a one to many relationship because a facility can host many different training sessions.

Since our facilities are so nice, we also host matches in these facilities. This is why Facility has a one to many relationship with the Matches entity. One facility will host many matches.

Being such a popular soccer club, we have many spectators at every game. The spectators have to buy tickets to gain admission to the matches. This is why there is a one to many relationship between Matches and the Ticket entity. One match will have many tickets.


Data Dictionary:














