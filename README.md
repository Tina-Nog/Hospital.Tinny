# 🏥Hospital - Saúde Tech
Transformando a gestão hospitalar com tecnologia e eficiência!
Este projeto tem como objetivo criar um sistema hospitalar moderno e dinâmico, utilizando o MongoDB como banco de dados. Com funcionalidades que abrangem desde o cadastro de médicos até o acompanhamento de internações, buscamos facilitar o dia a dia das equipes hospitalares e melhorar a experiência dos pacientes.

# 🎯 Status do Projeto: Em construção 🚧
Estamos apenas começando, mas grandes novidades estão a caminho!

# 📊 Funcionalidades

- **Parte 1**🧑🏿‍⚕️ :Gestão Clínica
Cadastro completo de médicos com suas especialidades:
Pediatria, clínica geral, gastroenterologia e dermatologia.
Médicos podem ser generalistas, especialistas ou residentes.
```

db["medicos"].insertMany([{
    
    "_id": ObjectId("64a1b14e0c5a8b001f2e4f10"),
    nome:"Dra. Carla Ferreira",
    especialidades: ["Pediatria"],
    tipo: "Especialista",
    contato:{ email: "ferreiracarla09@email.com", telefone: "135678903"},
    documentos: { CPF:"678.456.122-09", RG: " BR123456"}
},
{
    "_id": ObjectId("64a1b14e0c5a8b001f2e4f11"),
    nome: "Dr. Marcos Santos",
    especialidades: ["Clínico Geral"],
    tipo: "Residente",
    contato: { email: "santosmar84@email.com", telefone: " 456789309"},
    documentos: { CPF: " 345.789.811-01", RG: "BR123459"}
},
{
     "_id": ObjectId("64a1b14e0c5a8b001f2e4f12"),
     nome: " Dra. Anna Beatriz",
     especialidades: ["Ginecologista"],
     tipo: " Especialista",
     contato: { email: " trizanna04@email.com", telefone: "567890763"},
     documentos: { CPF: "672.789.333-12", RG: "BR124564"}
},
{
    "_id": ObjectId("64a1b14e0c5a8b001f2e4f13"),
    nome: "Dr. João Mantovani ",
    especialidades: ["Gastroenterologia"],
    tipo: " Residente",
    contato: { email:"mantovani89@email.com", telefone: " 456789564"},
    documentos: { CPF: " 678.234.890-88", RG: "BR123456"}
},
{
     "_id": ObjectId("64a1b14e0c5a8b001f2e4f14"),
     nome: "Dr. Gabriel Augusto",
     especialidades: ["Cardiologista"],
     tipo: " Especialista",
     contato:{email: " gabrielaug90@email.com", telefone: " 456789098"},
     documentos: { CPF: "213.456.789-95", RG: "BR345678"}
},
{
    "_id": ObjectId("64a1b14e0c5a8b001f2e4f15"),
    nome: "Dra. Aurora Sales",
    especialidades: ["Cardiologia"],
    tipo:" Especialista",
    contato: { email:"aurora@salesemail.com", telefone:"123789543"},
    documentos: { CPF: "456.786.222-04", RG:"BR567890"}
},
{
     "_id": ObjectId("64a1b14e0c5a8b001f2e4f16"),
     nome: "Dr. Júlio Cesar",
     especialidades: ["Clínico Geral"],
     tipo:"Generalista",
     contato:{email: "cesar78julio@email.com", telefone: " 456789065"},
     documentos:{ CPF: " 567.890.555-03", RG: "BR555666"}
},
{
     "_id": ObjectId("64a1b14e0c5a8b001f2e4f17"),
     nome: "Dra. Marina Mantovani",
     especialidades:["Ortopedia"],
     tipo:"Especialista",
     contato: {email:"marmantovini@email.com", telefone:"123487790"},
     documentos:{CPF:"345.675.899-05",RG:"BR678543"}
},
{
    "_id": ObjectId("64a1b14e0c5a8b001f2e4f18"),
    nome:"Dra. Fabiana de Paula",
    especialidades:["dermatologia"],
    tipo:"residente",
    contato:{CPF: "245.890.765-64",RG:"BR 2346678" }
}]);

```

