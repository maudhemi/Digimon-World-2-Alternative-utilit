# Painel Digimon — APK Android

Projeto Capacitor que empacota o app (www/index.html) num APK.
A compilação roda no GitHub Actions, então não precisa de Android Studio.

## Gerar o APK (uma vez)
1. Crie uma conta gratuita em github.com e um repositório novo (pode ser privado).
2. Envie TODO o conteúdo desta pasta para o repositório, incluindo a pasta oculta `.github`.
   Dica: se o envio pelo navegador ignorar `.github`, use "Add file > Create new file",
   digite `.github/workflows/build-apk.yml` como nome e cole o conteúdo do arquivo.
3. Abra a aba **Actions**, escolha **Gerar APK** e clique em **Run workflow**.
   (Ela também roda sozinha a cada envio.)
4. Quando ficar verde (uns 5 a 10 minutos), abra a execução e baixe **painel-digimon-apk**
   em "Artifacts". Dentro do zip está o `app-debug.apk`.

## Instalar no celular
1. Passe o `app-debug.apk` para o Android (cabo, Drive, WhatsApp...).
2. Abra o arquivo e permita "Instalar apps desconhecidos" quando o Android pedir.
3. Instale e abra "Painel Digimon".

## Atualizar o app
Troque `www/index.html` pela versão nova, envie ao repositório e rode o workflow de novo.

## Observações
- É um APK de depuração (assinado com a chave de debug): serve para uso próprio.
  Para a Google Play seria preciso um APK/AAB de release assinado com sua chave.
- Ícone e tela de abertura são os padrão do Capacitor. Dá para trocar com @capacitor/assets.
- O botão "Baixar planilha base" abre o Google Sheets no navegador.
