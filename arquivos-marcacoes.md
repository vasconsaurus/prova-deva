## **XML**

O arquivo XML consiste de _tags_, similar a um arquivo HTML. Por exemplo:

```
<pessoa idade="40" sexo="M">
    José Silva
</pessoa>
```

Na primeira linha do arquivo declaramos a versão do XML ou a codificação dos caractéres. Por exemplo:

```
<?xml version="1.0" encoding="UTF-8"?>
```

O XML segue um _schema_, um conjunto de normas, que define regras de validação quanto aos parâmetros que esperamos receber e seus formatos. Os _schemas_ também são documentos XML, recebem o nome de _XML Schema Definition_, XSD.

### **Vantagens**

- fácil legibilidade para humanos e sistemas
- extremamente extensível
- sua estrutura representa muito bem diversos cenários

### **Desvantagens**

- o uso de _tags_ aumentam o espaço necessário para armazenar o arquivo
- pode se tornar muito complexo
- pode gerar arquivos muito pesados

### **Exemplos de uso**

- é usado no protocolo SOAP
- foi usado até 2003 para armazenar dados de planilha do Excel
- pode ser usado para facilitar o trabalho de ferramentas de busca
- emissão de notas fiscais de Prefeituras ou do Estado

## **JSON**

Utiliza objetos existentes de JavaScript,
JSON é uma sigla para _JavaScript Object Notations_. Começou a ser usado no fim de 90, começo dos 2000. Sua padronização mais recente foi em 2017. Sua popularidade cresceu muito graças a ser o modo preferido de lidar com dados em requisições AJAX. É usado na maioria das APIs do mercado.

Possui o modelo chave-valor (como um objeto de JavaScript). Por exemplo:

```
{
  "nome": "Maria José",
  "idade": 30,
  "salario": 15000.00,
  "tecnologias": [
    "HTML",
    "CSS",
    "JavaScript",
    "Python"
  ]
}
```

### **Vantagens**

- é mais rápido que o XML
- tem alta compatibilidade
- server-side parsing é rápida com JSON
- o fato de armazenar os dados em objetos e arrays torna sua manipulação mais fácil

### **Desvantagens**

- não tem error handling para JSON calls
- 'falha silenciosamente'
- é vulnerável a uma serie de ataques

## **YML**

YAML ou YML, inicialmente _Yet Another Markup Language_, e agora _YAML Ain't Markup Language_, foi criado em 2001 e teve sua primeira versão em 2004.

Assim como JSON também usa o modelo "chave-valor". Mas diferente do JSON, aqui se diferencia onde cada coisa começa pela quebra de linhas e identação. Por exemplo:

```
exemplo1: meu valor sem aspas
exemplo2: "meu valor em aspas duplas"
exemplo3: 'meu valor em aspas simples'
exemplo4: |-
  Minha string dividida em várias
  linhas diferentes, com as quebras
  de linha sendo levadas em consideração
exemplo5: >-
  Outra string dividida em várias
  linhas, mas a diferença é que
  esta sintaxe ignora as quebras
  de linha
```

Podemos construir diciónarios e listas com YAML, basta atentar a identação.

Dicionário:

```
dados:
  nome: José Silva
  idade: 40
  sexo: M
```

Lista:

```
lista1:
  - valor1
  - valor2
  - valor3
lista2: [valor1, valor2, valor3]
```

> Algo interessante é que grande parte das bibliotecas de processamento de JSON também conseguem ler documentos YAML, pois é um superconjunto de JSON. Portanto, é possível usar algumas ferramentas de validação de schemas em JSON para validar YAML. O site Schema Validation for YAML (em inglês) elenca as principais opções para este cenário.

### **Vantagens**

- é ainda mais leve que o JSON
- tem uma ótima legibilidade
- torna fácil entender os dados
- tem uma grande variedade de usos, desde configuração à transferência de dados
- como é um superconjunto do JSON é fácil trocar entre um e outro, você pdoe usar o mesmo parser

### **Desvantagens**

- muitas aplicaçõe já usam XML ou JSON, sendo difícil substituir por YAML
- XML tem um ecosistema muito mais maduro
- é mais fácil achar suporte para JSON
- é fácil de quebrar ao errar um simples espaço da sua identação
- é complexo de processar, XML e JSON tem uma performance melhor.
