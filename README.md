# **Plantopedia - Documentação Oficial**  

| Versão    | O que mudou                      |
|-----------|----------------------------------|
| 0.1.0.70 | O código foi aprimorado, novas funções foram adicionadas e tudo foi otimizado. Agora o código é Open-Source sob a nova licença. |

## 📌 Essa documentação inclui:

- [Introdução](#introdução)  
- [Por que usar o Plantopedia?](#🌿-por-que-usar-o-plantopedia)  
- [O que é o Plantopedia?](#o-que-é-o-plantopedia)  
- [Principais Recursos](#principais-recursos)  
- [Como Usar](#como-usar)  
- [Como Usar a API](#como-usar-a-api)  
- [Contribuições](#contribuições)  
- [Termos de Uso](#termos-de-uso)  
- [Copyright e Licença de Uso](#copyright-e-licença-de-uso)

---

## **Introdução**  

O **Plantopedia** é um serviço gratuito e de código aberto que permite a pesquisa e catalogação de plantas. Ele fornece informações detalhadas sobre diversas espécies, incluindo nome científico, exigências de luz e água, propriedades medicinais e muito mais.

Nosso objetivo é democratizar o acesso ao conhecimento botânico, promovendo a preservação e o estudo da natureza de forma acessível e livre.  

### 🌿 **Por que usar o Plantopedia?**  
✔ Sem burocracia: use a API sem necessidade de chaves ou registros.  
✔ Open-source: qualquer pessoa pode contribuir com o projeto.  
✔ Gratuito: 100% livre para todos, sem custos.  
✔ Ilimitado: Sem limite de Requests mensais.

✔ Amplo e Flexível: Contém uma base estável e diversificada de dados, que é atualizada ocasionalmente para incluir mais dados.

---

## **O que é o Plantopedia?**  

O Plantopedia é uma **API** e **aplicativo autônomo** que rodam no GitHub.
O sistema permite que usuários busquem informações sobre plantas através de uma base de dados que está em constante crescimento.  

Ele é projetado para ser **simples e eficiente**, permitindo consultas rápidas sem a necessidade de autenticação ou credenciais.

O foco do app é ser **Direto ao Ponto.**

**Esse serviço depende de Terceiros para disponibilização de Imagens**

---

## **Principais Recursos**  

🌱 **Banco de Dados de Plantas** – Com informações científicas detalhadas.  
🔍 **Pesquisa por Nome Científico, Comum ou Características** – Encontre plantas facilmente, busque por nomes Populares, Comuns, Científicos, nomes na Schömner e até mesmo por características da planta, por exemplo buscar "Tronco Grosso" retorna plantas com essa característica.

Exemplo de Pesquisa:
```txt
Folhas redondas com espinhos, caules roxos e tronco delgado. Copa quadrada, raiz rasa, sempre tem 3 galhos principais.
```
📡 **API de Acesso Livre** – Use os dados sem complicação, não requer Conta, Requests, Assinatura e muito menos qualquer complicação, cole o link da API e pronto, faça requests.

📖 **Dados Botânicos Relevantes** – Inclui uma lista vasta de Dados como:

1. Nome na Schömner
2. Nome na Ciência
3. Tempo de Vida
4. Exigência de Luz (ex: 8H/Dia)
5. Exigência de Água (ex: 3L/Dia)
6. Tipo (ex: Frutífera)
7. Benefícios Ecológicos (ex: Atrai pássaros)
8. Suscetibilidade a Pragas/Doenças
9. Propriedades Medicinais
10. Se possui Fruto
11. Tipo de Fruto (ex: Comestível/Venenoso)
12. Tipo de Folha
13. Profundidade da Raiz
14. Altura Máxima
15. Taxa de Crescimento (ex: 30 cm/ano)
16. Solo Preferido (ex: Ácido/Seco)
17. De onde é Nativo
18. Nomes Populares/Comuns

E inclui questões detalhadas:

- [ Parágrafo 1;
Lista detalhes como característica das folhas, detalha características da planta, cada característica deve estar listada, como folhas, tronco, ou qualquer peculiaridade, um texto que permita identificar visualmente a planta. Isso inclui processos biológicos ou detalhes que as torne única (ex: a Pitangueira passa pelo amadurecimento das Folhas, nascem vermelhas e molengas e amadurece em algumas semanas. Isso é um dado útil e informativo) Lista dados assim ]

- [ Parágrafo 2;
Lista algo interessante como curiosidade ou fato sobre a planta que torna ela oque ela é (se houver) como origem do nome, ou algo intrigante ]

- [ Parágrafo 3;
Da informações sobre o fruto da Planta (se houver) e detalha sobre Flores, se houver, listando características e informações sobre elas. ]

- [Parágrafo 4;
Descreve o papel da planta no ecossistema, como ela interage com o ambiente ao redor, sua importância para a fauna e flora, e benefícios ecológicos gerais (ex: ajuda na polinização, fixação de nitrogênio, controle de erosão) ]

- [Parágrafo 5;
Se a planta tiver algum valor medicinal, descreve os usos mais comuns, propriedades terapêuticas e como ela tem sido utilizada historicamente em diferentes culturas. Se for uma planta com aplicação em cosméticos ou culinária, também pode ser mencionado ]

- [ Parágrafo: 6;
Se ela estiver em extinção, explica sobre e como preservar e o porquê está em extinção ]

---

## **Como Usar**  

1️⃣ Acesse o Plantopedia pelo botão ao lado: [Acessar Aplicativo](https://plantopedia.github.io/)  
2️⃣ Pesquise o nome de uma planta na interface do app ou via API.  
3️⃣ Veja informações detalhadas sobre a espécie desejada.  

Se quiser acessar os dados via API, confira a seção abaixo.  

---

## Como Usar a API

### 1. Adicione o Link da API ao seu HTML

Inclua a API no <head> do seu documento HTML para carregar o banco de dados de plantas:
```javascript
<script src="https://cdn.jsdelivr.net/gh/plantopedia/API@latest/planta-db.js"></script>
```

### 2. Criando a Interface de Pesquisa

Você pode criar seus próprios elementos HTML para pesquisa de plantas. Aqui está um exemplo simples:

```html
<!-- Barra de Pesquisa -->
<input id="search-bar" type="text" placeholder="Digite o nome da planta">
<button id="search-button">Buscar</button>

<!-- Espaço para exibir os resultados -->
<div id="results"></div>
```

### 3. Implementando a Pesquisa

O código abaixo permite buscar plantas no banco de dados da API e exibir os resultados. Você pode personalizá-lo conforme necessário pra atender ao seu gosto:

```javascript
<script>
/* Essa função garante que o Banco de Dados foi carregado antes de prosseguir com a pesquisa, se isso for removido pode dar erro, pois pode tentar acessar os documentos antes que eles existam. */
function ensurePlantIndexLoaded(callback) {
if (typeof window.plantIndex === "undefined") {

// Se o Banco de Dados ainda não foi carregado, espera 5ms e tenta novamente.
setTimeout(() => ensurePlantIndexLoaded(callback), 5);
} else {

// Se já está carregado, executa a função callback. 
callback(); }}

/* Função principal para pesquisar plantas */
function searchPlant() {

// Obtém o termo digitado pelo usuário e remove espaços extras
const query = document.getElementById("search-bar").value.trim();

// Obtém o elemento onde os resultados serão exibidos
const resultsContainer = document.getElementById("results");

// Limpa os resultados anteriores antes de mostrar novos
resultsContainer.innerHTML = ""; 

// Se o usuário não digitou nada, exibe uma mensagem e para a execução
if (!query) {
resultsContainer.innerHTML = "<p>Digite algo para buscar.</p>";
return; }

// Garante que a base de dados de plantas foi carregada antes de pesquisar
ensurePlantIndexLoaded(() => {

// Faz a busca pelo termo digitado pelo usuário
const results = buscarPlantas(query);
        
// Se nenhum resultado for encontrado, exibe uma mensagem e para a execução
if (!results.length || results[0].nome === "Nenhuma planta encontrada.") {

// Exibe visualmente 
resultsContainer.innerHTML = "<p>Nenhuma planta encontrada.</p>";
return; }

// Para cada planta encontrada, cria um card na tela
results.forEach(plant => {

// Se não houver arquivo vinculado à planta, ignora esse resultado
if (!plant.arquivo) return;

// Cria um elemento <div> para representar o card da planta
const card = document.createElement("div");
card.innerHTML = `<h3>${plant.nome}</h3><p>Carregando descrição...</p>`;

// Faz um request para buscar o arquivo da planta
fetch(plant.arquivo)
.then(response => response.text()) // Converte a resposta em texto
.then(scriptContent => {

// Cria um script para armazenar os dados da planta dinamicamente
const script = document.createElement("script");
script.innerHTML = `
(function() {
let localPlantData;
${scriptContent.replace("plantData =", "localPlantData =")}
window.plantDatabase = window.plantDatabase || {};
window.plantDatabase["${plant.arquivo}"] = localPlantData; })(); `;
document.body.appendChild(script); // Adiciona o script ao corpo da página

// Aguarda um curto tempo para garantir que os dados foram carregados
setTimeout(() => {
const plantData = window.plantDatabase[plant.arquivo];
if (plantData) {

// Atualiza o card com os detalhes da planta
card.innerHTML = `

// Nome da Planta (título)
<h3>${plantData.name}</h3>

// Prévia de Descrição (após o 0 define quantos caracteres serão visíveis na prévia
<p>${plantData.about.substring(0, 100)}...</p>

// Opcional, para Abrir o Card
<button onclick='openPlantDetails(${JSON.stringify(plantData)})'>Ver mais</button>
`;
}}, 100); });

/* Adiciona o card ao container de Resultados
resultsContainer.appendChild(card); });});}

/* Função para exibir os detalhes da planta em um alerta (pode ser melhorado para mostrar em um modal) */
function openPlantDetails(plantData) {
alert(`Nome: ${plantData.name}\nDescrição: ${plantData.about}`); }

/* Adiciona eventos para chamar a função de pesquisa ao clicar no botão ou pressionar "Enter" */

// Clique
document.getElementById("search-button").addEventListener("click", searchPlant);

// Pressionando Enter
document.getElementById("search-bar").addEventListener("keypress", function(event) {
if (event.key === "Enter") {
searchPlant(); }});
</script>
```

### 4. Personalizando os Resultados

Alterar estilos: Modifique o CSS dos elementos para adaptar o design ao seu gosto.

Adicionar mais informações: O objeto plantData contém detalhes adicionais como nome científico, exigências de luz e água, propriedades medicinais, entre outros.

Alterar exibição: Você pode substituir a alert() por um modal, um painel lateral ou qualquer outro método de exibição.

### Estrutura de Dados

O Plantopedia API retorna objetos no seguinte formato:
```javascript
plantData = {
name: "Nome Geral da Planta",
schominicalName: "Nome na Schömner",
scientificName: "Nome na Ciência",
lifespan: "Tempo de Vida",
lightRequirement: "Quanto de luz deve consumir por dia",
waterRequirement: "Quanto de água bebe por dia",
type: "Tipo de Planta",
ecologicalBenefits: "Benefícios Ecolôgicos",
pestSusceptibility: "Suscetibilidade a Pragas",
medicinalProperties: "Propriedades Medicinais",
hasFruit: true,
fruitType: "Tipo de Fruta",
leafType: "Tipo de Folha",
rootDepth: "Profundidade da Raiz",
maxHeight: "Altura máxima",
growthRate: "Taxa de crescimento, quanto cresce em quanto tempo",
preferredSoil: "Tipo de solo preferido",
nativeRegion: "País ou Região que é Nativa",
sustainability: "Oque ela melhora na Natureza",
popularNames: ["Nomes separados", "Dessa Forma"],
image: "Link da Imagem",
about: `Descrição detalhada da Planta` };
```
---

## Contribuições

O Plantopedia é um projeto aberto e aceita contribuições da comunidade.

💡 Como ajudar?

1. Sugira melhorias no código
2. Liste novas plantas para adicionar ao banco de dados
3. Melhorias na documentação
4. Contribua dando Estrela no GitHub

Para contribuir no GitHub, acesse:

[Página da API](https://github.com/plantopedia/API)

[Página do Aplicativo](https://github.com/plantopedia/plantopedia.github.io)

---

## Termos de Uso

O Plantopedia é oferecido gratuitamente para qualquer pessoa utilizar. No entanto, ao usar nossa API e banco de dados, você concorda com os seguintes termos:

1️⃣ Uso Livre – Os dados podem ser usados para qualquer propósito, desde que citada a fonte, não é necessário poluir visualmente seu design com os créditos, embora seja o mais adequado inserir um texto nem que pequeno, mas é sempre necessário incluir a Documentação Oficial do Plantopedia.

2️⃣ Sem Garantias – As informações são fornecidas como estão, sem garantias de precisão ou disponibilidade por terceiros, uma vez que Terceiros podem inserir dados customizados nos resultados. Garantimos precisão nos requisitos que nós mesmos listamos, se não está listado, não é garantido.

3️⃣ Respeito ao Código Aberto – Modificações são bem-vindas, desde que respeitem a licença do projeto, veja abaixo como você pode usar este código.

---

## Copyright e Licença de Uso

O Plantopedia foi construído sobre uma licença customizada da **Creative Commons 4.0**, chamada **ALL-TO**, que permite os seguintes usos:

### O que você pode fazer?

1. Uso Ilimitado da API – Você pode fazer requisições sem restrição de quantidade.

2. Acesso ao Banco de Dados – Qualquer item disponível pode ser consultado livremente.

3. Uso do Código-Fonte – Você pode se inspirar e reutilizar trechos de CSS, HTML ou JavaScript do Plantopedia.

4. Modificação e Redistribuição – É permitido remixar, modificar ou repostar o conteúdo do Plantopedia.

5. Compartilhamento Livre – Os dados podem ser compartilhados em qualquer rede social ou plataforma.

**Porém**

Se você utilizar qualquer parte do Plantopedia, você deve seguir estas regras:

1. Creditação Obrigatória – Sempre atribua o devido crédito aos desenvolvedores oficiais do Plantopedia:
**Kirey Cazkdnsky
Kireiygo**


2. Descrição do Uso – Se você usar CSS, JS, HTML ou alguma parte do banco de dados, informe claramente o que foi utilizado.


### O que você **NÃO**pode fazer?

A licença ALL-TO impõe algumas restrições para evitar usos indevidos do Plantopedia:

1. Proibido Uso em Sites Monetizados de Alta Renda

Você **NÃO** pode utilizar o Plantopedia em sites, aplicativos ou serviços empresariais que tenham lucro bruto superior a R$10.000,00 (considerando toda a empresa).

Pequenos projetos e negócios com ganhos abaixo desse valor podem utilizar sem restrição, oque pode ser burlado somente sob permissão clara do desenvolvedor permitindo o uso.


2. Proibido para Sites de Jornalismo

Você *NÃO* pode indexar ou usar o sistema como ferramenta para pesquisas jornalísticas.

O uso para criação de artigos científicos ou educativos é permitido.


3. Proibido Adulterar Informações sem Aviso

Se você modificar qualquer dado do Plantopedia, deve deixar claro que a informação foi alterada.

A modificação deve ser indicada em Texto Vermelho, com Fundo Preto, sem Transparência, e uma Fonte de no mínimo 30px em qualquer dispositivo (via CSS).

### Quais são as exceções?

1. Uso Educacional Permitido

O Plantopedia pode ser utilizado para fins educativos, como:

Sites informativos sem fins lucrativos
Vídeos no YouTube
Projetos pessoais ou acadêmicos


2. Uso para Pequenos Criadores de Conteúdo

Se você é um criador de conteúdo independente, pode utilizar o Plantopedia, desde que siga as regras de creditação.

Se houver alguma monetização, desde que não ultrapasse R$10.000,00 brutos, o uso é liberado.

---

## Perguntas Frequentes (FAQ)

1. Posso usar o Plantopedia em um aplicativo gratuito?

Sim, desde que o aplicativo não ultrapasse a renda bruta de R$10.000,00 e siga as regras de creditação.

2. Posso copiar partes do código-fonte do Plantopedia para outro projeto?

Sim, você pode reutilizar trechos de CSS, HTML ou JS, desde que credite os desenvolvedores e informe o que foi utilizado.

3. Posso vender um projeto que use o banco de dados do Plantopedia?

Não, a licença proíbe o uso para fins comerciais de alta renda. Projetos educacionais ou sem fins lucrativos são permitidos.

4. Posso modificar informações do banco de dados e usá-las no meu site?

Sim, mas você deve indicar a alteração conforme exigido (Texto Vermelho, Fundo Preto, sem Transparência e Fonte de no mínimo 30px).

5. O que acontece se eu não creditar os desenvolvedores?

O uso sem creditação viola a licença ALL-TO, e seu acesso ao Plantopedia poderá ser bloqueado ou restringido, primeiramente você será comunicado, e terá 3 chances para corrigir possíveis problemas danosos.

6. Posso usar o Plantopedia para um site de pesquisas científicas?

Sim, desde que o uso seja para fins educacionais ou acadêmicos e não seja para jornalismo ou lucro acima do limite permitido.

7. Existe alguma restrição técnica para o uso da API?

Atualmente, a API do Plantopedia não possui limite de requisições, mas o uso excessivo pode ser monitorado para evitar abusos.

---

#### Reservamos o direito de remover qualquer projeto que seja danoso a nós, limitar ou dar strike em conteúdo que abuse do nosso sistema ou o use indevidamente apenas para fim de lucro (exemplo: Jornais que postam crianças mortas para viralizar e ganhar encima disso, cegamente fazendo de tudo por dinheiro)

#### Também reservamos o direito de atualizar a Documentação a qualquer momento sem aviso prévio.

#### [Acesse o Discord da Phrest para falar diretamente com o CEO dono do Plantopedia](https://discord.gg/btqkKbt3je)
