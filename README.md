**Table: Users (Utilisateurs)**
| Column Name (Nom de la colonne) | Data Type (Type de données) | Description (Description) |
|---------------------------------|-----------------------------|---------------------------|
| id (ID de l'utilisateur)        | Primary Key (Clé primaire) | Identifiant unique pour chaque utilisateur. |
| email (Email)                   | String (Chaîne de caractères) | Le nom d'utilisateur choisi par l'utilisateur. |
| password (Mot de passe)         | String (Chaîne de caractères) | Le mot de passe hashé et salé pour l'authentification de l'utilisateur. |

**Table: Categories (Catégories)**
| Column Name (Nom de la colonne) | Data Type (Type de données) | Description (Description) |
|---------------------------------|-----------------------------|---------------------------|
| id (ID de la catégorie)          | Primary Key (Clé primaire) | Identifiant unique pour chaque catégorie. |
| user_id (ID de l'utilisateur)    | Foreign Key (Clé étrangère) | Référence l'utilisateur propriétaire de cette catégorie. |
| category_name (Nom de la catégorie) | String (Chaîne de caractères) | Le nom ou l'étiquette de la catégorie (par exemple, "Épicerie", "Services publics"). |
| description (Description)        | String (Chaîne de caractères) | Une brève description de la catégorie. |

**Table: Budgets (Budgets)**
| Column Name (Nom de la colonne) | Data Type (Type de données) | Description (Description) |
|---------------------------------|-----------------------------|---------------------------|
| id (ID du budget)        | Primary Key (Clé primaire) | Identifiant unique pour chaque budget. |
| user_id (ID de l'utilisateur)    | Foreign Key (Clé étrangère) | Référence l'utilisateur qui a créé ce budget. |
| category_id (ID de la catégorie) | Foreign Key (Clé étrangère) | Référence la catégorie à laquelle appartient ce budget. |
| budget_name (Nom du budget)     | String (Chaîne de caractères) | Un nom ou une étiquette pour le budget (par exemple, "Budget mensuel d'épicerie"). |
| amount (Montant)                | Decimal (Décimal)           | Le montant total prévu pour ce budget. |
| start_date (Date de début)      | Date (Date)                 | La date de début de la période budgétaire. |
| end_date (Date de fin)          | Date (Date)                 | La date de fin de la période budgétaire. |

**Table: Expenses (Dépenses)**
| Column Name (Nom de la colonne) | Data Type (Type de données) | Description (Description) |
|---------------------------------|-----------------------------|---------------------------|
| id (ID de la dépense)   | Primary Key (Clé primaire) | Identifiant unique pour chaque dépense. |
| user_id (ID de l'utilisateur)    | Foreign Key (Clé étrangère) | Référence l'utilisateur qui a enregistré la dépense. |
| category_id (ID de la catégorie) | Foreign Key (Clé étrangère) | Référence la catégorie à laquelle appartient cette dépense. |
| expense_name (Nom de la dépense) | String (Chaîne de caractères) | Un nom ou une description de la dépense (par exemple, "Dîner au restaurant"). |
| amount (Montant)                | Decimal (Décimal)           | Le montant dépensé pour la dépense. |
| expense_date (Date de la dépense) | Date (Date)               | La date à laquelle la dépense a été effectuée. |
| description (Description)       | String (Chaîne de caractères) | Détails ou notes supplémentaires sur la dépense. |
