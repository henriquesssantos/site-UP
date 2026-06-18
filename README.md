# Ideia do projeto:

Meu objetivo foi criar uma página de destino (landing page) simples, que:

    1. Alerte sobre os perigos reais de passar o dia parado.
    2. Desmistifique conceitos errados sobre exercícios.
    3. Forneça ferramentas práticas (como cálculo de IMC e ingestão de água) para a pessoa dar o primeiro passo naquele exato momento.

## O Framework: Bootstrap (Tema Lux)

Para a interface, optei por utilizar o framework CSS Bootstrap (na versão 5.3.3), integrado com o tema Lux disponibilizado pelo Bootswatch.

Vantagens que percebi ao utilizar este framework:

    1. Responsividade: O site já se adapta automaticamente para telas de celulares e tablets sem que eu precisasse escrever dezenas de Media Queries no CSS.

    2. Agilidade Visual: Componentes como cards, botões (btn), e listas (list-group) já vêm com um design moderno e padronizado.

    3. Tema Lux: Escolhi este tema específico porque ele traz uma tipografia mais elegante, contrastes fortes e uma paleta de cores (como o primary escuro) que transmite seriedade, combinando muito bem com a área da saúde.

## Documentação e estrutura do codigo:

O projeto foi construído em um arquivo único (Single Page) para facilitar a visualização e entrega, dividido em três camadas principais:

### HTML Semântico e CSS Customizado
    Utilizei tags semânticas como <header>, <section>, e <footer> para organizar o conteúdo de forma lógica e acessível.

### CSS Complementar: 
    Embora o Bootstrap faça 90% do trabalho visual, adicionei um pequeno bloco de <style> no <head>. Usei isso para criar ícones personalizados com pseudo-elementos (::before) nas listas de mitos e verdades, e para implementar Flexbox na centralização exata das áreas de resultado das calculadoras.

### Seções da Página
#### Cabeçalho: Título principal e subtítulo de impacto.

    Por que mudar agora?: Apresenta os malefícios do sedentarismo e benefícios da mudança de hábito.
    Mito x Verdade: Uma seção comparativa visual usando cores (vermelho para perigo/mito, verde para sucesso/verdade).
    Ferramentas Úteis: Contém os formulários interativos (Cards).

### Lógica em JavaScript

Meu conhecimento a respeito de JS era bem precário, porem com ajuda da inteligencia artifical pude desensolver o codigo para as simples formulas necessárias e aprender um pouco sobre JS, conforme os comentários do código.

#### calcularIMC():

    Captura os valores de peso e altura digitados pelo usuário.
    Valida se os campos estão vazios ou com números negativos (retornando um aviso visual em vermelho usando .classList.add("text-danger")).
    Aplica a fórmula matemática (peso / (altura * altura)).
    Utiliza uma estrutura de condição (if / else if) para classificar o resultado segundo a OMS.
    Renderiza o resultado formatado (.toFixed(2)).

#### calcularAgua():

    Captura apenas o peso do usuário.
    Realiza a validação de segurança.
    Aplica o cálculo recomendado para hidratação (35ml de água por kg).
    Converte o resultado para Litros dividindo por 1000 e exibe na tela.

OBS: Toda estrutura HTML, escolha e divisão das tags foi feito de forma 100% manual. Já na parte da estilização, após ter encontrado o framework ideal depois de algumas pesquisas, utilizei a IA para colocar as tags corretas refenrente ao framework escolhido, porem teve algumas alterações manuais como cores e tamanhos de texto. 
