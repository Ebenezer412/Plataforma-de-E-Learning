📚 Plataforma E-Learning (Protótipo Funcional)

Este é um protótipo de uma mini plataforma de e-learning construído em um único arquivo HTML, utilizando tecnologias web modernas para simular funcionalidades de uma aplicação completa, como persistência de dados e autenticação.

✨ Funcionalidades

Design Moderno e Responsivo: Interface limpa e agradável, estilizada usando Tailwind CSS.

Lista de Cursos: Exibe uma lista de cursos disponíveis com informações resumidas e imagens placeholders.

Página de Detalhes: Ao clicar em um curso, o usuário é levado a uma tela detalhada com a descrição e a lista de lições.

Controle de Progresso Persistente: O status de conclusão de cada curso é salvo no Google Firestore, garantindo que o progresso seja mantido entre sessões.

Autenticação Funcional: Utiliza o Firebase Authentication para gerenciar sessões anônimas/personalizadas, garantindo que o progresso seja exclusivo para o ID do usuário logado (UID).

Feedback de Conclusão: Exibe um badge "CONCLUÍDO" tanto na lista quanto na página de detalhes após o curso ser marcado como finalizado.

🛠️ Tecnologias Utilizadas

HTML5: Estrutura base do documento.

JavaScript (ES6+): Lógica de estado e manipulação do DOM.

Tailwind CSS: Framework de CSS utilitário para estilização rápida e responsiva.

Firebase/Firestore: Utilizado para persistência de dados (status de conclusão) e autenticação.

🚀 Como Funciona o Protótipo

O projeto opera em um modelo de página única (SPA simplificado) e utiliza um estado global de cursos (window.cursos).

Inicialização: Ao carregar, o JavaScript inicializa o Firebase.

Autenticação: O usuário é autenticado automaticamente (anônima ou via token). O UID é então exibido no cabeçalho.

Sincronização de Dados: Um listener do Firestore (através de onSnapshot) é configurado para buscar e atualizar o status de conclusão dos cursos específicos daquele userId.

Marcação de Conclusão: Quando o botão "Marcar como Concluído" é clicado, um novo documento é criado no Firestore para registrar o curso como finalizado. O listener então atualiza a UI em tempo real.