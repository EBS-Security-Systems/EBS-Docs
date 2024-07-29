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

### Padrões de Encriptação Simétrica

Cada algoritmo de encriptação simétrica tem um tamanho definido de chaves e vetores. Veja a tabela abaixo:

| Algoritmo | Quantidade de bits da chave | Tamanho da chave | Tamanho do vetor |
| --- | --- | --- | --- |
| DES | 64 bits | 8 caracteres | 8 caracteres |
| AES | 128, 192 ou 256 bits | 16, 24 ou 32 caracteres | 16 caracteres |
| 3DES | 128 bits |  16 caracteres | 8 caracteres |
| ARC2 | máximo 128 bits | 5 a 16 caracteres | 8 caracteres |
| CAST | 64 ou 128 bits | 8 ou 16 caracteres | 8 caracteres |
| Blowfish | máximo 448 bits | 4 a 56 caracteres | 8 caracteres |
| ChaCha20* | 256 bits | 32 caracteres | 8 caracteres |

> OBS.: O ChaCha20 é uma cifra de fluxo, porém precisa do IV para gerar o _KeyStream_

### Padrões de Encriptação Assimétrica

Diferentemente da criptografia simétrica, que pode receber um número fixo de caracteres para chave e vetor, a assimétrica por si só gera um par de chaves específico, onde uma chamada **pública** é usada para encriptar e outra chamada **privada** é usada para decriptar.
<br>
Ao enviar mensagens encriptadas com esse tipo de procedimento, você e o receptor devem ambos gerarem um par de chaves. Você deve enviar sua chave pública ao receptor e ele lhe enviar a dele. Agora você pode encriptar a mensagem com a chave do receptor e somente ele poderá decriptar com a chave privada.

> A geração de chaves é um processo que consome um alto processamento! Logo resolveremos esse problema.

No momento temos os seguintes algoritmos de encriptação assimétrica

| Algoritmo | Tamanho máximo de chave (bits) |
| --- | --- |
| RSA | 4096* |

### Observações
1. Nem sempre será possível gerar um par de chaves 4096, pois exige um processamento considerável. Garantimos que o mais seguro será o 2048 ou o 3072, porém a cifra aceita outros valores.

2. A criptografia RSA não aceita uma grande quantidade de texto para ser encriptado de uma vez! Algumas sugestões seriam implementar o *Cipher Block Chaning* (CBC) ou criptorafia por bloco desprovido de vetor.

3. O valor de bits aplicado para o tamanho da chave pode ser variável fora dos que são usados normalmente (1024, 2048, 3072, e 4096). 
<br>Ex.: Você pode gerar um par de chaves de 1050 bis, porém é algo fora do padrão

4. O tamanho em bits aplicado ao par de chaves não pode ser menor que 1024 pois é considerado inseguro! Queremos implementá-lo para testes no EBS-LAB (spoilers 😁)

5. Você pode gerar um par de chaves fora do EBS-CSP com até uma quantidade maior de bits. Isso possibilita ao EBS-CSP encriptar mensagens maiores.

### Assinaturas Digitais - Hashs

O **EBS-CSP** permite gerar hashs sobre a padronização de diversos algoritmos com múltiplos variados. Abaixo vê-se uma tabela com os hashs disponíveis.

| Hash       | Comprimento (bits) |
|------------|--------------------|
| MD5        | 128                |
| SHA-1      | 160                |
| SHA-224    | 224                |
| SHA-256    | 256                |
| SHA-384    | 384                |
| SHA-512    | 512                |
| BLAKE2b    | 256                |
| BLAKE2s    | 256                |
| SHA3-224   | 224                |
| SHA3-256   | 256                |
| SHA3-384   | 384                |
| SHA3-512   | 512                |
| SHAKE-128  | Variável (mínimo ideal 128) |
| SHAKE-256  | Variável (mínimo ideal 256) |

> Os algoritmos **SHAKE-128** e **SHAKE-256** permitem uma saída variável por meio de um tamanho inteiro.

> O **EBS-CSP** agora permite também gerar o BASE-64 dos hashs em lugar dos hexadecimais também! Eles geralmente continuam com tamanho fixo, diferentemente das encriptações.


### Ultima edição por [ThiagoSousa81](https://github.com/ThiagoSousa81/) em 28/07/2024

[VOLTAR](https://github.com/EBS-Security-Systems/EBS-Docs#readme)