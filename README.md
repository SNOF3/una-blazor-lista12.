# una-blazor-lista12.
aula interação e UX 
Aqui está o modelo estruturado para o seu projeto, focado na clareza técnica e na organização exigida:

---

## 1. Identificação
* **Nome Completo:** HEITOR SOUSA CARMO 
* **Curso:** CIÊNCIA DA COMPUTAÇÃO 

---

## 2. Heurísticas de Nielsen Aplicadas
As heurísticas de Nielsen são princípios de design que garantem uma interface intuitiva. No desenvolvimento deste componente, destacam-se:

* **Visibilidade do Status do Sistema:** O componente fornece feedback imediato ao usuário (ex: ao atualizar o contador ou carregar dados), garantindo que ele saiba exatamente o que está acontecendo internamente no sistema.
* **Flexibilidade e Eficiência de Uso:** Através do uso de parâmetros, o componente permite que tanto usuários novatos quanto experientes interajam com a interface de forma otimizada, adaptando-se a diferentes contextos de dados sem a necessidade de recriar a estrutura.

---

## 3. Guia de Execução
Para rodar o projeto localmente via terminal, siga os passos abaixo:

1.  **Clonar o repositório:**
    `git clone [URL_DO_REPOSITORIO]`
2.  **Acessar a pasta do projeto:**
    `cd [NOME_DA_PASTA]`
3.  **Instalar as dependências:**
    `npm install` ou `yarn install`
4.  **Iniciar a aplicação:**
    `npm start` ou `yarn start`
5.  **Visualizar no navegador:**
    Acesse `http://localhost:3000` (ou a porta indicada no seu terminal).

---

## 4. Explicação Técnica: Reutilização via Parâmetros
O uso de **[Parameter]** (ou *Props* em frameworks como React/Vue) é o que torna este componente verdadeiramente dinâmico. 

### Como funciona:
Em vez de "chumbar" (hardcode) informações como títulos, cores ou funções dentro do código, o componente foi construído como um molde vazio. Ao chamar o componente, passamos o **[Parameter]** como um argumento.

* **Abstração de Dados:** O componente não precisa saber *o que* está exibindo, apenas *como* exibir. Se passarmos um parâmetro de "cor", o mesmo botão pode ser azul para "Confirmar" ou vermelho para "Deletar".
* **Manutenibilidade:** Se precisarmos alterar o estilo do componente, alteramos em um único arquivo, e todos os lugares que utilizam esse **[Parameter]** serão atualizados automaticamente, seguindo o princípio **DRY** (*Don't Repeat Yourself*).

> **Nota Técnica:** No código, isso é implementado recebendo o objeto de parâmetros na assinatura da função do componente, permitindo que a lógica interna renderize o conteúdo de forma condicional ou dinâmica.
