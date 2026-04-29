# 🌐 MAJB Sistemas - Portal de Soluções CRM

Bem-vindo ao repositório central da **MAJB Sistemas**. Este projeto funciona como a "porta de entrada" (Landing Page) e o Hub de acesso para todos os sistemas de gestão personalizados desenvolvidos sob o domínio **majb.online**.

## 🏛️ Arquitetura do Projeto

O portal foi desenhado seguindo o conceito de **Micro-Frontends Desacoplados**:

1.  **Capa Principal:** Uma landing page moderna que apresenta a marca e lista os sistemas disponíveis.
2.  **Subdiretórios de Clientes:** Pastas independentes (ex: `/lql`) que utilizam o **Método Iframe Blindado** para exibir os sistemas processados no Google Apps Script, mascarando a infraestrutura da Google e mantendo a identidade visual da MAJB.

## 🛠️ Tecnologias Utilizadas

- **Frontend:** HTML5 e CSS3 (Tailwind CSS) para um design responsivo e de alta performance.
- **Tipografia:** Fonte Inter (Google Fonts).
- **Iconografia:** Font Awesome 6.
- **Hospedagem:** Hostinger (hPanel).
- **Versionamento:** Git para controlo de alterações independentes do núcleo do CRM.

## 📂 Estrutura de Pastas

```text
/ (raiz)
├── index.html           # Landing Page principal da MAJB Sistemas
├── .gitignore           # Ignora pastas de desenvolvimento e CRMs específicos
├── Logo-MAJB.jpg        # Identidade visual da marca (na raiz ou /src)
└── /lql                 # Diretório do cliente LQL Soluções
    └── index.html       # Iframe blindado apontando para o sistema oficial
```

## 🚀 Como Adicionar um Novo Cliente

Para integrar um novo CRM neste portal, siga o procedimento padrão da MAJB:

Criar Diretório: Crie uma nova pasta na raiz do servidor com o nome do cliente (ex: /novo_cliente).

Configurar Iframe: Copie o ficheiro index.html do Iframe blindado para a nova pasta e atualize o src com o link de Produção do Google Apps Script.

Ajustar Visual: Aplique o recuo de -28px no CSS do Iframe para ocultar o banner nativo do Google.

Atualizar Capa: Adicione um novo "Cartão de Acesso" no index.html principal apontando para a nova rota.

## 🛡️ Ambientes e Ciclo de Vida

Produção: Acedido via majb.online.

Homologação: Testes realizados via subdomínio homologacao.majb.online com base de dados isolada para garantir a segurança dos dados reais.

"Tudo o que fizerem, façam de todo o coração, como para o Senhor." - Colossenses 3:23

Desenvolvido por Gerson Bernardo da Silva - MAJB Sistemas.
