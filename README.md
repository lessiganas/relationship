create  Entity relationship model:
* entities:
Gym: GymID (unique identifier), Name, Address, PhoneNumber
Member:
Member: MemberID (unique identifier), LastName, FirstName, Address, DateOfBirth, Gender
Session:
Session: SessionID (unique identifier), SportType, Schedule, MaxCapacity (20)
Coach:
coach: CoachID (unique identifier), LastName, FirstName, Age, Specialty
* relationship :

-  One-to-Many (Gymnasium to Member):

A gymnasium can have many members, but a member belongs to only one gymnasium.
This is represented by the foreign key GymnasiumID in the Member table, referencing the primary key GymnasiumID in the Gymnasium table.


-  One-to-Many (Gymnasium to Session):

A gymnasium can have many sessions, but a session is held at only one gymnasium.
This is represented by the foreign key GymnasiumID in the Session table, referencing the primary key GymnasiumID in the Gymnasium table.
-  Many-to-Many (Member to Session):

A member can attend many sessions, and a session can have multiple members attending.
This is implemented using the junction table Attendance, which has foreign keys to both MemberID and SessionID, forming the many-to-many relationship.
-  Many-to-Many (Coach to Session):

A coach can lead multiple sessions, and a session can be led by multiple coaches.
This is implemented using the junction table Coaching, which has foreign keys to both CoachID and SessionID, forming the many-to-many relationship.
