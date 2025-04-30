User
- id PK UUID
- name
- email UNIQUE
- password_hash
- role ENUM ('admin', 'user')
- created_at
- updated_at

Project
- id PK UUID
- title
- description
- created_by FK -> User.id
- created_at
- updated_at

Task
- id PK UUID
- title
- description
- status ENUM('todo', 'in_progress', 'done')
- project_id FK -> Project.id
- assigned_to FK -> User.id
- created_at
- updated_at

Comment
- id PK UUID
- content
- task_id FK -> Task.id
- user_id FK -> User.id
- created_at
