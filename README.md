# Projeto de Infraestrutura de TI - Vinícola Terras do Vinho

![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-green)
![Platform](https://img.shields.io/badge/Plataforma-Windows%20Server-blue)

## 📖 Sobre o Projeto

[cite_start]Este repositório contém a documentação completa de um projeto acadêmico desenvolvido para a disciplina de **Sistemas Operacionais II** do curso de Tecnologia em Análise e Desenvolvimento de Sistemas da **Fatec Itu - Dom Amaury Castanho**[cite: 1, 8].

[cite_start]O objetivo do projeto foi planejar e implementar a infraestrutura de Tecnologia da Informação para a empresa fictícia "Vinícola Terras do Vinho"[cite: 2], utilizando um ambiente baseado em Windows Server com Active Directory, políticas de grupo (GPO), servidor de arquivos e segurança de rede com proxy.

##  winery Cenário

[cite_start]A **Vinícola Terras do Vinho** é uma empresa familiar que nasceu do sonho de três gerações[cite: 79]. [cite_start]A empresa possui uma estrutura departamental clara, incluindo setores de Produção, Vendas, Financeiro, Logística e Compras, todos sob a liderança da presidente Maria Martins[cite: 154]. Para suportar seu crescimento, foi proposta uma infraestrutura de TI centralizada, segura e organizada.

## 🛠️ Tecnologias e Ferramentas

* **Sistema Operacional:** Windows Server
* **Serviços de Diretório:** Active Directory Domain Services (AD DS)
* **Gerenciamento:** Group Policy Management Console (GPMC)
* **Serviços:** Servidor de Arquivos (File Server), DNS, DHCP
* [cite_start]**Segurança de Rede:** Endian Firewall (Proxy e Filtro de Conteúdo) [cite: 195]

## ✨ Funcionalidades Implementadas

A infraestrutura foi configurada com as seguintes funcionalidades e políticas:

### 1. Gerenciamento de Identidade e Acesso (Active Directory)
* [cite_start]**Domínio:** Criação do domínio principal `terradovinho.NET`[cite: 155].
* [cite_start]**Estrutura Organizacional (OUs):** Unidades Organizacionais foram criadas para cada departamento da empresa (Compras, Logística, Financeiro, Vendas, Produção e Presidência) para organizar objetos e aplicar políticas específicas[cite: 155].
* [cite_start]**Usuários e Grupos:** Todos os funcionários foram cadastrados como usuários e organizados em grupos de segurança correspondentes a seus departamentos (ex: `GR_Compras`, `GR_Vendas`)[cite: 157, 160].

### 2. Servidor de Arquivos e Permissões
* **Estrutura de Pastas:** Diretórios departamentais foram criados para o armazenamento centralizado de arquivos.
* **Permissões NTFS:** O acesso às pastas é restrito por grupos. [cite_start]Usuários só podem acessar os diretórios de seu próprio setor, com permissões de "Leitura e Execução", enquanto administradores possuem controle total[cite: 163, 164].
* [cite_start]**Cotas de Armazenamento:** Foram implementadas cotas de disco para limitar o espaço de armazenamento por usuário (400MB para funcionários e 800MB para a presidência)[cite: 167, 165].

### 3. Políticas de Grupo (GPO)
Foram aplicadas GPOs para automatizar configurações e reforçar a segurança:
* [cite_start]**Mapeamento de Unidades de Rede:** Mapeamento automático de drives de rede (T:, U:, V:, W:, Y:, Z:) para cada departamento, garantindo acesso rápido aos arquivos do setor[cite: 172, 173].
* [cite_start]**Wallpaper Corporativo:** Definição de um papel de parede padrão em todas as estações de trabalho para reforçar a identidade visual da empresa[cite: 176].
* [cite_start]**Bloqueio do Painel de Controle:** Restrição de acesso ao Painel de Controle para evitar alterações indevidas no sistema pelos usuários[cite: 177].
* [cite_start]**Bloqueio de Dispositivos USB:** GPO que impede a leitura e gravação em mídias removíveis, aumentando a segurança contra vazamento de dados e malware[cite: 175].
* [cite_start]**Configuração de Proxy Centralizada:** Aplicação automática das configurações de proxy para todos os usuários, garantindo que todo o tráfego de internet passe pelo firewall[cite: 178].

### 4. Segurança de Rede e Controle de Acesso
* [cite_start]**Servidor Proxy:** Implementação do Endian Firewall como servidor proxy para monitorar e filtrar o tráfego web[cite: 195].
* [cite_start]**Filtro de Conteúdo:** Criação de políticas de acesso à internet com três níveis[cite: 183]:
    * `GR_Endian_Liberado`: Acesso irrestrito para sites essenciais.
    * [cite_start]`GR_Endian_Bloqueado`: Bloqueio total a sites inadequados (redes sociais, entretenimento)[cite: 189].
    * [cite_start]`GR_Endian_Filtrado`: Acesso monitorado e com restrições a categorias específicas de conteúdo (Jogos, Compras, etc.)[cite: 191, 201].

## 👥 Autores

Este projeto foi desenvolvido por:

* [cite_start]Calebe Sousa de Araujo [cite: 3]
* [cite_start]Cleiton Valentim [cite: 4]
* [cite_start]Ivo Sousa Araujo [cite: 5]
* [cite_start]José Carlos Carneiro [cite: 6]
* [cite_start]Kátia Cursi [cite: 7]

### Professor Orientador
* [cite_start]Prof. Celso Corazza [cite: 1]

---
