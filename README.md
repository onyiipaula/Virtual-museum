# Virtual-museum
Entity-Relationship Diagram (ERD) for Virtual Museum Tour
Entities:
Exhibit

Attributes: ExhibitID (PK), Name, Description, ImageURL
Visitor

Attributes: VisitorID (PK), Name, Comment
Relationships:
Visitor-Comment-Exhibit
Relationship Type: One Visitor can comment on Many Exhibits
Attributes: CommentID (PK), VisitorID (FK), ExhibitID (FK), CommentText
Diagram:
scss
Copy code
  +--------------+        +----------------+        +--------------+
  |    Exhibit   |        | Visitor-Comment |        |   Visitor    |
  +--------------+        +----------------+        +--------------+
  | ExhibitID (PK)| 1    M| CommentID (PK)  | M    1| VisitorID (PK)|
  | Name         |--------| VisitorID (FK)  |--------| Name         |
  | Description  |        | ExhibitID (FK)  |        |              |
  | ImageURL     |        | CommentText     |        |              |
  +--------------+        +----------------+        +--------------+
Explanation:
Exhibit Entity: Represents each exhibit in the museum.

Attributes: ExhibitID (Primary Key), Name, Description, ImageURL.
Visitor Entity: Represents visitors who interact with the exhibits.

Attributes: VisitorID (Primary Key), Name.
Visitor-Comment-Exhibit Relationship: Represents the association where a visitor can comment on multiple exhibits.

Attributes: CommentID (Primary Key), VisitorID (Foreign Key referencing Visitor), ExhibitID (Foreign Key referencing Exhibit), CommentText.
