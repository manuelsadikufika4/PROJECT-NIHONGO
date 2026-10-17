<div align="center">

# 日本語の道 · Nihongo Michi

**Aprende japonês por níveis, com cultura, furigana, pronúncia e quizzes. 100% offline.**

[![Build APK](https://github.com/SEU_USUARIO/nihongo-michi/actions/workflows/build.yml/badge.svg)](https://github.com/SEU_USUARIO/nihongo-michi/actions/workflows/build.yml)
![Plataforma](https://img.shields.io/badge/Plataforma-Android-3DDC84?logo=android&logoColor=white)
![Capacitor](https://img.shields.io/badge/Capacitor-6-119EFF?logo=capacitor&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Offline](https://img.shields.io/badge/Funciona-Offline-2e7d4f)
![Idioma](https://img.shields.io/badge/Ensina-日本語-c8372d)
![Licença](https://img.shields.io/badge/Licen%C3%A7a-MIT-blue)
![Status](https://img.shields.io/badge/Status-MVP-orange)

</div>

---

## Sobre

O **Nihongo Michi** ("O caminho do japonês") é uma app para aprender japonês de forma simples e progressiva. Não precisa de servidor nem de base de dados: as aulas já vêm dentro da app e o progresso fica guardado no telemóvel.

## Funcionalidades

- **Onboarding:** ecrã inicial animado e pergunta "Como te chamas?", com o nome guardado localmente.
- **Dashboard:** saudação, pontos totais, ranking e módulos.
- **3 módulos por nível:** Básico (N5), Intermediário (N4) e Avançado (N3). Cada módulo só abre depois de concluíres o anterior.
- **Aulas completas:**
  - Título e contexto cultural (por que os japoneses se curvam, etc.)
  - Frase em japonês com **furigana**, romaji e tradução
  - **Pronúncia** em áudio (voz japonesa do dispositivo)
  - Pergunta final que vale nota
- **Pontuação e ranking:** guardados no dispositivo.
- **Tema claro e escuro** automático.
- **Funciona offline.**

## Sistema de pontos

| Regra | Valor |
|-------|-------|
| Pergunta certa à primeira | **10 pontos** |
| Pergunta certa depois de errar | 0 pontos (a aula conta como feita) |
| Nota do módulo | Soma das aulas do módulo |
| Ranking | Média da percentagem de todos os módulos |

## Tecnologias

- **HTML, CSS e JavaScript** puros, num único ficheiro, sem frameworks
- **[Capacitor](https://capacitorjs.com/)** para empacotar a app como APK Android
- **[GitHub Actions](https://github.com/features/actions)** para compilar o APK na nuvem
- **[Bootstrap Icons](https://icons.getbootstrap.com/)** como SVG embutido
- **`localStorage`** para guardar nome e progresso
- **Web Speech API** para a pronúncia

## Estrutura do projeto

```
nihongo-michi/
├── .github/
│   └── workflows/
│       └── build.yml          # Compila o APK automaticamente
├── www/
│   └── index.html             # A app completa
├── capacitor.config.json      # Configuração do Capacitor
├── package.json
├── LICENSE
└── README.md
```

## Como testar no navegador

1. Faz download ou clona o repositório.
2. Abre o ficheiro `www/index.html` no navegador.

Não é preciso instalar nada.

## Como gerar o APK (via GitHub)

1. Faz push do projeto para o teu repositório.
2. Abre o separador **Actions** e espera a build **Build APK** terminar (3 a 6 minutos).
   Se não arrancar sozinha, clica em **Run workflow**.
3. Quando aparecer o visto verde, abre a execução e, em **Artifacts**, descarrega **nihongo-apk**.
4. Descompacta o ZIP e instala o `app-debug.apk` no telemóvel.
   O Android pode pedir para permitir a instalação de fontes desconhecidas.

> O APK `debug` serve para testes. Para publicar na Play Store é preciso gerar uma versão `release` assinada.

## Como adicionar novas aulas

Dentro de `www/index.html`, procura a constante `AULAS` e acrescenta um objeto à lista `aulas` do módulo pretendido:

```js
{
  id: "1.5",
  titulo: "Sayonara – Adeus",
  cultura: "Texto sobre a cultura japonesa relacionada com a aula.",
  jp: "さようなら",                     // aceita <ruby>漢字<rt>かんじ</rt></ruby> para furigana
  rm: "sa-yo-u-na-ra",
  tr: "Adeus",
  p: "Como se diz «Adeus»?",
  o: ["Ohayou", "Sayonara", "Arigatou"],  // opções
  c: 1                                    // posição da opção correta (começa em 0)
}
```

## Roadmap

- [x] Onboarding com nome guardado localmente
- [x] Dashboard com módulos e ranking
- [x] Aulas com cultura, furigana, romaji e pronúncia
- [x] Quiz com pontuação
- [x] Build automática do APK
- [ ] Mais aulas por módulo
- [ ] Áudios gravados por falantes nativos
- [ ] Ícone personalizado da app
- [ ] Exercícios de escrita (hiragana e katakana)
- [ ] Revisão espaçada
- [ ] Versão release para a Play Store

## Autor

**Manuel Sadi Kufika**

## Licença

Distribuído sob a licença **MIT**. Vê o ficheiro [LICENSE](LICENSE).

Ícones por [Bootstrap Icons](https://icons.getbootstrap.com/) (MIT).

---

<div align="center">

Feito por Manuel Sadi Kufika · がんばって！

</div>
