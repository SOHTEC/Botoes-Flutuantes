## Como adicionar os Botões Flutuantes da SOHTEC em seu Site.

Veja abaixo os passos necessários para inserir os botões da SOHTEC em seu site, e utilizar todos os recursos da nossa plataforma.

### 1º - Adicionar Biblioteca

Inserir ao final da tag **HEAD** do site a chamada para o script da biblioteca da SOHTEC

Exemplo:
```html {.line-numbers}
<head>
  ...
  <link href="https://api.sohtec.com.br/Scripts/2.0/soh-style.min.css" rel="stylesheet" type="text/css">
  <script type="text/javascript" src="https://api.sohtec.com.br/Scripts/2.0/soh-lib.js"></script>
</head>
```

### 2º - Adicionar Script de configuração para o botão flutuante.

Inserir no inicio da tag **BODY** do site a chamada para as configurações.

**Obs:** O **ID_DA_SUA_EMPRESA** é fornecido pela SOHTEC no momento do contrato.

Exemplo:
```html {.line-numbers}
<script type="text/javascript">
  
    //SOH_API.Imovel é OPCIONAL, ou seja, ele deve ser informado sempre que estiver na página de detalhe de um imóvel
    //Se estiver na Home do  site ou qualquer outra página favor não informar o SOH_API.Imovel.
    SOH_API.Imovel = {
        "Modulo": "LOCACAO", //ou VENDAS
        "Codigo": "0002",
        "FotoUrl": "https://sohtec.com.br/services//images/modelo.jpg", //Informe a URL Absoluta da imagem (Ex: http://www.seudominio.com.br/imagem.jpg)
        "Endereco": "Endereco Teste",
        "Numero": "1234",
        "Complemento": "Apto 305",
        "Bairro": "Bairro teste",
        "Cidade": "Cidade Teste",
        "Estado": "RS",
        "Dormitorios": "3",
        "Vagas": "2",
        "Cep": "00000-000",
        "Valor": 1200.25,
        "Condominio": 653.45,
        "Iptu": 147.89,
    };
  
    var config = {
        "EmpresaId": ID_DA_SUA_EMPRESA,            
        "whatsapp": {
            "enable": true,
            "posicao": "right",
            "bottom": "50px"
        },
    };

    SOH_API.INIT(config);
  
</script>
```
