# EBS-CSP
## Provedor de Serviços de Encriptação

### Resumo
<b>EBS-CSP</b> (conhecido também por <i>Provedor de Serviço de Encriptação</i>) é um sistema que tem por objetivo principal ser um serviço especializado em <b>criptografia</b> e <b>assinatura digital (hashs)</b> no contexto de produção para implementação em novas aplicações.

### Funcionalidades que estão sendo implementadas na versão BETA
- Integração direta com o [EBS-WEB](https://github.com/EBS-Security-Systems/EBS-Docs/blob/main/docs/EBS-WEB.md)
- Criptografia e descriptografia de textos e bytes
- Hasheamento avançado
- Geração de Chaves-Públicas
- Uso de algoritmos de chave pública

### Acesso
É possível utilizá-la pelo link https://csp.ebs-systems.epizy.com/. O formulário gera um link preparado da API com sua conta que pode ser utilizado como uma API-CSP em seu próprio aplicativo.

> Para selecionar um algoritmo de forma mais rápida e fácil, clique no botão autopreenchimento.

### Padrões

Cada algoritmo tem um tamanho definido de chaves e vetores. Veja a tabela abaixo:

| Algoritmo | Quantidade de bits da chave | Tamanho da chave | Tamanho do vetor |
| --- | --- | --- | --- |
| DES | 64 bits | 8 caracteres | 8 caracteres |
| AES | 128, 192 ou 256 bits | 16, 24 ou 32 caracteres | 16 caracteres |
| 3DES | 128 bits |  16 caracteres | 8 caracteres |
| ARC2 | máximo 128 bits | 5 a 16 caracteres | 8 caracteres |
| CAST | 64 ou 128 bits | 8 ou 16 caracteres | 8 caracteres |
| Blowfish | 256 bits | 32 caracteres | 8 caracteres |
| ChaCha20* | 256 bits | 32 caracteres | 8 caracteres |

> OBS.: O ChaCha20 é uma cifra de fluxo, porém precisa do IV para gerar o _KeyStream_


### Ultima edição por [ThiagoSousa81](https://github.com/ThiagoSousa81/) em 11/07/2024

[VOLTAR](https://github.com/EBS-Security-Systems/EBS-Docs#readme)