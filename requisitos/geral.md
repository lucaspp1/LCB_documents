# Especificação de Requisitos do Sistema

## 1. Introdução

### 1.1 Propósito

O propósito deste documento é definir os requisitos para o desenvolvimento de um **Sistema de Gestão de Treinos e Dietas (LCB)**. O sistema permitirá que os usuários criem e gerenciem planos de treino personalizados, controlem sua dieta e acompanhem a evolução física por meio de gráficos e previsões de resultados. O sistema deve operar com a filosofia "offline first", garantindo o uso de suas principais funções sem conexão com a internet, exceto para sincronização e visualização de gráficos e históricos.

### 1.2 Escopo

O sistema tem como objetivo atender praticantes de atividades físicas que buscam personalizar e acompanhar seus planos de treino e dieta. O aplicativo será disponibilizado para dispositivos móveis e permitirá a criação e edição de treinos, gestão de dieta, acompanhamento de evolução física e compartilhamento de planos de treino e dieta com outros usuários.

### 1.3 Definições, Acrônimos e Abreviações

* **Offline First**: Arquitetura que prioriza o funcionamento do sistema sem conexão com a internet, sincronizando os dados quando uma conexão estiver disponível.
* **CRUD**: Create, Read, Update, Delete (operações básicas de dados).
* **Sincronização**: Processo de atualização dos dados locais com o servidor remoto quando há internet.

## 2. Descrição Geral

### 2.1 Perspectiva do Produto

O sistema será um aplicativo móvel **Offline First**, permitindo que os usuários criem, editem e gerenciem seus treinos e dietas sem necessidade constante de conexão com a internet. Ele deverá sincronizar os dados quando a conexão for restabelecida e será capaz de gerar gráficos de evolução física (peso, desempenho no treino) e previsões de ganhos e perdas de peso.

### 2.2 Funções do Produto

* Criação e personalização de treinos, com controle de variáveis como séries, repetições, intervalos e carga.
* Gerenciamento de dietas, com controle de alimentos, calorias e nutrientes.
* Acompanhamento da evolução física, com gráficos e registros de peso e medidas corporais.
* Previsões de ganho/perda de peso baseadas no plano de treino e dieta, com opções semanal, mensal e anual.
* Compartilhamento de planos de treino e dieta com outros usuários.
* Sincronização de dados de treino e dieta quando a internet estiver disponível.
* Operação **Offline First**, permitindo que o sistema funcione sem internet, exceto para gráficos e históricos.

### 2.3 Usuários do Sistema

* **Usuário Comum**: Pode criar, editar e acompanhar planos de treino e dieta, atualizar suas medidas corporais e compartilhar suas rotinas com outros usuários.

## 3. Requisitos Funcionais

### 3.1 Cadastro e Autenticação de Usuários

* **Descrição**: O sistema permitirá que usuários se cadastrem e façam login com suas credenciais.
* **Entrada**: Nome, e-mail, senha.
* **Processo**: Validação e criação de contas de usuários.
* **Saída**: Acesso à conta pessoal para gerenciamento de treinos e dieta.

### 3.2 Criação e Edição de Exercícios

* **Descrição**: O usuário poderá criar, editar e salvar um exercício para adicionar posteriormente a um plano de treino personalizado.
* **Entrada**: Nome, músculo alvo, músculos auxiliares, mídia * do exercício (foto ou gif), equipamento, **Descrição**.
* **Processo**: O sistema armazenará o exercício e permitirá que o usuário faça edições posteriores.
* **Saída**: Exercício salvo no dispositivo local e na nuvem.

### 3.3 Criação e Edição de Plano de Treino

* **Descrição**: O usuário poderá criar, editar e salvar um plano de treino personalizado.
* **Entrada**: Exercício (previamente cadastrado), quantidade de séries, repetições, intervalo (opcional), carga, observações, técnica avançada (opcional).
* **Processo**: O sistema armazenará o plano de treino e permitirá que o usuário faça edições posteriores.
* **Saída**: Plano de treino salvo no dispositivo local e na nuvem.

### 3.4 Gerenciamento de Dieta

* **Descrição**: O sistema permitirá que os usuários registrem e controlem seus alimentos e calorias diárias, divididos em blocos de refeições previamente cadastrados.
* **Entrada**: Alimento cadastrado, quantidade, bloco de refeição (café, almoço, lanche, etc.).
* **Processo**: O sistema calculará o total de calorias e nutrientes consumidos e armazenará a dieta.
* **Saída**: Dieta registrada com total de calorias e nutrientes.

### 3.5 Acompanhamento de Evolução Física

* **Descrição**: O sistema permitirá que o usuário registre suas medidas e peso para acompanhar sua evolução.
* **Entrada**: Peso, medidas corporais (braços, cintura, etc.).
* **Processo**: O sistema armazenará esses dados e gerará gráficos de evolução.
* **Saída**: Gráficos de evolução física e tabelas de medidas.

### 3.6 Previsão de Ganho/Perda de Peso

* **Descrição**: O sistema calculará previsões de ganho ou perda de peso com base em parâmetros científicos, onde o aumento ideal de peso é entre 0,25% e 0,5% do peso corporal por semana.
* **Processo**: O sistema calculará estimativas semanais, mensais e anuais de ganho/perda de peso.
* **Saída**: Previsões de peso exibidas ao usuário.

### 3.7 Compartilhamento de Treino e Dieta

* **Descrição**: O sistema permitirá que os usuários compartilhem seus planos de treino e dieta com outros usuários.
* **Entrada**: Seleção de treino ou dieta para compartilhar e usuário destinatário.
* **Processo**: O sistema enviará os dados do plano para o usuário selecionado.
* **Saída**: Confirmação de compartilhamento.

### 3.8 Sincronização de Dados (Offline First)

* **Descrição**: O sistema deve operar sem conexão com a internet e sincronizar os dados de treino e dieta quando a conexão for restabelecida.
* **Entrada**: Dados do usuário armazenados localmente.
* **Processo**: O sistema sincronizará automaticamente os dados com o servidor remoto ao detectar conexão.
* **Saída**: Dados sincronizados com sucesso.

## 4. Requisitos Não Funcionais

### 4.1 Performance

O sistema deve funcionar sem atrasos perceptíveis em modo offline para as funções de treino e dieta.
A sincronização deve ser realizada em segundo plano, sem impactar a experiência do usuário.

### 4.2 Segurança

Os dados do usuário devem ser armazenados localmente de maneira criptografada.
As credenciais de login devem seguir padrões de segurança com autenticação segura (por exemplo, OAuth2).

### 4.3 Usabilidade

A interface deve ser intuitiva e responsiva para dispositivos móveis.
O design deve ser adaptado para fácil navegação, permitindo que usuários criem e gerenciem treinos e dietas com poucos cliques.

### 4.4 Disponibilidade

O sistema deve estar disponível em plataformas iOS e Android.
O modo offline deve funcionar completamente para a criação e edição de treinos e dietas.

## 5. Conclusão

Este documento especifica os requisitos funcionais e não funcionais do **Sistema de Gestão de Treinos e Dietas (LCB)**, que permitirá a personalização de treinos, controle de dieta, acompanhamento de evolução física e o compartilhamento de planos com outros usuários. O sistema será construído com uma arquitetura "offline first", garantindo que as principais funcionalidades estejam sempre disponíveis, mesmo sem conexão à internet.
