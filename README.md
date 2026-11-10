# Isa Magnaboschi, Nutricionista

Página da nutricionista esportiva Isadora Magnaboschi (@nutri.isamagnaboschi, CRN-3 77635), com consultório na Vila Henrique, em Salto, SP, e atendimento on-line. Ela não tinha site; esta é a primeira versão, feita do zero.
Versão 1 (10/11/2026), conceito "a lousa do box" (ela treina CrossFit): abertura em marrom com a foto do ensaio e o "WOD de hoje" a giz, a interação "O que você não fica sem?" com as respostas reais dela no podcast, a história da salinha da academia ao espaço próprio, placar em LED com as avaliações, os rounds do acompanhamento e o consultório com horários presenciais e on-line.
HTML, CSS e JavaScript puros, sem build. Todos os botões de agendamento abrem o WhatsApp.

## Estrutura

```
index.html                 página completa (estilos, scripts e logo "isa" dentro do arquivo)
img/isa-encostada.jpg      foto da abertura (ensaio, Instagram)
img/isa-retrato.jpg        foto da negociação (enviada pelo WhatsApp)
img/isa-cafe.jpg           mosaico "Quem é" (ensaio, Instagram)
img/isa-treino.jpg         mosaico: no box de CrossFit (Instagram)
img/isa-bolotinhas.jpg     mosaico: receita das bolotinhas (quadro de vídeo do Instagram)
img/isa-perfil.jpg         consultório (foto de perfil do Instagram)
img/favicon.png            ícone da aba (logo "isa")
img/apple-touch-icon.png   ícone ao salvar na tela do celular
vercel.json                configuração da Vercel (URLs limpas)
```

## Publicar

1. Crie um repositório no GitHub (ex.: `Isa_Magnaboschi`) e envie os arquivos desta pasta para a raiz dele.
   Importante: **arraste a pasta `img` inteira** para a área de upload. O botão "choose your files" não envia pastas.
2. Na Vercel, clique em **Add New → Project**, importe o repositório e mantenha:
   - Project Name: `nutri-isamagnaboschi`
   - Framework Preset: **Other**
   - Build Command: vazio
   - Output Directory: vazio (raiz)
3. Clique em **Deploy**. O site fica em https://nutri-isamagnaboschi.vercel.app/ e cada novo commit publica a atualização sozinho.

## Imagens

Ao trocar uma imagem mantendo o mesmo nome, aumente o número `?v=1` nos links do `index.html` (por exemplo `?v=2`) para os navegadores baixarem a versão nova.
A foto das bolotinhas é um quadro de vídeo (qualidade média); se a Isa mandar fotos do ensaio em alta resolução, dá para trocar.

## Logo

O logo "isa" (o pingo do i é uma folha) está no `index.html` como texto na fonte DM Serif Display mais o símbolo `i-folha`. Os arquivos PNG para a cliente usar em outros lugares ficam fora desta pasta, em `previas/isadora-magnaboschi/logo/`.

## Editar conteúdo

- Número do WhatsApp: variável `numero` no fim do `index.html` (hoje 5511971411966) e o número exibido no rodapé.
- Mensagem padrão: atributo `data-wa` de cada botão. Ao escolher na negociação, todos os botões passam a enviar "Oi, Isa! Vim pelo site. Eu não fico sem <item> e quero agendar uma consulta."
- Respostas da negociação: objeto `ITENS` no script (pergunta, resposta e explicação de cada opção). A lousa reserva a altura da resposta mais longa para a foto não mudar de tamanho.
- Horários: tabela `.tabela` e o objeto `faixas` do "Aberto agora" no fim do script (presencial: seg, qua e sex 9h às 20h; ter e qui 8h às 16h; on-line também sábado 8h às 12h).
- Cores: variáveis no início do `<style>` (`--grafite` é o marrom da lousa, `--coral` o pêssego, `--blush`, `--nude`, `--salvia`).
- Se o endereço final do site mudar, atualize `og:url`, `og:image` e `canonical` no `<head>`.

## A confirmar com a cliente

- Se trabalha com consulta e acompanhamentos de 90 e 180 dias (o conteúdo de cada round vem do que ela contou no podcast).
- Se aprova citar a Adefis e o podcast "Bora Ser Fit".
- Se aprova o logo "isa" criado para o site.
- Fotos do ensaio em alta resolução, se tiver.
