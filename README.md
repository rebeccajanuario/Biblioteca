# 🎫 ConectMAM 🎫
![Brimston](https://github.com/rebeccajanuario/Biblioteca/assets/129446615/3187f19a-6598-4688-84d2-ae7aa7af4729)

# 👥 Participantes
Brenda Marques CP3020665

Rebecca Januario CP3020622

# 🎨 Software para controlar a venda de ingressos do MAM(Museu de Arte Moderna de São Paulo) e a reserva de sua biblioteca🎨
O MAM enfrenta desafios na gestão da venda de ingressos e da reserva de livros da biblioteca, que atualmente são processos manuais e propensos a erros. Isso resulta em filas, indisponibilidade de materiais e dificuldade na obtenção de dados precisos para análises estratégicas. O software proposto integrará em um único sistema a venda de ingressos online, a reserva de livros e a gestão de dados, oferecendo aos visitantes uma plataforma intuitiva e eficiente para interagir com o museu.


# 🔖 C4Model
# 🔸Diagrama de Contexto

![contexto](https://github.com/rebeccajanuario/Biblioteca/assets/65727310/1fc797aa-c85a-4832-b1e4-9529df248000)

Este diagrama de contexto fornece uma visão geral simplificada do sistema de Venda de Ingressos e Reserva da Biblioteca do Museu de Arte Moderna de São Paulo (MAM). Ele identifica as principais entidades externas e como elas interagem com o sistema principal.

Principais Entidades Externas:

    Visitante: Usuário que solicita reservas de ingressos e livros.
    Bibliotecário: Responsável por gerenciar as reservas de ingressos e eventos.
    Administrador do Sistema: Monitora as métricas de desempenho do sistema.

Sistema Principal:

    Sistema de Venda de Ingressos e Reserva da Biblioteca - MAM: Sistema que gerencia reservas de ingressos e livros para o Museu de Arte Moderna de São Paulo.

Principais Interações:

    O visitante solicita reservas de ingressos e livros através do sistema.
    O bibliotecário gerencia reservas de ingressos e eventos através do sistema.
    O administrador do sistema monitora métricas de desempenho do sistema.
# 🔸Diagrama de Container

![fPNDRXit4CVlUWfsqOC4MDgYpIb0WTYEqJYLOsLNJdiJPfSZYGcNt93SJTMY3zDJaNFH9z2BbKD9D655heiQXiqFyZSVy-Vi2-l0kAwHWw-4gcN7aQsTQ-tpF3VmQR8IRjrLdKLJQ-LGkKcjcxoLeEZEs3ekHPLVFXlFQEdkPfetO1qQlxIuz3T0A3IJDl0vBlsCNL_UlhahfaymuxeMkFdktfpmk-EbFp6shH4ERTv_Etas-IRwtXbvuE](https://github.com/rebeccajanuario/Biblioteca/assets/65727310/a3af71fc-7e75-4d89-a839-8bedfb72907b)

Diagrama de Contexto:
Fornece uma visão geral do sistema "MAM", mostrando como ele interage com os visitantes, bibliotecários e administradores do sistema.

Diagrama de Containers:
Detalha os principais contêineres do sistema e suas interações. Mostra os serviços de backend e frontend, o processador de reservas, banco de dados, e os sistemas de monitoramento de métricas (Power BI e Data Studio).

Neste diagrama, o backend e o processador de reservas são implementados em JavaScript. O frontend é desenvolvido em React. As métricas do sistema são gerenciadas pelo Power BI e exibidas pelo Data Studio. O banco de dados MySQL armazena detalhes das reservas. As interações assíncronas são gerenciadas pelo Kafka.



# 🔸Diagrama de Componentes
O diagrama de componentes detalha os componentes dentro dos principais contêineres do sistema. No sistema "MAM", ele mostra os controladores, serviços e outros componentes do backend, bem como suas interações internas.

![componente](https://github.com/rebeccajanuario/ConectMAM/assets/65727310/089ec350-51ee-49cc-b357-4e2084ab6da6)


Descrição dos Componentes:

Backend:

    Controlador de Ingressos: Controla as solicitações de reservas de ingressos.
    Controlador de Livros: Controla as solicitações de reservas de livros.
    Controlador de Eventos: Gerencia os eventos.
    Serviço de Autenticação: Responsável pela autenticação e autorização dos usuários.
    Serviço de Reservas: Processa as reservas de ingressos e livros.
    Serviço de Banco de Dados: Interage com o banco de dados MySQL para armazenar informações de reservas.

Processador de Reservas:

    Processador de Reservas: Confirma ou rejeita reservas de ingressos e livros, comunicando os resultados e armazenando os detalhes das reservas no banco de dados MySQL.


# 🔸Diagrama de Código

![codigo](https://github.com/rebeccajanuario/ConectMAM/assets/65727310/1ce34b79-fd8f-45d3-8fb3-e7df28093ccb)




Este diagrama de código representa a estrutura de classes do backend e do processador de reservas do Sistema de Venda de Ingressos e Reserva da Biblioteca - MAM.

Interações:

    O IngressoController e o LivroController usam o ServicoReserva para processar reservas.
    O EventoController usa o ServicoAutenticacao para autenticação e autorização.
    O ServicoReserva usa o ServicoBancoDeDados para salvar, obter e deletar reservas.
    O ProcessadorReserva comunica os resultados das reservas ao ServicoReserva e usa o ServicoBancoDeDados.
    
# 🔸Diagrama de Classes com Factory
O uso do padrão Factory desacopla a criação de controladores do código que os usa, facilitando a manutenção e a escalabilidade do sistema.
![image](https://github.com/rebeccajanuario/ConectMAM/assets/129446615/1de4d184-a550-49da-81b2-415e3e205949)




# 🔸Diagrama de Classes com Strategy
O uso do padrão Strategy permite que a lógica de reserva de ingressos e livros seja encapsulada em classes distintas, facilitando a manutenção e a extensão do sistema.
![image](https://github.com/rebeccajanuario/ConectMAM/assets/129446615/9c9f41fa-c5cf-4c84-853c-6ea4006ee4ff)


# 🎟 Padrão Arquitetural MVC
![image](https://github.com/rebeccajanuario/ConectMAM/assets/129446615/bfdb2f98-ca50-4130-9d7e-49643cb6af3d)

Fluxo de Interação:

*O Usuário interage com a Visão, realizando ações como: preencher formulários ou clicar em botões.

*A Visão captura essas ações e, quando necessário, faz atualizações no Modelo (por exemplo, quando um formulário é submetido).

*A Visão também pode acessar dados do Modelo para exibir informações ao usuário (por exemplo, mostrar a disponibilidade de ingressos ou livros).

*O Controlador recebe as ações do Usuário através da Visão e executa a lógica necessária para manipular o Modelo (por exemplo, validar uma reserva ou processar um pagamento).

*Qualquer mudança no Modelo pode ser refletida de volta na Visão para manter o usuário atualizado com as últimas informações.







