---
# try also 'default' to start simple
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
fonts:
  sans: 'Avenir'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
---

# Portfolio Dev

---

# Qu'est-ce qu'un Portfolio ?

<v-click>

Un portfolio est un support de présentation qui permet de mettre en valeur les réalisations à travers lesquelles vous avez construit votre expérience

</v-click>

<v-click>

En fonction de la profession, celui-ci peut se présenter sous plusieurs formes, mais il peut aussi se composer de plusieurs documents ou sources:

</v-click>

<v-clicks>

- 💻 **Un site web**
- 🧑‍💻 **Un book**
- 📖 **Un blog**
- 📱 **Des liens vers des réseaux sociaux ou professionnels**
- 📢 **Des témoignages de clients, ou figures publiques**
- 💡 **Libre à votre imagination d'inaugurer des nouveaux formats !**

</v-clicks>

---

# Contenu du portfolio

Au minimum, un portfolio devrait contenir les points suivants:

<v-clicks>

- 💬 Une présentation personnelle, de préférence avec une photo
- 🔗 Des liens vers son travail
- 📚 Expériences et compétences
- 📩 De quoi vous contacter (formulaire de contact, coordonnées ...)

</v-clicks>

---

# Portfolio de dev

Pour les développeurs, il est toujours plus délicat de présenter son travail, puisque très souvent il ne peut pas être visualisé.

<v-click>

**Il va quand même falloir miser sur la présentation**, puisqu'elle compensera le manque de visuels que vous aurez à présenter

</v-click>

<v-click>

### Mais avant tout, que voulons nous montrer ?

</v-click>

---

# Portfolio de dev

Là où il faudra tout donner pour un portfolio de dev, c'est sur la présentation des projets.

Projets étudiants, ou personnels, contribution open-source... Tout est bon à mentionner. Mais surtout, **chaque projet doit être illustré et présenté**. Même si c'est un projet back-end sans visuel, des schémas ou des exemples d'input/output sont bons et permettent au lecteur de mieux comprendre comment fonctionne le projet. Les documentations sont des exemples parfaits.

Exemples de projets sans visuels:

- **[gitmoji-cli](https://github.com/carloscuesta/gitmoji-cli)**
- **[igdm-cli](https://github.com/noook/igdm-cli)**
- **[vue-composition-paginate](https://github.com/noook/vue-composition-paginate)**

---

# Outils

- **[Adobe portfolio](https://portfolio.adobe.com/)**
- **[Wordpress](https://wordpress.org/)**
- **A la main 😁** (HTML, CSS, JS?) ou éventuellement avec un framework comme
  - **[Gatsby.js](https://www.gatsbyjs.com/)** (React)
  - **[Next.js](https://nextjs.org/)** (React)
  - **[Nuxt.js](https://nuxtjs.org/)** (Vue)
- **[A partir de templates HTML & CSS](https://bashooka.com/html/free-html-css-portfolio-web-design-templates/)**

---

## Adobe Portfolio

Adobe Portfolio est un outil de la suite Adobe **payant** mais qui est inclus dans la suite Creative Cloud. Il est utilisé à la façon d'un [CMS](https://en.wikipedia.org/wiki/Content_management_system) (Content Management System), c'est à dire que la partie contenu est dissociée de la partie présentation.

_Lorsque vous initiez un projet Adobe Portfolio, vous avez le choix du thème, mais pas de panique, si vous voulez changer de thème, normalement vous pouvez sans risque. Le thème décide juste de la façon dont le contenu va être présenté._

<small class="text-xs">Je ne suis pas sûr du point au dessus, je n'ai malheureusement plus de licence pour vérifier :(</small>

Un thème efficace est Martha, il met à disposition une série de liens dans la navbar pour rediriger vers les réseaux sociaux, et dispose aussi d'un système de _cartes_ pour présenter ses projets. Une page = un projet, et on peut le décrire, l'illustrer, mettre des liens...

---

## Wordpress(.org)

Un outil relativement facile à prendre en main, mais moins facile à mettre en ligne et maintenir.

Il requiert aussi une installation d'une stack **PHP** avec une base de données et **un serveur web en amont** (nginx, ou Apache par exemple). Vous pouvez très bien monter votre portfolio sur votre stack locale, ou **directement sur votre serveur distant** où sera déployé le portfolio. Le plus simple reste quand même de le faire directement sur le serveur distant mais il faut déjà avoir toute la configuration de prête.

Wordpress dispose de plein d'avantages, comme celui de pouvoir **utiliser des templates créés par la communauté**, mais surtout, tous les outils sont déjà à votre disposition si vous voulez rajouter une **section blog** à votre portfolio.

---

## Intégration à la main

Là, pas de surprise, **mais de la sueur** surtout si c'est votre premier portfolio puisqu'il faudra **partir de 0**.

Libre à vous de faire quelque chose de simple, et de vous servir de petites librairies rajoutant quelques effets <span class="animate-ping">***\*waouh\****</span> (comme [particles.js](https://vincentgarreau.com/particles.js/) par exemple) ou d'utiliser un framework qui vous propose déjà des structures de pages en mode SPA (Single Page App) avec génération de contenu statique à la fin <span class="text-sm">(ça a l'air compliqué.)</span>

Mais ça reste toute de même possible. Les liens vers les frameworks en dessous proposent de quoi créer une SPA pas trop lourde (**et statique**) pour pouvoir la déployer derrière gratuitement sur des services de déploiement automatisé (on y vient après)

- **[Nuxt.js](https://nuxtjs.org/)** (Vue, in static mode not SSR)
- **[Gatsby.js](https://www.gatsbyjs.com/)** (React)
- **[Next.js](https://nextjs.org/)** (React)

---

# Déploiement

Pour les sites statiques (= pas de back-end pour rappel), des outils gratuits permettent de le déployer, et même d'y lier son nom de domaine.

- **[Netlify](https://www.netlify.com/)** (ces slides sont hebergées ici :D)
- **[Vercel](https://vercel.com/)**

Il en existe d'autres mais ces plateformes sont les plus connues.

Pour du déploiement non statique, nous pouvons utiliser **[Heroku](https://www.heroku.com/)**. Pour qu'il soit gratuit, il faut une contrepartie: les *dynos* (= instances) dorment après un moment d'inactivité, c'est à dire que la première visite après une période d'inactivité va rallumer le serveur et la requête risque d'être plus longue.

---

# Ressources

- **[Carlos Cuesta](https://carloscuesta.me)** - Front End Developer
- **[Victor Garcia](https://vicflix.me/)** - Front End Developer
- **[Bruno Simon](https://bruno-simon.com/)** - Front End Developer
- **[Anthony Fu](https://antfu.me/)** - Vue.js core team, and lots of open source projects
- **[Evan You](https://evanyou.me/)** - Vue.js creator
- **[Abel Derderian](https://abel.fr/)** - Front-End Developer
- **[Ismaël Bah](https://portfolio-isbah.vercel.app/)** - Dev 2023
- **[Neil Richter](https://nook.sh)** - Fullstack Developer
- **[Ulysse Asso'o Emane](https://www.ulysse-asso-o.fr/)** - Dev 2023
- **[Ivan Milosevic](https://alvai.dev/)** - Dev 2020
- **[Eduardo San Morote](https://esm.dev/)** - Vue.js core team
- **[Guillaume Chau](https://guillaume-chau.info/)** - Vue.js core team

➡️ **[Awesome Portfolios](https://github.com/amnashanwar/awesome-portfolios)** - Curated list of portfolios

<style>
.slidev-layout li {
  line-height: 1.6em;
}
</style>

