---
# try also 'default' to start simple
theme: vuetiful
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev

# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  initial thoughts about how we will use Vue and other frontend stuff compared to our old approachin rails
layout: intro
---

# Welcome to Vue

## Points we will be discussing

- **TS vs JS**
- **Vue** (2 vs 3)
- **Vite vs VueCLI vs Nuxt**
- **Usage of Tailwindcss vs Bootstrap**
- **scss vs css**
- **Netlify vs AWS Amplify**

<!--
Table of contents
-->

---

# [TS](https://www.typescriptlang.org/)

<br>

## Pros

- Superset of JS
- Less error prone code
  - Type Checking
  - Advanced tooling when coding and building project (literally build step)
  - Adds predictability to JS
- Can nicely remove rudamentary unit tests from needing to be written ie verify input/output types

---

# [TS](https://www.typescriptlang.org/)

<br>

## Cons

- adds a lot more code depending how typescripty you make it be
- another thing to learn
- complicates component building
- slows down initial coding
- another thing to loearn that is rapidly changing

---

# [TS](https://www.typescriptlang.org/)

<br>

## Conclusion

I think for the time being that we should avoid using Typescript, its something that has too many unknowns for the team at the moment
we should circle back to it being a possibility depending on how things go with the project, fairly easy to move to typescript comparing to removing it

<br>
<br>

**Thoughts?**

---

# [Vue 3](https://v3.vuejs.org/)

- it's the newest version of Vue
- v3.2 has been released and is even faster, stable and easier to work with the v3
- best support for composition API and "future syntax"
- it's mature enough and getting rapid fast support for bugs and features
- infinitely better TS support/tooling if we decide to go down that path
- component library support is not there yet but I am not sure we should bother with them

<br>

Nothing much to say here, I think it is fairly straight forward at this point to go Vue 3

---

# Why [Vite](https://vitejs.dev/) over [Vue-cli](https://cli.vuejs.org/)

- blazing fast as it is built on esbuild whereas Vue-cli is built using webpack
- uses more modern browser ways of loading/importing/building
- much more simpler than webpack based projects
- has a lot of builtin functionality and has an extensable framework

---

# Why [Vue-cli](https://cli.vuejs.org/) over [Vite](https://vitejs.dev/)

- More Mature than Vite, which is fairly new
- Has a variety of plugins which make it extensable which are easily installed
- lots of support online for webpack
- supports older browsers

---

# [Vite](https://vitejs.dev/) vs [Vue-cli](https://cli.vuejs.org/)

**Conclusion**

Did not really bring up nuxt as V3 which supports Vue 3 does not exist yet. It will not be ready for a long time (2022 before stable).

We can easily switch between Vite and either Vue cli or nuxt very easily and less so the other way around.

I want to keep things as flexible as possible starting out so we can learn what works best for the team.

---

# Why [Tailwindcss](https://tailwindcss.com/) over [Bootstrap](https://getbootstrap.com/)

- utility based api
- provides tools to create what we want not what the framework wants
- extensive support and documentation
- extensiable ie add your own colours, variables etc and utilities are auto generated from them
- no JS allows us to use Vue very easily to customize behaviour
- the one caveat is that all the systems bootstrap has would need ot be manually created but things like headlessUI help with that
- tailwindUI is something we can pay for that will create out of the box components built with tailwind that we can more easily manipulate to our needs

---

# [SCSS](https://sass-lang.com/) vs [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)

- the differences between the 2 are so small at this point that the only real difference is that you can do nested state css in SCSS
- css has variables
- going to use tailwind anyways which has things like hover utilities builtin

<br>

Hard to see the point in SCSS these days but we can if it makes people more comfortable

---

# [Netlify](https://www.netlify.com/) vs [AWS Amplify](https://aws.amazon.com/amplify/)

I really like netlify over AWS but it really comes down to things like domain management, pricing and possibly intgrating with other AWS based stuff

- netlify is easier to use and is more developer friendly from the point of docs and OOB functionality
- amplify is integrated into all of our other AWS stuff
- netlify is multi cloud and tuned for performance, does things like cache invalidation for us
- netlify will deploy your code for every branch automatically, this allows testers to easily test code for reviews and free up staging lanes
- netlify has a very extenable feature set that is easy to use where AWS i would argue is a lot more complicated
- netlify does not have transparent pricing for enterprise (which would be the ideal plan from them as its the most reliable and robust)
- can commit our assets directly and have them automagically be put into a high performance CDN, cache control is amazing
- netlify will easily have all assets globally distributed (not 100% how sure this works with AWS)

## this does not need to be deicded now but is a big decision
