# MIST 4610 Group Project 1 
### Group Name:

Sp24_47114_Group 1

### Group Members:

Isabelle Kiser 
[@isabellekiser](https://github.com/isabellekiser)

Will Cobb 
[@wjc56122](https://github.com/wjc56122)

Bhavik Maniklal 
[@BhavikManiklal](https://github.com/BhavikManiklal ) 

Ty Marcinczyk 
[@TylerMar1](https://github.com/TylerMar1)

Ryan Schoessling 
[@rschoess3](https://github.com/rschoess3)

Jaiden Timmons 
[@jaidentimmons](https://github.com/jaidentimmons)

### Client Scenario Overview:

Community FC, under the dynamic leadership of the owner, has established itself as a cornerstone of local soccer culture, offering extensive programs that cater to various age groups, skill levels, and interests. The club aims to nurture talent, promote physical well-being, and foster a sense of community through soccer. Its offerings include youth and adult leagues, training camps, weekend tournaments, and special events like workshops and clinics with professional players.

The club's facilities are top-notch, featuring multiple soccer fields, a clubhouse with locker rooms, a gym, and a merchandise shop. Community FC prides itself on its inclusive environment, welcoming members from various backgrounds to participate in its programs.

### Project Problem:

At Community FC, our primary challenge revolves around the complex coordination needed to manage our soccer club efficiently. From member management and team organization to league administration, facility scheduling, financial transactions, and merchandise sales, many interconnected elements require seamless integration.

Coordinating member profiles, team assignments, league participation, facility bookings, financial transactions, and merchandise inventory demands meticulous attention to detail and effective communication among staff, coaches, players, and parents.

To tackle this challenge, we require a relational database system that can streamline these processes, providing real-time visibility into club operations and facilitating smooth coordination across all facets of our organization. This solution will enable us to enhance member experiences, optimize resource utilization, and uphold Community FC's commitment to excellence in our local soccer community.

### Data Model:
![DataModelpic](https://github.com/isabellekiser/Soccer-Team/assets/149964200/0969a4d6-e0a9-46c0-8d85-15938972a8c4)

Our data model is based on the structure of a hypothetical professional soccer club. The Member entity represents individual members of the club. A member can be a player, coach, athletic trainer, etc. This is represented by the “role” attribute within member. A member is further detailed by the entity Membership which is related to Member with a many-to-one relationship. A member may have multiple membership types if they have multiple duties with the club. 

Member is also related to Transactions with a one-to-many relationship which shows that a member can make multiple transactions with the club. Our soccer club also sells merchandise. The transaction is related to the Merchandise entity through a many-to-one relationship. This represents that a piece of merchandise can be sold in multiple transactions.

Our soccer club has many different teams ranging from the highest level professional teams to many developmental teams where we have players that we believe will one day be good enough to play on our top team. The Team entity is related to Member with a many-to-many relationship through the associative entity MemberTeam. MemberTeam represents the different team members on each team.

Since we have multiple teams with different skill levels, naturally they play in different leagues. The League entity is related to team through a one-to-many relationship. This is because a league hold host to many different teams, but a team can only play in one league.

Each team has a number of different matches they play throughout the season. This is why Team is related to the Matches entity through a many-to-many relationship with the associated entity TeamMatches. TeamMatches represents the individual matches and which team played in the match.

Our players will only get better if they practice their craft. This is why we host multiple training sessions per week. Team is connected to the TrainingSession entity by a one-to-many relationship. This represents how one team has many different training sessions. These training sessions take place in one of our state-of-the-art facilities. The Facility entity is connected to TrainingSession by a one-to-many relationship because a facility can host many different training sessions.

Since our facilities are so nice, we also host matches in these facilities. This is why Facility has a one-to-many relationship with the Matches entity. One facility will host many matches.

Being such a popular soccer club, we have many spectators at every game. The spectators have to buy tickets to gain admission to the matches. This is why there is a one-to-many relationship between Matches and the Ticket entity. One match will have many tickets.

### Data Dictionary:
# ![facility table](https://github.com/isabellekiser/Soccer-Team/assets/149964200/7c653ca1-baa1-47d7-939e-9fc8659a3bac)
# ![league table](https://github.com/isabellekiser/Soccer-Team/assets/149964200/323a022f-6323-4773-ba2c-74be7007c44e)
# ![Matches table](https://github.com/isabellekiser/Soccer-Team/assets/149964200/c9423233-45d4-4ebb-bac0-8870db6f7354)
# ![member table](https://github.com/isabellekiser/Soccer-Team/assets/149964200/723b2a7f-c405-41ca-9f8d-af394346bc80)
# ![membership](https://github.com/isabellekiser/Soccer-Team/assets/149964200/693112a9-098b-4c38-a58e-179d7800a526)
# ![memberteam](https://github.com/isabellekiser/Soccer-Team/assets/149964200/49d3644e-f895-4fc2-9772-ea213566af57)
# ![merchandise](https://github.com/isabellekiser/Soccer-Team/assets/149964200/57f318a3-1e06-4688-9380-3c50bd3224f2)
# ![teammatches](https://github.com/isabellekiser/Soccer-Team/assets/149964200/90482a3b-b63f-4bdb-947c-0a0099d2e614)
# ![ticket](https://github.com/isabellekiser/Soccer-Team/assets/149964200/041dde10-9805-45e5-917b-72d627dfc7a4)
# ![training session](https://github.com/isabellekiser/Soccer-Team/assets/149964200/c238d21b-eb68-45d6-9659-c365abccb6dd)
# ![transaction](https://github.com/isabellekiser/Soccer-Team/assets/149964200/080d167a-cc50-40d8-aa7f-1e323001dad9)
# ![team](https://github.com/isabellekiser/Soccer-Team/assets/149964200/e406d8ea-69ca-4ccb-8b92-74c8a9fc2be0)

### Queries:
<img width="760" alt="Screenshot 2024-03-27 at 4 57 14 PM" src="https://github.com/isabellekiser/Soccer-Team/assets/150088753/96ebecb4-8f05-4fc1-8f98-fdbe39497afa">

Query 1:
# ![query 1](https://github.com/isabellekiser/Soccer-Team/assets/149964200/8ef2d313-7802-407e-bb86-dea37f59fc90)
Query 1 selects product names and their corresponding stock levels from the "Merchandise" table, filtering for items with stock levels below 40 and prices exceeding 50. This provides managers with a concise list of high-value products that are running low on stock, aiding in strategic inventory management. By prioritizing restocking efforts for these items, managers can ensure the availability of profitable products to meet customer demand, optimize inventory levels, and minimize the risk of stockouts, thereby enhancing sales and customer satisfaction.

Query 2:
# ![query 2](https://github.com/isabellekiser/Soccer-Team/assets/149964200/bce6e505-feab-4b6d-9c38-925385fbd406)
Query 2 aggregates data from a training session database, counting the occurrences of each focus area within the sessions. This information is invaluable for managers as it provides a clear snapshot of where training efforts are being directed. By identifying which skills or topics receive more attention, managers can allocate resources more effectively, tailor training programs to address specific needs and ensure a balanced approach to skill development within the organization. Additionally, it enables managers to pinpoint areas of strength and areas needing improvement, facilitating informed decision-making to optimize workforce performance and achieve organizational goals efficiently.

Query 3:
# ![query 3](https://github.com/isabellekiser/Soccer-Team/assets/149964200/f2eb3074-85a9-47a3-9c65-27fddb524384)


Query 4:
# ![query 4](https://github.com/isabellekiser/Soccer-Team/assets/149964200/9de8f5a8-f84d-4f2f-b736-bb9c49171dfb)
Query 4 retrieves the genders of members whose memberships are set to end in 2024 by joining the "Membership" table with the "Member" table on their respective IDs and filtering for memberships ending in that year. This information is crucial for soccer team management as it allows them to understand the demographic composition of expiring memberships, which in turn informs targeted retention strategies, marketing efforts, and resource allocation. By knowing the genders of members whose memberships are ending, the management can tailor communication, programming, and facilities to better cater to the diverse preferences of their membership base, ultimately fostering greater engagement and ensuring the club's long-term success.

Query 5:
# ![query 5](https://github.com/isabellekiser/Soccer-Team/assets/149964200/8b6ba846-7031-419c-94c1-34856b74d720)


Query 6:
# ![query 6](https://github.com/isabellekiser/Soccer-Team/assets/149964200/cdca4ca4-8794-4772-9a60-a7a1cc5642f0)


Query 7:
# ![query 7](https://github.com/isabellekiser/Soccer-Team/assets/149964200/72d5c9e0-999e-4d5e-b2c6-f522c0d96e3e)


Query 8:
# ![query 8](https://github.com/isabellekiser/Soccer-Team/assets/149964200/ce3c7421-68c6-48f3-9448-09d874c78a9c)


Query 9:
# ![query 9](https://github.com/isabellekiser/Soccer-Team/assets/149964200/ce6d7ba0-b8cf-482f-8670-64e769fafd63)


Query 10:
# ![query 10](https://github.com/isabellekiser/Soccer-Team/assets/149964200/4e37e059-22b8-4e50-964c-632b93956060)


### Database information:
Name of the database: Sp24_47114_Group 1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