- **Pacientes** 🤒 : 15 registro de dados pessoais, documentos e convênios.
  
```
db["pacientes"].insertMany([
  {
    nome: "João Pedro Almeida",
    data_nascimento: new Date("1992-03-25"),
    endereco: {
      rua: "Rua das Palmeiras",
      numero: 123,
      bairro: "Centro",
      cidade: "Rio de Janeiro",
      estado: "RJ",
      cep: "20031-000"
    },
    telefone: "981234567",
    email: "joao.pedro@email.com",
    documentos: { CPF: "112.223.334-45", RG: "RJ123456" },
    convenio: { nome: "Intermédica", cnpj: "11.223.334/0001-99", tempo_carencia: 45 }
  },
  {
    nome: "Carolina Vasconcelos",
    data_nascimento: new Date("1987-12-12"),
    endereco: {
      rua: "Avenida Atlântica",
      numero: 450,
      bairro: "Copacabana",
      cidade: "Rio de Janeiro",
      estado: "RJ",
      cep: "22021-001"
    },
    telefone: "982345678",
    email: "carolina.vasconcelos@email.com",
    documentos: { CPF: "223.334.445-56", RG: "RJ223344" },
    convenio: { nome: "Hapvida", cnpj: "22.334.445/0001-88", tempo_carencia: 30 }
  },
  {
    nome: "Fernando Oliveira Santos",
    data_nascimento: new Date("1975-07-15"),
    endereco: {
      rua: "Rua das Rosas",
      numero: 300,
      bairro: "Jardim América",
      cidade: "Belo Horizonte",
      estado: "MG",
      cep: "30110-123"
    },
    telefone: "983456789",
    email: "fernando.santos@email.com",
    documentos: { CPF: "334.445.556-67", RG: "MG334455" },
    convenio: { nome: "Mediplan", cnpj: "33.445.556/0001-77", tempo_carencia: 60 }
  },
  {
    nome: "Beatriz Ramos Lima",
    data_nascimento: new Date("1998-06-05"),
    endereco: {
      rua: "Rua dos Girassóis",
      numero: 50,
      bairro: "Boa Vista",
      cidade: "Curitiba",
      estado: "PR",
      cep: "80540-010"
    },
    telefone: "984567890",
    email: "beatriz.lima@email.com",
    documentos: { CPF: "445.556.667-78", RG: "PR445566" },
    convenio: { nome: "CarePlus", cnpj: "44.556.667/0001-66", tempo_carencia: 90 }
  },
  {
    nome: "Lucas Henrique Rocha",
    data_nascimento: new Date("1985-02-14"),
    endereco: {
      rua: "Avenida das Nações",
      numero: 789,
      bairro: "Asa Norte",
      cidade: "Brasília",
      estado: "DF",
      cep: "70040-000"
    },
    telefone: "985678901",
    email: "lucas.rocha@email.com",
    documentos: { CPF: "556.667.778-89", RG: "DF556677" },
    convenio: { nome: "BioVida", cnpj: "55.667.778/0001-55", tempo_carencia: 120 }
  },
  {
    nome: "Mariana Ferreira Costa",
    data_nascimento: new Date("1990-09-09"),
    endereco: {
      rua: "Rua dos Jacarandás",
      numero: 234,
      bairro: "Setor Bueno",
      cidade: "Goiânia",
      estado: "GO",
      cep: "74230-010"
    },
    telefone: "986789012",
    email: "mariana.costa@email.com",
    documentos: { CPF: "667.778.889-90", RG: "GO667778" },
    convenio: { nome: "OneHealth", cnpj: "66.778.889/0001-44", tempo_carencia: 75 }
  },
  {
    nome: "Rafael Moura Alves",
    data_nascimento: new Date("1972-11-20"),
    endereco: {
      rua: "Rua das Acácias",
      numero: 98,
      bairro: "Lagoa Nova",
      cidade: "Natal",
      estado: "RN",
      cep: "59075-000"
    },
    telefone: "987890123",
    email: "rafael.alves@email.com",
    documentos: { CPF: "778.889.990-01", RG: "RN778889" },
    convenio: { nome: "Promed", cnpj: "77.889.990/0001-33", tempo_carencia: 45 }
  },
  {
    nome: "Cláudia Regina Araújo",
    data_nascimento: new Date("1988-04-02"),
    endereco: {
      rua: "Avenida Rui Barbosa",
      numero: 120,
      bairro: "Centro",
      cidade: "Recife",
      estado: "PE",
      cep: "50050-000"
    },
    telefone: "988901234",
    email: "claudia.araujo@email.com",
    documentos: { CPF: "889.990.101-12", RG: "PE889990" },
    convenio: { nome: "NotreDame", cnpj: "88.990.101/0001-22", tempo_carencia: 60 }
  },
  {
    nome: "Renata Pereira Barbosa",
    data_nascimento: new Date("1994-05-11"),
    endereco: {
      rua: "Rua das Orquídeas",
      numero: 67,
      bairro: "Alto da Glória",
      cidade: "Curitiba",
      estado: "PR",
      cep: "80040-000"
    },
    telefone: "989012345",
    email: "renata.barbosa@email.com",
    documentos: { CPF: "990.101.212-23", RG: "PR990101" },
    convenio: { nome: "Porto Seguro Saúde", cnpj: "99.101.212/0001-11", tempo_carencia: 30 }
  },
  {
    nome: "Pedro Lucas Carvalho",
    data_nascimento: new Date("1996-10-08"),
    endereco: {
      rua: "Avenida Central",
      numero: 45,
      bairro: "Centro",
      cidade: "Florianópolis",
      estado: "SC",
      cep: "88015-000"
    },
    telefone: "990123456",
    email: "pedro.carvalho@email.com",
    documentos: { CPF: "101.212.323-34", RG: "SC101212" },
    convenio: { nome: "Allianz Saúde", cnpj: "10.212.323/0001-66", tempo_carencia: 90 }
  }
]);
```
  
