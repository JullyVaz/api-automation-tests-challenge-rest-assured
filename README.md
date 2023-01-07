# api-automation-tests-challenge-rest-assured
Parte obrigatória do desafio

As descrições a seguir são referentes às classes criadas tomando como referência a API Restful-booker:
A classe Java chamada Booking, representa uma reserva em um sistema de reservas de hospedagem. A classe possui diversos atributos, como nome e sobrenome do hóspede, preço total da reserva, informação sobre se o depósito já foi pago, detalhes da data da reserva (classe BookingDates) e informações adicionais. Ela também possui métodos getters e setters para cada atributo, permitindo obter e alterar os valores destes atributos.

A classe BookingDates representa a data de check-in e check-out de uma reserva (ou booking, em inglês). Ela possui dois atributos, checkin e checkout, ambos do tipo String, que armazenam essas informações.
Ela possui um construtor que recebe os valores dessas variáveis como parâmetros e os atribui aos atributos da classe. Além disso, possui métodos getters e setters para esses atributos, permitindo acessar ou modificar os valores das datas de check-in e check-out.

A classe User representa um usuário com os seguintes atributos: username: - nome de usuário do usuário, - firstName: primeiro nome do usuário, - lastName: sobrenome do usuário, - email: email do usuário, - password: senha do usuário e - phone: telefone do usuário.

As descrições a seguir são referentes à classe criada para fazer automação dos testes:
A classe importa três outras classes: Booking, BookingDates e User. Essas classes representam os objetos de reserva, datas de reserva e usuário, respectivamente. A 

A classe também importa a biblioteca Faker para gerar dados aleatórios para preencher esses objetos.
A classe também importa a biblioteca RestAssured, que é usada para fazer solicitações HTTP à API de reserva de hotel. A classe também usa os filtros RequestLoggingFilter, ResponseLoggingFilter e ErrorLoggingFilter da biblioteca RestAssured para registrar solicitações, respostas e erros durante os testes.

A classe possui três métodos de teste: getAllBookingsById_returnOk, getAllBookingsByUserFirstName_BookingExists_returnOk e CreateBooking_WithValidData_returnOk. Cada método de teste envia uma solicitação HTTP à API de reserva de hotel e verifica se a resposta é válida.

O método Setup é executado uma vez antes de todos os testes, e inicializa o objeto faker, cria um novo usuário e uma nova reserva com as informações do usuário e atribui a URL da API de reserva de hotel à propriedade baseURI da classe RestAssured.

O método setRequest é executado antes de cada método de teste e inicializa o objeto request com as configurações padrão para as solicitações HTTP (como o tipo de conteúdo e autenticação básica).

A  API Restful-booker foi utilizada para a criação da coleção Postman de acordo com os critérios especificados e a	geração de relatórios com Allure Framework.
