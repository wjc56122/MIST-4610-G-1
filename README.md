# MIST 4610 Group Project 1 
### Group Name

Sp24_47114_Group 1

### Group Members
Isabelle Kiser, Will Cobb, Bhavik Maniklal, Ty Marcinczyk, Ryan Schoessling, Jaiden Timmons

### Client Scenario Overview:

Community FC, under the dynamic leadership of the owner, has established itself as a cornerstone of local soccer culture, offering extensive programs that cater to various age groups, skill levels, and interests. The club aims to nurture talent, promote physical well-being, and foster a sense of community through soccer. Its offerings include youth and adult leagues, training camps, weekend tournaments, and special events like workshops and clinics with professional players.

The club's facilities are top-notch, featuring multiple soccer fields, a clubhouse with locker rooms, a gym, and a merchandise shop. Community FC prides itself on its inclusive environment, welcoming members from various backgrounds to participate in its programs.

### Project Problem

At Community FC, our primary challenge revolves around the complex coordination needed to manage our soccer club efficiently. From member management and team organization to league administration, facility scheduling, financial transactions, and merchandise sales, many interconnected elements require seamless integration.

Coordinating member profiles, team assignments, league participation, facility bookings, financial transactions, and merchandise inventory demands meticulous attention to detail and effective communication among staff, coaches, players, and parents.

To tackle this challenge, we require a relational database system that can streamline these processes, providing real-time visibility into club operations and facilitating smooth coordination across all facets of our organization. This solution will enable us to enhance member experiences, optimize resource utilization, and uphold Community FC's commitment to excellence in our local soccer community.

### Data Model 
![Soccer](https://github.com/isabellekiser/Soccer-Team/assets/149964200/9b751434-b5e1-4c10-9ae3-a451cf59c727)

*Explanation*

### Data Dictionary
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

### Queries
# ![query 1](https://github.com/isabellekiser/Soccer-Team/assets/149964200/67b69ad1-f6ca-4a44-be75-6a3197a18cad)
Query 1 selects team names from the "Team" table where the number of players exceeds 10. This query offers insights into team dynamics, resource allocation, and strategic planning. Teams with over 10 players may require additional resources like coaching staff, facilities, and equipment. It is helpful for aspects such as registering for tournaments, where team size often affects eligibility and competitiveness.

Query 2

Query 3

Query 4

# ![query 5](https://github.com/isabellekiser/Soccer-Team/assets/149964200/10fa89bf-6952-4dda-aa0e-ae31ba6b6e0f)
Query 5 retrieves the memberId, last name, and total transaction amount for each member whose transactions exceed $400. It accomplishes this by joining the "Member" table with the "Transaction" table on member IDs, summing up transaction amounts for each member, and filtering for those whose total exceeds $400. This information is crucial for soccer team management as it allows them to identify high-value members who significantly contribute to the club financially. Understanding the financial contributions of individual members enables tailored communication, acknowledgment, and benefits, fostering stronger relationships and loyalty. It also aids in revenue forecasting, budget allocation, and resource planning, ultimately contributing to the financial stability and growth of the club


# ![query 6](https://github.com/isabellekiser/Soccer-Team/assets/149964200/8902c08c-e079-468c-820f-9decf29e7185)
Query 6 retrieves the genders of members whose memberships are set to end in 2024 by joining the "Membership" table with the "Member" table on their respective IDs and filtering for memberships ending in that year. This information is crucial for soccer team management as it allows them to understand the demographic composition of expiring memberships, which in turn informs targeted retention strategies, marketing efforts, and resource allocation. By knowing the genders of members whose memberships are ending, the management can tailor communication, programming, and facilities to better cater to the diverse preferences of their membership base, ultimately fostering greater engagement and ensuring the club's long-term success.

# 
Query 7

# 
Query 8

# 
Query 9

# 
Query 10

### Database information:
Name of the database: Sp24_47114_Group 1