- **Consultas**: controle de agendamentos com data, hora, médico responsável e especialidade.
Emissão de receitas médicas com medicamentos, dosagem e instruções detalhadas para os pacientes.
Visualização ou impressão de receitas para maior praticidade.
- **Parte 2** 🩺 : Controle de Internações
- **Internações** :
Registro de entrada, previsão de alta, alta efetiva e descrição de procedimentos.
Quartos: tipos (apartamento, duplo ou enfermaria) com descrição e valor diário.
Cadastro de profissionais de enfermagem, incluindo nome, CPF.
Relacionamento das internações com médicos responsáveis e pacientes.

## 🌟Categorias de Quartos 🛏️
- **Apartamento**: Privacidade total com conforto premium.
- **Duplo**: Quartos compartilhados com ótimo custo-benefício.
- **Enfermaria**: Uma solução coletiva para internações rápidas e eficientes.
 
```
db["quarto"].insertMany([
  { numero: 101, tipo: "Apartamento", valor_diario: 500 },
  { numero: 102, tipo: "Quarto Duplo", valor_diario: 300 },
  { numero: 103, tipo: "Enfermaria", valor_diario: 200 },
  { numero: 104, tipo: "Apartamento", valor_diario: 550 },
  { numero: 105, tipo: "Quarto Duplo", valor_diario: 320 },
  { numero: 106, tipo: "Enfermaria", valor_diario: 220 },
  { numero: 107, tipo: "Apartamento", valor_diario: 600 },
  { numero: 108, tipo: "Quarto Duplo", valor_diario: 350 },
  { numero: 109, tipo: "Enfermaria", valor_diario: 250 },
  { numero: 110, tipo: "Apartamento", valor_diario: 580 }
]);
```

# 🛠️ Etapas de Desenvolvimento
- **🔍 Parte 1**: Mãos à Obra
 Construção do diagrama de banco de dados.
 Implementação de cadastros para médicos, pacientes e convênios.
 Sistema para registro de consultas e emissão de receitas.
- **🔍 Parte 2**: Internações
 Desenvolvimento do módulo de internações.
 Cadastro e controle de quartos e profissionais de enfermagem.
 Relatórios detalhados para alta hospitalar.

# 📌 Observações
Este repositório está em constante evolução. 💡

Próximos Passos: O desenvolvimento do diagrama
