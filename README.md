# Protetor de documentos

Protótipo para encontrar e remover dados pessoais (LGPD) em vários arquivos de uma vez. A ferramenta sugere, a pessoa decide: cada dado sensível tem botões **Remover** e **Manter**, separados por arquivo.

**Tudo roda no navegador.** Nenhum arquivo é enviado a servidores. Os dados dos exemplos são fictícios.

## Recursos

- PDF, Word (.docx), Excel (.xlsx, .xls, .csv), PowerPoint (.pptx), e-mail (.eml) e texto (.txt), até 100 arquivos por vez
- Detecta CPF (com validação dos dígitos), RG, telefone, e-mail, CEP, nº de contrato, endereço e nomes
- Lista de dados por arquivo, com trecho de contexto, confiança e origem da sugestão
- Marcação manual de termos não detectados
- Download em ZIP: textos protegidos + registro CSV por arquivo (tipo e local, nunca o valor removido)

## Acessibilidade

- Navegação completa por teclado, link "Pular para o conteúdo", regiões e tabelas rotuladas
- Anúncios por `aria-live` e botões com `aria-pressed` (testar com NVDA, JAWS, VoiceOver, TalkBack)
- Ajuste de tamanho do texto, alto contraste, tema escuro, respeito a "reduzir movimento"
- Libras com o widget [VLibras](https://www.gov.br/governodigital/pt-br/vlibras), carregado de `vlibras.gov.br`

## Como usar

Abra `index.html` no navegador ou publique com GitHub Pages:
**Settings → Pages → Deploy from a branch → `main` / `(root)`**.

Requer internet para carregar JSZip, SheetJS e PDF.js (cdnjs), a fonte Atkinson Hyperlegible (Google Fonts) e o VLibras.

## Limitações

- PDFs digitalizados precisam de OCR (não incluído)
- A formatação original não é preservada: a saída é texto (.txt)
- Nomes e endereços usam um modelo de contexto simulado; revise sempre
