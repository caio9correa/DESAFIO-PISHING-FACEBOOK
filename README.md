# Phishing para captura de credenciais do Facebook

### 🛠️ Ferramentas 

- Kali Linux (Virtual Box)
- setoolkit

### 🔐 Defesa do Facebook contra scripts maliciosos
- Atualmente o Facebook possui uma proteção contra script maliciosos, o que impede que a ferramenta setoolkit extraia as credenciais na forma mais básica de usar os comenados. Isso pode ser visto na imagem abaixo:

<div align="center">
<img src="https://github.com/user-attachments/assets/11209e53-c525-48ae-9bbf-70e3469cbcf4" width="700px" />
</div>

### ⚙️ Configurando o Phishing no Kali Linux
Já podemos deixar nosso Setoolkit pronto para clonarmos o site. Para isso basta seguir os passos abaixo:
- Acesso root: ``` sudo su ```
- Iniciando o setoolkit: ``` setoolkit ```
- Tipo de ataque: ``` Social-Engineering Attacks ```
- Vetor de ataque: ``` Web Site Attack Vectors ```
- Método de ataque: ```Credential Harvester Attack Method ```
- Método de ataque: ``` Site Cloner ```
- Obtendo o endereço da máquina: ``` ifconfig ```
- URL para clone: http://www.facebook.com

### ↩️ Burlando a defesa
- Para passarmos por essa defesa, podemos usar a própria opção que está no próprio ```setoolkit``` onde se pode realizar ```Custon Import```. Nesta opção iremos realizar uma alteração no código fonte, removendo o script de defesa e em seguida clonar o site através do código fonte que editamos. 

<div align="center">
<img src="https://github.com/user-attachments/assets/64408bd3-7b39-4f29-ad8f-975ff44f83bb" width="700px" />
</div>

### Salvar página

- No site original do facebook (www.facebook.com), iremos salvar a página com o nome ```index.html```. 

<div align="center">
<img src="https://github.com/user-attachments/assets/8d653af8-b85f-4d78-8fce-9f1aa7c3a792" width="700px" />
</div>

### Editando código fonte (index.html)

- Em seguida iremos copiar o código fonte do site oficial do facebook (www.facebook.com) e colar no arquivo que salvamos (index.html) substituindo todo o código anterior.

<div align="center">
<img src="https://github.com/user-attachments/assets/736e2779-e2b5-44d2-bc8a-5b9d67027d26" width="700px" />
</div>

<div align="center">
<img src="https://github.com/user-attachments/assets/c74c9e68-88de-4173-b7f2-9d7fc67ca715" width="700px" />
</div>

<div align="center">
<img src="https://github.com/user-attachments/assets/9352296e-820b-449b-9771-7878949eda16" width="700px" />
</div>

- Agora no código fonte que colamos, iremos identificar em qual script o ```button ID``` está sendo chamado e em seguida apagar.

<div align="center">
<img src="https://github.com/user-attachments/assets/7195162f-1914-4bf7-9ce7-c3a378e64bfb" width="700px" />
</div>

- Agora basta salvar o arquivo e acessarmos novamente o setoolkit.

### 🟰 Clonando o index usando o Custom Import do Setoolkit

- No ```setoolkit``` iremos selecionar a opção ```Custom Import``` e apontar para a pasta onde o código fonte (index.html) que editamos se encontra.

- Copie o diretorino da pasta onde se localiza o código fonte manipulado.

- Cole o diretório no setoolkit. 

![COLAR O DIRETORIO](https://github.com/user-attachments/assets/4f49c8a4-9877-4af6-b537-b3ca57533681)

->Selecione ```Copy the entire folder```

![OPÇÃO COPIAR A PASTA INTEIRA](https://github.com/user-attachments/assets/7ecadd9c-1229-4e74-9894-f423d6023aa3)

### Resutados (Versão sem Defesa)

->Em seguida defina a ```URL``` do site importado.

![DEFINIR COM A URL DA PAG FONTE](https://github.com/user-attachments/assets/50e80c13-6ea2-42e9-ab2c-399edf6f20dd)

## Resultado após aplicação do método contra a defesa

![USER AND PASSWORD](https://github.com/user-attachments/assets/11b8a323-1403-41d8-81d6-1744a0e448be)
