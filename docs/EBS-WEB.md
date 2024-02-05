# EBS-WEB
## OAuth de Acesso a Serviços Integrados

### Resumo

O <strong>EBS-WEB</strong> é um <strong>OAuth</strong> onde todas as pessoas que acessam os serviços EBS são registradas criando uma conta para acessá-los. Ele controla o acesso para as aplicações e serviços de forma contínua e totalmente segura. Todos os dados são tratados com uma mesclagem dos melhores algoritmos de assinatura digital, sendo com que ninguém que tenha acesso ao SGBD veja informações sigilosas dos usuários do sistema, entre elas a senha.

### Funcionalidades

No momento o <strong>EBS-WEB</strong> realiza as seguintes funções
- [Login](https://web.ebs-systems.epizy.com/login/)
- [Cadastro](https://web.ebs-systems.epizy.com/singup/)
- [Solicitação e controle de serviço](https://web.ebs-systems.epizy.com/services/)
- [Acesso às aplicações](https://web.ebs-systems.epizy.com/applications/)
- [Edição de dados da conta](https://web.ebs-systems.epizy.com/config)

Esta aplicação agora delimita níveis de acesso para o sistema. Os níveis de acesso são separados por <strong>badges</strong>.

### As principais badges são:

- <code>EBS-DEV</code>: Exclusiva para os devs que fazem parte da equipe de desenvolvimento do EBS-WEB. Essa badge trás privilégios de visualização dos [dashboards](https://web.ebs-systems.epizy.com/dashboards/) da EBS.
- <code>EBS-CLIENT</code>: Destinada aos usuários que solicitam serviços à EBS-Systems. Essa badge trás privilégios de edição de senha <code>root</code> dos serviços.
- <code>EBS-PRO</code>: Esta badge especial é destinada aos assinantes de planos EBS para usurfruir de aplicações dedicadas em lugar das gerais.

### Ultima edição por [ThiagoSousa81](https://github.com/ThiagoSousa81/) em 05/02/2024

[VOLTAR](https://github.com/EBS-Security-Systems/EBS-Docs#readme)
