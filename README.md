# Sistema de Anamnese Veterinária — Jéssica Rezende

Protótipo local de ficha de anamnese e avaliação fisioterápica veterinária, desenvolvido para uso em notebook ou tablet. A interface foi pensada para toque e baseada na ficha de referência da Jéssica Rezende.

> **Estado do projeto:** protótipo para testes e validação. Não é um sistema clínico de produção nem oferece sincronização entre dispositivos.

## Funcionalidades

- Cadastro e edição de tutores e animais.
- Foto do animal, escolhida da galeria ou capturada pela câmera quando o dispositivo oferece essa opção. A imagem é reduzida no próprio navegador.
- Anamnese organizada nas 12 seções da ficha:
  1. Identificação do paciente
  2. Identificação do tutor
  3. Queixa principal
  4. Histórico da alteração atual
  5. Histórico clínico
  6. Dor
  7. Avaliação funcional
  8. Rotina e ambiente
  9. Avaliação fisioterápica
  10. Objetivos da reabilitação
  11. Plano terapêutico
  12. Evolução
- Assinatura desenhada na tela.
- Histórico de fichas e busca por animal ou tutor.
- Impressão da ficha completa ou salvamento em PDF pelo navegador.
- Exportação e restauração de backup em JSON.
- Acesso local com senha básica.

## Tecnologias

- HTML
- CSS
- JavaScript
- IndexedDB para registros, cadastros, fotos e assinaturas no navegador

O protótipo não depende de servidor, banco de dados remoto ou conexão com a internet para o fluxo local.

## Como executar

### Opção recomendada: arquivo único

1. Baixe o arquivo `Anamnese-Jessica-Local.html` deste repositório.
2. Abra-o no Chrome ou Edge. No Android, use o gerenciador de arquivos e escolha o navegador, evitando a prévia do próprio gerenciador.
3. Na primeira abertura, defina uma senha local com pelo menos seis caracteres.
4. Cadastre tutor e animal, crie uma ficha e salve.

O arquivo único já contém o HTML, o CSS e o JavaScript; não precisa dos arquivos auxiliares.

### Arquivos separados para desenvolvimento

O projeto também inclui `index.html`, `styles.css` e `app.js`. Mantenha os três na mesma pasta e abra `index.html` em um navegador compatível.

O suporte a IndexedDB para páginas abertas diretamente como arquivo local pode variar conforme o navegador e o dispositivo. Faça um cadastro de teste e reabra a página para confirmar que os dados foram mantidos.


## Armazenamento e segurança

- Os registros ficam no IndexedDB do perfil do navegador usado naquele dispositivo. Eles não são sincronizados automaticamente com outros navegadores ou dispositivos.
- A senha local é uma barreira básica na interface; ela não criptografa os registros. Uma pessoa com acesso ao perfil do navegador pode potencialmente contornar a tela de login ou apagar os dados.
- Limpar os dados do navegador, reinstalá-lo, trocar de perfil ou perder o dispositivo pode causar perda dos registros. Mantenha backups atualizados.
- A imagem de assinatura é capturada no dispositivo. Isso, por si só, não comprova a identidade do signatário nem garante validade jurídica.
- Não use dados reais de clientes ou pacientes em uma versão publicada sem avaliar os requisitos de privacidade, segurança e consentimento aplicáveis.


## Licença

A licença ainda não foi definida. Até que uma licença seja incluída, todos os direitos permanecem reservados; não presuma autorização para redistribuir ou reutilizar o código.