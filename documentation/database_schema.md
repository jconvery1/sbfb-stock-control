## Database Schema
This schema may change as the project develops, for now this is just a first draft.
### Tables

#### stock_item
| Column Name       | Data Type | Constraints |
|-------------------|-----------|-------------|
| id                | INT       | PRIMARY KEY |
| name              | VARCHAR   | NOT NULL    |
| stock_weight      | DECIMAL   | NOT NULL    |
| cardboard_quantity | INT      | NOT NULL    |
| plastic_quantity  | INT       | NOT NULL    |
| small_ifco_quantity | INT     | NOT NULL    |
| big_ifco_quantity | INT       | NOT NULL    |

#### delivery
| Column Name       | Data Type | Constraints |
|-------------------|-----------|-------------|
| id                | INT       | PRIMARY KEY |
| weight            | DECIMAL   | NOT NULL    |
| team_member_id    | INT       | FOREIGN KEY |
| location_id       | INT       | FOREIGN KEY |
| datetime          | DATETIME  | NOT NULL    |

#### replenishment
| Column Name       | Data Type | Constraints |
|-------------------|-----------|-------------|
| id                | INT       | PRIMARY KEY |
| weight            | DECIMAL   | NOT NULL    |
| cardboard_quantity | INT      | NOT NULL    |
| plastic_quantity  | INT       | NOT NULL    |
| small_ifco_quantity | INT     | NOT NULL    |
| big_ifco_quantity | INT       | NOT NULL    |
| location_id       | INT       | FOREIGN KEY |
| team_member_id    | INT       | FOREIGN KEY |
| datetime          | DATETIME  | NOT NULL    |

#### crate
| Column Name       | Data Type | Constraints |
|-------------------|-----------|-------------|
| id                | INT       | PRIMARY KEY |
| stock_item_id     | INT       | FOREIGN KEY |
| crate_type_id     | INT       | FOREIGN KEY |
| weight            | DECIMAL   | NOT NULL    |

#### crate_type
| Column Name       | Data Type | Constraints |
|-------------------|-----------|-------------|
| id                | INT       | PRIMARY KEY |
| name              | VARCHAR   | NOT NULL    |
| weight            | DECIMAL   | NOT NULL    |

#### location
| Column Name       | Data Type | Constraints |
|-------------------|-----------|-------------|
| id                | INT       | PRIMARY KEY |
| name              | VARCHAR   | NOT NULL    |
| address           | VARCHAR   |             |

#### replen_item
| Column Name       | Data Type | Constraints |
|-------------------|-----------|-------------|
| id                | INT       | PRIMARY KEY |
| crate_id          | INT       | FOREIGN KEY |
| replen_id         | INT       | FOREIGN KEY |

#### team
| Column Name       | Data Type | Constraints |
|-------------------|-----------|-------------|
| id                | INT       | PRIMARY KEY |
| name              | VARCHAR   | NOT NULL    |

#### team_member
| Column Name       | Data Type | Constraints |
|-------------------|-----------|-------------|
| id                | INT       | PRIMARY KEY |
| first_name        | VARCHAR   | NOT NULL    |
| surname           | VARCHAR   | NOT NULL    |
| team_id           | INT       | FOREIGN KEY |
