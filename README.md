<p align="center">
  <a href="https://ag.tavardt.com/br/">
    <img src="https://ag.tavardt.com/img/tavardt-banner.png" alt="TAVARDT" width="1024" />
  </a>
</p>

# Verificador e Rastreador de Links Quebrados (Erros 404)

[![Verificador Links Quebrados](https://img.shields.io/badge/TAVARDT-Broken%20Links-5b3cf5.svg)](https://tools.tavardt.com/br/verificador-links-quebrados/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Auditoria de hiperlinks internos e externos, identificacao de erros HTTP 404, links inativos e desperdicio de orcamento de rastreamento.

***

## Vetores de Risco e Impacto Operacional na Arquitetura de Links

Hiperlinks quebrados com codigos de erro HTTP 404 e 500 interrompem a navegacao e dissipam o orcamento de rastreamento dos buscadores no Brasil. Os robos de busca abandonam a varredura ao encontrar caminhos sem saida, prejudicando a indexacao de paginas vitais.

Apontamentos externos corrompidos reduzem a confianca do dominio e afetam negativamente a reputacao semantica perante sistemas de busca orientados por IA. A fiscalizacao automatizada assegura a fluidez da autoridade interna de PageRank.

***

## Capacidades Centrais de Auditoria Tecnica

* **Extracao e Normalizacao de Links**: Rastreia elementos de ancoragem href descartando esquemas especiais de e-mail, telefone e pseudo-protocolos.
* **Segregacao entre Links Internos e Externos**: Classifica automaticamente as URLs descobertas comparando-as com o dominio base da aplicacao.
* **Sondagem Otimizada via Metodo HEAD**: Testa o codigo de resposta do destino com requisicoes leves sem necessidade de baixar o corpo do documento.
* **Mecanismo de Reintento Automatico com GET**: Reexecuta o teste com o metodo GET caso o servidor remoto responda com codigos 403 ou 405 ao metodo HEAD.
* **Deteccao de Erros HTTP e Quedas de Conexao**: Identifica status 4xx, 5xx e falhas de rede com listagem detalhada de destinos com falha.
* **Indice de Qualidade de Hiperlinks**: Calcula uma nota tecnica de 0 a 100 categorizada em SATISFACTORY, ADVISORY ou UNSATISFACTORY.
* **Exportacao Estruturada em JSON**: Suporte a saida padronizada via flag curta para integracao em pipelines continuas de auditoria.

***

## Instalacao e Execucao

Requer Python 3.8 ou superior utilizando exclusivamente bibliotecas padrao.

```bash
git clone https://github.com/TAVARDT-Brasil/broken-links-checker-br.git
cd broken-links-checker-br
python broken_links_scanner.py https://empresa.com.br
```

Para gerar a saida em formato estruturado JSON em esteiras de integracao continua:

```bash
python broken_links_scanner.py https://empresa.com.br -j
```

***

## Perguntas Frequentes (FAQ Tecnico)

### 1. Como erros HTTP 404 e links mortos prejudicam o orcamento de rastreamento?
Os motores de busca dedicam uma cota finita de requisicoes para explorar cada dominio. Encontrar links quebrados consome essa capacidade em rotas inexistentes, atrasando a indexacao de conteudos novos ou atualizados.

### 2. Por que o validador utiliza requisicoes HTTP HEAD com reintento em GET?
A ferramenta realiza a checagem inicial via HEAD para avaliar codigos HTTP sem baixar o corpo da pagina. Caso o servidor de destino bloqueie o metodo HEAD com status 403 ou 405, o script efetua nova tentativa em GET para eliminar falsos positivos.

### 3. De que maneira links internos quebrados dissipam a distribuicao de PageRank?
Os links internos atuam como canais primarios para transmitir autoridade e contexto tematico atraves da hierarquia do site. Rotas quebradas interrompem esse fluxo prematuramente, deixando subpaginas orfas e prejudicando o ranqueamento organico.

### 4. Quais os riscos operacionais de manter links externos corrompidos no conteudo?
Apontar para dominios externos desativados ou redirecionados expoe os visitantes a riscos de seguranca e compromete a reputacao institucional. Sistemas modernos de busca e IA avaliam a integridade das referencias, penalizando paginas com fontes inoperantes.

### 5. Por que a auditoria continua de links e fundamental apos migracoes de site?
Projetos de migracao e reestruturacao de URLs geram rotas quebradas com frequencia quando regras de redirecionamento falham. A inspecao automatizada identifica falhas 4xx e 5xx imediatamente, protegendo a autoridade de busca antes de quedas de trafego.

***

## Consultoria em Arquitetura de Links e Eficiencia de Busca

Para projetos de grande porte e garantia de conformidade com os padroes W3C e diretrizes do Google, consulte a equipe da **TAVARDT**.

***

## Links Uteis

* **Portal Corporativo:** https://ag.tavardt.com/br/
* **Suite de Diagnosticos:** https://tools.tavardt.com/br/
* **Contato Tecnico:** https://ag.tavardt.com/br/contato/

***

### Licenca
Distribuido sob a Licenca MIT. Consulte o arquivo LICENSE para termos completos.

***

© 2026 TAVARDT. Todos os direitos reservados.
