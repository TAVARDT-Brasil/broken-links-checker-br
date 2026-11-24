# Verificador e Rastreador de Links Quebrados (Erros 404)

[![Verificador Links Quebrados](https://img.shields.io/badge/TAVARDT-Broken%20Links-5b3cf5.svg)](https://tools.tavardt.com/br/verificador-links-quebrados/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Auditoria automatizada de hiperligacoes internas e externas, mapeamento de codigos de resposta HTTP e prevencao de perda de autoridade de busca.

Desenvolvido e mantido pela divisao de rastreamento e arquitetura de dados da **TAVARDT Brasil**.

***

## Capacidades de Auditoria de Links e Erros 404

* **Rastreamento de Hiperligacoes Internas e Externas**: Extracao exaustiva de tags de ancoragem (`<a href>`), validando status de conexao e integridade estrutural.
* **Mapeamento de Codigos de Erro HTTP**: Identificacao imediata de falhas de cliente (404 Not Found, 403 Forbidden, 410 Gone) e indisponibilidades de servidor (500, 502, 503).
* **Auditoria de Links Quebrados com Fragmentos**: Validacao de ancoras internas com hash (`#secao`) para garantir destino existente na pagina.
* **Preservacao de Crawl Budget e Equidade de PageRank**: Deteccao de caminhos truncados que geram desperdicio de varredura por motores de busca.
* **Indice de Integridade de Links**: Pontuacao tecnica quantitativa de 0 a 100 com listagem priorizada de URLs com falha.

***

## Instalacao e Execucao

Requer Python 3.8 ou superior sem necessidade de pacotes externos adicionais.

```bash
git clone https://github.com/TAVARDT-Brasil/broken-links-checker-br.git
cd broken-links-checker-br
python broken_links_scanner.py https://empresa.com.br
```

Para gerar relatorio estruturado em formato JSON:

```bash
python broken_links_scanner.py https://empresa.com.br -json
```

***

## Diagnostico Completo na Web

Para varredura completa de links em massa e inspecao em tempo real:

* **Verificador de Links Quebrados Oficial**
* **[Portal Corporativo TAVARDT Brasil](https://ag.tavardt.com/br/)**

***

## Consultoria em Arquitetura de Links e SEO Tecnico

Para saneamento de arquitetura de URLs e conformidade com Diretrizes de Qualidade Google Search Central e W3C URI Guidelines, contate os especialistas da **TAVARDT Brasil**.

***

© 2026 TAVARDT. Todos os direitos reservados.
