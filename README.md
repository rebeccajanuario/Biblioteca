# ConectMAM
![Brimston](https://github.com/rebeccajanuario/Biblioteca/assets/129446615/3187f19a-6598-4688-84d2-ae7aa7af4729)

# Software para controlar a venda de ingressos do MAM(Museu de Arte Moderna de São Paulo) e a reserva de sua biblioteca.
O MAM enfrenta desafios na gestão da venda de ingressos e da reserva de livros da biblioteca, que atualmente são processos manuais e propensos a erros. Isso resulta em filas, indisponibilidade de materiais e dificuldade na obtenção de dados precisos para análises estratégicas. O software proposto integrará em um único sistema a venda de ingressos online, a reserva de livros e a gestão de dados, oferecendo aos visitantes uma plataforma intuitiva e eficiente para interagir com o museu.


# C4Model
# Diagrama de Contexto

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
# Diagrama de Container

![fPNDRXit4CVlUWfsqOC4MDgYpIb0WTYEqJYLOsLNJdiJPfSZYGcNt93SJTMY3zDJaNFH9z2BbKD9D655heiQXiqFyZSVy-Vi2-l0kAwHWw-4gcN7aQsTQ-tpF3VmQR8IRjrLdKLJQ-LGkKcjcxoLeEZEs3ekHPLVFXlFQEdkPfetO1qQlxIuz3T0A3IJDl0vBlsCNL_UlhahfaymuxeMkFdktfpmk-EbFp6shH4ERTv_Etas-IRwtXbvuE](https://github.com/rebeccajanuario/Biblioteca/assets/65727310/a3af71fc-7e75-4d89-a839-8bedfb72907b)

Diagrama de Contexto:
Fornece uma visão geral do sistema "MAM", mostrando como ele interage com os visitantes, bibliotecários e administradores do sistema.

Diagrama de Containers:
Detalha os principais contêineres do sistema e suas interações. Mostra os serviços de backend e frontend, o processador de reservas, banco de dados, e os sistemas de monitoramento de métricas (Power BI e Data Studio).

Neste diagrama, o backend e o processador de reservas são implementados em JavaScript. O frontend é desenvolvido em React. As métricas do sistema são gerenciadas pelo Power BI e exibidas pelo Data Studio. O banco de dados MySQL armazena detalhes das reservas. As interações assíncronas são gerenciadas pelo Kafka.



# Diagrama de Componentes
O diagrama de componentes detalha os componentes dentro dos principais contêineres do sistema. No sistema "MAM", ele mostra os controladores, serviços e outros componentes do backend, bem como suas interações internas.

![fLJ1JXiz4Bxp5FwZ_m0IoLOj9wHAG5fLLA6bH9oZMNkI6BoUPUnD1LMVfWUUe4_0YzNEPjDbPHRQvX3Pwvdl-sRciu-S1_PLONR-qrQQIg5OUb-wmonZ-3fQQB-iyieXIx8UhHz9AhBIW8qvG-ULqNasFXYUnq-NPvEi0EUHmwVPc8gIRCmfr_WAvzgYE1r__dHvCNa1ZQzAKFpcDvqEfyDvY1YwahL7bwrUZmv6hxRQApODVgPm5UDTnW](https://github.com/rebeccajanuario/Biblioteca/assets/65727310/75c98f5a-0b25-461b-8c26-8accefd655b2)

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


# Diagrama de Código

![XPD1RzGm48Nl-HLkJwrG4WISUa2bBOUY2b0hpcZMdjswE7OqCmuIgF-TXFN2QEjsVLhvlVdUvja-Pm6IF8JcoE7QHpJNbry-VxkzCVSY8v_rFS7FRkFbFgyo8zaK1QDqDWszv14SlUt70751j7vMs_NiQ7aaByZzzAPxrxrkZdoq8JlC57Rytk6q-Bb_W0dOaX_b-mhS1hjn-JlD2FO7RD0SNym_C3fpycastlqrdXwRtusPbmt0RAxZXf](https://github.com/rebeccajanuario/Biblioteca/assets/65727310/96698338-6d8e-4761-a557-647aaee378af)



Este diagrama de código representa a estrutura de classes do backend e do processador de reservas do Sistema de Venda de Ingressos e Reserva da Biblioteca - MAM.

Interações:

    O IngressoController e o LivroController usam o ServicoReserva para processar reservas.
    O EventoController usa o ServicoAutenticacao para autenticação e autorização.
    O ServicoReserva usa o ServicoBancoDeDados para salvar, obter e deletar reservas.
    O ProcessadorReserva comunica os resultados das reservas ao ServicoReserva e usa o ServicoBancoDeDados.
    
# Diagrama de Classes com Factory
O uso do padrão Factory desacopla a criação de controladores do código que os usa, facilitando a manutenção e a escalabilidade do sistema.
![0](https://github.com/rebeccajanuario/Biblioteca/assets/129446615/7406447f-9c94-482a-840e-4d1c48a31492)

Fluxo de Criação de Controladores:

   O ConcreteControllerFactory implementa a interface IControllerFactory, fornecendo métodos para criar controladores específicos (IngressoController, LivroController, EventoController).

   Os controladores criados (IngressoController e LivroController) usam o ServicoReserva para processar as reservas.

   O EventoController usa o ServicoAutenticacao para autenticar e autorizar ações de gerenciamento de eventos.

# Diagrama de Classes com Strategy
O uso do padrão Strategy permite que a lógica de reserva de ingressos e livros seja encapsulada em classes distintas, facilitando a manutenção e a extensão do sistema.
![0](https://github.com/rebeccajanuario/Biblioteca/assets/129446615/fd828c75-c898-4d4f-b2dc-9fab08ac1ce9)

Fluxo de Criação de Controladores:

   IngressController e LivroController são configurados com uma instância da estratégia apropriada (ReservaIngressoStrategy ou ReservaLivroStrategy).

   IReservaStrategy define a interface para as estratégias de reserva, garantindo que todas as estratégias implementem os métodos +processarReserva() e +cancelarReserva().

   ReservaIngressoStrategy e ReservaLivroStrategy encapsulam a lógica específica de processamento e cancelamento de reservas de ingressos e livros, respectivamente.

   ServicoReserva e ServicoBancoDeDados são usados pelas estratégias para interagir com o sistema de reservas e o banco de dados.

 



