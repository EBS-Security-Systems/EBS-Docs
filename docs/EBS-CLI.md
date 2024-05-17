# EBS-CLI
## Interface de Linha de Comando
### Resumo
O <strong>EBS-CLI</strong> é um programa de computador que controla processos de criptografia através de linhas de comando. É uma ótima opção para <strong>desenvolvedores</strong> que precisam proteger códigos ou para pessoas que querem ter suas pastas no computador <strong>criptografadas</strong>.

É um programa leve, rápido e eficaz para encriptar e desencriptar de forma confiável.

### Funcionalidades
- Criptografar arquivos e diretórios
- Salvar e executar scripts de encriptação (automação de segurança)
- Criar e importar pares de chaves de encriptação simétricas e assimétricas
- Compartilhamento de <i>scripts</i> na [EBS-IDC](https://github.com/EBS-Security-Systems/EBS-Docs/blob/main/docs/EBS-IDC.md)

### Site oficial: <https://cli.ebs-systems.epizy.com/>

### Instalação

<details><summary>Clique para visualizar...</summary>

<br>
<a href="https://cli.ebs-systems.epizy.com/" target="_blank"><img src="https://img.shields.io/badge/📥Download-dark?style=flat" style="height: 30px"/></a> 

1. Execute o arquivo setup.exe

2. Coloque o <code>script.ps1</code> em um lugar fácil, como na área de trabalho

> Obs.: Esse arquivo é só um exemplo de uso mas você pode adaptá-lo como achar melhor

3. Ative a execução de scripts do Windows Powershell, assim:

    3.1. Para fazer isso abra o Windows PowerShell como Administrador

    3.2. Execute esse comando: <code>Set-ExecutionPolicy Unrestricted</code>

    3.3. Na pergunta de confirmação, insira <code>A</code>

    3.4. Execute esse comando: <code>exit</code>

4. Clique com o botão direito no <code>script.ps1</code> e em Executar com PowerShell

5. Se executar as 2 janelas, já pode apagar os outros arquivos inúteis como o <code>EBS-CLI.zip</code> e a pasta <code>publish</code>

> Qualquer anormalidade no funcionamento, ou dúvida entre em contato com o e-mail thiagosousa81@gmail.com

</details>

### Comandos

<details><summary>Clique para visualizar...</summary>

#### Lista de Comandos

| Comando | Parâmetros | Função |
| --- | --- | --- |
| <code>help</code> | nenhum | Chamar ajuda do aplicativo |
| <code>Encrypt-File</code> | <code>URL_In</code><br><code>URL_Out</code><br><code>Algorithm</code><br><code>Key</code><br><code>IV</code><br><code>Multiple</code> | Encripta um arquivo e gera uma saída através dos parâmetros selecionados |
| <code>Decrypt-File</code> | <code>URL_In</code><br><code>URL_Out</code><br><code>Algorithm</code><br><code>Key</code><br><code>IV</code><br><code>Multiple</code> | Decripta um arquivo e gera uma saída através dos parâmetros selecionados |

#### Tipo de dado dos parâmetros

| Parâmetro | Tipo de dado |
| --- | --- | 
| <code>URL_In</code> | Path |
| <code>URL_Out</code> | Path |
| <code>Algorithm</code> | String |
| <code>Key</code> | String |
| <code>IV</code> | String |
| <code>Multiple</code> | Int32 |

> Obs.: Você pode digitar <code>Explorer</code> num parâmetro de caminho para selecionar o local com o Windows Explorer
  
</details>

### Exemplos de uso

<details><summary>Clique para visualizar...</summary>

#### Encriptando

    Encrypt-File
    C:\Users\User\Downloads\EBS-CLI.zip
    C:\Users\User\Downloads\EBS-CLI.zip
    RC2
    Thiago
    09876543
    10

    Encrypt-File
    C:\Users\User\Downloads\EBS-CLI.zip
    C:\Users\User\Downloads\EBS-CLI.zip
    DES
    74125896
    36251478
    50

    Encrypt-File
    C:\Users\User\Downloads\EBS-CLI.zip
    C:\Users\User\Downloads\EBS-CLI.zip
    AES
    741258961qazxsw2
    362514784rfvbgt5
    75

    Encrypt-File
    C:\Users\User\Downloads\EBS-CLI.zip
    C:\Users\User\Downloads\EBS-CLI.zip
    3DES
    741258961qazxsw2
    4rfvbgt5
    25

#### Decriptando

    Decrypt-File
    C:\Users\User\Downloads\EBS-CLI.zip
    C:\Users\User\Downloads\EBS-CLI.zip
    3DES
    741258961qazxsw2
    4rfvbgt5
    25

    Decrypt-File
    C:\Users\User\Downloads\EBS-CLI.zip
    C:\Users\User\Downloads\EBS-CLI.zip
    AES
    741258961qazxsw2
    362514784rfvbgt5
    75

    Decrypt-File
    C:\Users\User\Downloads\EBS-CLI.zip
    C:\Users\User\Downloads\EBS-CLI.zip
    DES
    74125896
    36251478
    50

    Decrypt-File
    C:\Users\User\Downloads\EBS-CLI.zip
    C:\Users\User\Downloads\EBS-CLI.zip
    RC2
    Thiago
    09876543
    10
    

</details>


### Ultima edição por [ThiagoSousa81](https://github.com/ThiagoSousa81/) em 16/05/2024

[VOLTAR](https://github.com/EBS-Security-Systems/EBS-Docs#readme)
