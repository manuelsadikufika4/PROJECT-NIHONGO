# Como contribuir · 貢献する方法

Obrigado por quereres ajudar o **Nihongo Michi** (日本語の道)! 🎌
Toda a ajuda é bem-vinda: aulas novas, correções de japonês, melhorias no código, design, testes e ideias.

## Formas de contribuir

- **Criar aulas novas** para os módulos Básico (N5), Intermediário (N4) e Avançado (N3)
- **Corrigir erros** de japonês, furigana, romaji ou tradução
- **Rever textos culturais** para garantir que estão corretos e respeitosos
- **Reportar bugs** ou sugerir funcionalidades através das [Issues](../../issues)
- **Melhorar o código**, o design ou a acessibilidade da app
- **Ajudar com o Roadmap**: ícone da app, exercícios de hiragana/katakana, revisão espaçada, áudios de falantes nativos

## Primeiros passos

1. Faz **Fork** do repositório.
2. Clona o teu fork:
   ```bash
   git clone https://github.com/manuelsadikufika4/PROJECT-NIHONGO.git
   cd PROJECT-NIHONGO
   ```
3. Cria uma branch para a tua alteração:
   ```bash
   git checkout -b tipo/descricao-curta
   ```
   Exemplos: `aula/sayonara`, `fix/furigana-aula-2-3`, `feat/ranking`.
4. Abre `www/index.html` no navegador para testar. Não é preciso instalar nada.

## Adicionar uma aula nova

As aulas ficam em `www/index.html`, na constante `AULAS`. Acrescenta um objeto à lista `aulas` do módulo pretendido:

```js
{
  id: "1.5",
  titulo: "Sayonara – Adeus",
  cultura: "Texto sobre a cultura japonesa relacionada com a aula.",
  jp: "さようなら",            // aceita <ruby>漢字<rt>かんじ</rt></ruby> para furigana
  rm: "sa-yo-u-na-ra",
  tr: "Adeus",
  p: "Como se diz «Adeus»?",
  o: ["Ohayou", "Sayonara", "Arigatou"],
  c: 1                          // posição da opção correta (começa em 0)
}
```

**Checklist para aulas:**

- [ ] O `id` é único e segue a sequência do módulo
- [ ] O japonês está correto (hiragana, katakana, kanji)
- [ ] O furigana e o romaji correspondem à frase
- [ ] A tradução está em português
- [ ] O texto cultural é curto, factual e respeitoso
- [ ] Há uma única resposta correta e `c` aponta para ela
- [ ] Testei a aula no navegador, incluindo a pronúncia

## Padrões de código

- O projeto usa **HTML, CSS e JavaScript puros**, sem frameworks.
- Mantém a app **100% offline**: não adiciones dependências externas nem pedidos de rede.
- Segue o estilo do código existente (indentação, nomes e comentários).
- Garante que funciona nos **temas claro e escuro**.
- Mantém a app leve e usável em telemóveis Android.

## Mensagens de commit

Usa mensagens curtas e claras, no imperativo:

```
Adiciona aula "Sayonara" ao módulo 1
Corrige furigana na aula 2.3
Melhora contraste no tema escuro
```

## Enviar um Pull Request

1. Faz push da tua branch para o teu fork.
2. Abre um **Pull Request** para a branch `main`.
3. Descreve o que mudou e porquê. Se for visual, junta uma captura de ecrã.
4. Espera pela revisão. Podem ser pedidos ajustes.

Mantém cada PR **pequeno e focado** numa só coisa. Assim é mais rápido de rever.

## Reportar bugs e sugerir ideias

Abre uma [Issue](../../issues) e inclui:

- O que aconteceu e o que esperavas que acontecesse
- Passos para reproduzir
- Dispositivo, versão do Android ou navegador
- Capturas de ecrã, se ajudarem

## Código de conduta

Sê respeitoso e acolhedor. O projeto é para quem está a aprender, por isso:

- Trata todos com cortesia, seja qual for o nível de japonês ou de programação
- Dá feedback construtivo e aceita-o com abertura
- Não toleramos assédio, discriminação nem linguagem ofensiva

## Licença

Ao contribuíres, aceitas que o teu trabalho seja distribuído sob a licença [MIT](LICENSE) do projeto.

---

ありがとうございます！ がんばって！
