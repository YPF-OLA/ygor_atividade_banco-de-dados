```sql
CREATE DATABASE tecinternet_escola_ygor CHARACTER SET utf8mb4;

CREATE TABLE cursos(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    titulo VARCHAR(250) NOT NULL,
    cargaHoraria INT NOT NULL,
    professor_id INT
)

CREATE TABLE professores(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(200) NOT NULL,
    area_de_atuacao ENUM('design', 'desenvolvimento', 'infra')
    curso_id INT
)

CREATE TABLE alunos(
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(200) NOT NULL,
    data_de_nascimento DATE NOT NULL,
    primeira_nota DECIMAL(6,2) NOT NULL,
    segunda_nota DECIMAL(6,2) NOT NULL,
    curso_id INT
);
```

```sql
INSERT INTO cursos(titulo, cargaHoraria, professor_id)
VALUES(
   'Front-End',
   2400
), 
(
   'Back-End',
   4800
),
(
    'UX/UI Design',
    1800
),
(
    'Figma',
    600
),
(
    'Redes de Computadores',
    6000
),

```

```sql
INSERT INTO professores(nome, area_de_atuacao, curso_id)
VALUES(
   'Pedro',
   'Infra',
   5
),
(
    'João',
    'Design',
    4
),
(
    'Marcelo',
    'Design',
    3
),
(
    'Julio',
    'Desenvolvimento',
    2
),
(
    'Bruno',
    'Desenvolvimento',
    1
);
```

