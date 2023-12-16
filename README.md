# Projeto de Infraestrutura em Contêineres - Trabalho 2 - Redes de Computadores

Este projeto visa demonstrar o uso eficiente de contêineres para a criação de uma infraestrutura completa, oferecendo uma solução versátil para ambientes empresariais. Utilizando o Docker Compose, a implementação engloba uma variedade de serviços interconectados para compartilhamento de arquivos, colaboração, streaming de mídia e mais.

## Serviços Implementados:

1. **Nextcloud:**
   - Descrição:* Plataforma robusta para compartilhamento de arquivos e colaboração.
   - Configuração:* Integrado com PostgreSQL e LibreOffice para melhor experiência do usuário.

2. **PostgreSQL (db):**
   - Descrição:* Sistema de gerenciamento de banco de dados robusto para suportar o Nextcloud.
   - Configuração:* Volume configurado para persistência de dados entre reinicializações.

3. **Adminer:**
   - Descrição:* Cliente para administração do PostgreSQL com interface web amigável.
   - Configuração:* Mapeado para acesso web e dependente do serviço PostgreSQL.

4. **Nginx:**
   - Descrição:* Servidor web e proxy reverso para Nextcloud e LibreOffice.
   - Configuração:* Utiliza arquivo `nginx.conf` específico para cada serviço.

5. **Plex:**
   - Descrição:* Servidor de mídia para streaming.
   - Configuração:* Mapeamento de portas e volumes para oferecer solução completa de streaming.

6. **LibreOffice:**
   - Descrição:* Suíte de escritório para visualização de documentos no Nextcloud.
   - Configuração:* Integrado ao Nextcloud para pré-visualização eficiente de documentos.

## Configuração e Uso:

1. **Clone o Repositório:**
   ```bash
   git clone https://github.com/kassioma/Trabalho-2---Redes-UnB.git
   cd Trabalho-2---Redes-UnB
2. **Inicialize os Contêineres:**
   ```bash
   docker-compose up -d
3. **Acesse os Serviços:**

- Nextcloud: http://localhost:8080
- Adminer: http://localhost:8081
- Plex: http://localhost:32400
- LibreOffice: http://localhost:3000

4. **Encerre os Contêineres:**
   ```bash
   docker-compose down

## Observações Importantes:

- Certifique-se de ter o Docker e o Docker Compose instalados.
- Acesse os serviços através dos URLs fornecidos após a inicialização.


##### Este projeto foi desenvolvido como parte do Trabalho 2 de Redes de Computadores da Universidade de Brasília.
