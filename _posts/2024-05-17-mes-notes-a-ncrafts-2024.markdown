---
layout: post
title:  "notes NewCrafts 2024"
date:   2024-05-17 15:22 +0100
categories: craft notes
---

## Jour 1

### Patrick Debois - From Pilot to Transformation: Embracing the Reality of GenAI at Scale

There is never just one prompt—flow is everywhere, and it depends on the models. Open-source alternatives, such as those from @huggingface, offer flexibility, and bigger is not always better or cheaper. This applies to prompts, models, and hardware alike. Techniques like quantization, for instance, help reduce the size of LLMs without sacrificing too much performance.

On political concerns, LLMs remain biased, though opt-out mechanisms exist to prevent data from being scraped. Understanding how and where knowledge is sourced is becoming more transparent thanks to SBOMs. When it comes to data strategies, "**bring your own data**" is taking shape: RAG is becoming the default approach, typically handled by engineers, while fine-tuning remains an exception, led by data specialists. Soon, both will be commoditized. The current challenge is bridging the gap between GenAI systems and datalakes, where memory resides. With the rise of agents, engineers must shift their mindset from how to what, grouping these solutions under an orchestration layer. Eventually, crafting prompts—through refactoring and model-agnostic design—will become a specialized skill.

Then comes **Act 2: delivery pipeline**, where the most exciting challenge emerges—testing. However, since LLMs are non-deterministic, traditional assertions don’t work. Instead, we need refined validation frameworks, such as checking whether generated text is optimistic or semantically close to expectations.

**Act 3: operate** focuses on monitoring, particularly costs, but also introduces new metrics like Time to First Token. Continuous quality monitoring becomes essential since pipeline tests alone are insufficient. Security, especially against prompt injections, must be reinforced. This phase also requires rethinking infrastructure, with caching mechanisms and abstractions, as well as reconsidering established practices like A/B testing, technical metrics, and end-user feedback collection.

Finally, **Act 4: business as usual** depends on cultural adoption. A shift-right approach fosters collaboration between data scientists and full-stack engineers through well-defined APIs. In the end, innovation remains an expensive endeavor.

> GenAI will never invent @ncraftsConf (as a system of thinking).

### Jessica Brentnall - Stabilising eccentric systems

Making teams enjoyable starts with reframing the way we see their work. Instead of calling old code legacy, renaming it _pre-loved_ fosters empathy for those who built it before. Sharing an ubiquitous language, especially with junior team members, helps create alignment, while shifting the focus from domain to _product_ brings clarity.

Conversations matter. Asking “_How do you use it?_” rather than just “_What is it?_” leads to a deeper understanding of real needs. Capability mapping, as suggested by Ian Cooper, can serve as a high-level preparation before diving into event storming. Understanding what truly frustrates teams is just as crucial, though opinions may vary - some argue that predictability is key, but the real priority is ensuring that teams focus on what delivers the most value, which ultimately impacts prioritization in the same way.

Communication should also include those who are not directly impacted but still interested - these peers should not be forgotten. Finally, being able to say no is a real superpower, but one that is easier to acquire than it seems.

### Trond Hjorteland - Human-centred system design

Les limites de l’approche socio-technique classique ? Ca commence déjà si on considère que le social est un système ouvert, chaotique, tandis que le système technique est fermé et prédictif. Le véritable enjeu réside donc dans l’alignement de ces deux dynamiques fondamentalement différentes.

Cette opposition rappelle le clivage entre DP1 et DP2 :
- **DP1** : système industriel, technique, autoritaire, structuré.
- **DP2** : système social, démocratique, organisation apprenante.

Le passage de l’un à l’autre est délicat, notamment parce qu’**être démocratique ne signifie pas simplement "laisser-faire"**. Sans cadre, une organisation peut sombrer dans un chaos encore plus problématique qu’un système autoritaire.

Les freins au changement
- **Difficulté de passage à l'échelle** : les expérimentations réussies se diluent dans l’organisation.
- **Motivations divergentes** : un changement durable fonctionne mieux en partant des besoins de la base.

Loin d’être des figures imposant une vision, les experts devraient plutôt aborder chaque nouvel environnement comme une feuille blanche. De plus, certaines transformations n’exigent pas forcément d’expertise extérieure : le **design participatif** peut suffire à passer de DP1 à DP2.

Néanmoins, certains workshop échouent : “_It is only when the people involved work out their own designs that the necessary motivation, responsibility and commitment to effective implementation is present_” (Merrelyn Emery).

Emery proposant plusieurs niveaux d'environnement d'organisation :

1. **placid, randomized environment** (nothing needed :-))
2. **placid, clustered environment** (tactics needed)
3. **disturbed, reactive environment** (strategy needed)
4. **turbulent field environment** (unpredictable)

Ca ressemble à du Cynefin, non ?

Une illustration nous a été donnée le lendemain matin, par Andrew Harmel-Law : “_The idea of "structurelessness" does not prevent the formation of invormal structures, only formal ones_”. “_Structurelessness then becomes a smokescreen for the strong or the lucky to establish unquestioned hegemony over others_”.

> Accepter de la fluidité dans les rôles, en parlant plus des besoins que des solutions.

## Jour 2

### Stefan Hofer - Domain Storytelling - a Practical Introduction

Une méthode pour structurer un _ubiquitous language_ en privilégiant les conversations plutôt que la documentation. Complémentaire à l’event storming, elle permet une approche plus large et exploratoire.

Dans l’animation, l’attention portée aux mots est essentielle : reformuler, dessiner en parallèle, poser des questions activantes comme « _et après ?_ » ou « _comment ?_ ». Identifier les niveaux _how_ <=> _why_ (référence à l’impact mapping) permet de structurer plusieurs niveaux de diagrammes.

L’outil *Egon.io* facilite la capture des échanges entre acteurs (individus, groupes, systèmes… voire objets physiques comme un bateau ou un conteneur), des objets de travail (documents, e-mails, données en base), et des activités (verbes, gérondifs, prépositions). Chaque interaction est transformée en phrases numérotées et animables, mettant en évidence les relations.

À noter : les objets sont recopiés dans chaque phrase (contrairement aux acteurs), et peuvent évoluer en changeant de forme (du papier à une BDD, par exemple) ou d’état.

### Andrew Harmel-Law - Power Structures and their Impact on Software

>Andrew Harmel-Law qui demande l'aide de l'assistance pour lui dire s'il sort du flow de sa keynote en annonçant le plan, c'est cool.

 Power structures depend on how knowledge is encapsulated and shared. Coupling is the act of sharing knowledge. Good architecture reduces coupling 🤯 - or rather, it finds better ways to manage it.

Code is knowledge. Code is power. (_Knowledge is power._) But code is also the **history** of knowledge, the **landscape*** we navigate, and as such, it solidifies both knowledge and power—including societal power.

Great programmers are often great because they’re not afraid to write and navigate a _big ball of mud_. But this reinforces gatekeeping, concentrating power in the hands of those who can handle the chaos. And if you remove roles, structure, and organization - hoping things will just work naturally - then unconscious cultural structures take over. And guess what? Those structures tend to serve the elites.

Three factors that lead to **unbalanced power**:

1. Control of punishment
1. Control of information
1. Individual charisma

Three freedoms that help rebalance power:
1. Freedom to reorganize (at the team level)
1. Freedom to move (through transparency, reducing gatekeeping)
1. Freedom to disobey (even against the general consensus)

**Good ending**: Anyone can make any decision, but before doing so, they must seek advice from all affected parties and those with expertise.

**Bad ending**: Reducing knowledge through LLMs will erode power balance.

> Harmel-Law me rassure, il est comme moi <3 : pas très bon à stocker de la connaissance, mais vraiment pas mauvais à accélérer son flux. (Plus une autoroute qu'un parking, cf une précédente édition :-))


### João Rosa - Leveraging Team Topologies for software evolution (workshop)

First, respect the brain - respect cognitive load - before talking tech when thinking about (re)organization. _Where does full-stack stop?_

Working with social dynamics is more about puzzle solving than problem solving. You never know what the next piece will be. Code is always code _in a context_.

Some workshops won’t work if you can’t shift into a DP2 organization, at least temporarily. Same for training.

Focus on the mess or on what’s working? It’s hard to switch between all these perspectives: open systems, closed systems, ideal future, concrete future, present, false strategies. Too much for a single workshop.

Maybe _puzzle thinking_ is the way forward.

> New things are going on team topologies

### Michel Grootjans - experiencing team flow

Je me trompais dans la définition du throughput : ce n'est pas la moyenne du temps qu'un ticket a mis à aller en prod, mais la moyenne du temps que *tous les tickets entrés dans le système* mettront pour aller en prod, l'*estimant* pour ceux qui ne sont pas encore terminés. Donc ça veut dire que si on met plus de ticket en input qu'on est capable de livrer, le throughput diverge. C'est l'intérêt du sprint planning scrum : on limite les tickets qu'on va faire rentrer dans le système, et du coup pas besoin de limiter le WIP - ce qu'il faut bien faire en Kanban. Qu'importe votre organisation, il faut trouver une manière de limiter le WIP de l'équipe pour réduire les temps d'attente, par exemple :
- en limitant le WIP du bottle neck (Kanban)
- en limitant l'input à l'entrée du système (Scrum) 
- en ayant tout le monde pouvant travailler sur toutes les tâches (plutôt dans le monde industriel) 
- Ah, et bien sûr l'ensemble programming :).

### Woody Zuill - Failure to communicate

In coding Dojos, in the beginning, the team won't be able to resolve even a simple kata in two hours, whereas every body would have finished it in 30 min alone. But as a team, the time to make people agree after the code is written would be much higher.

> Comment essayer de partager notre modèle mental avec les GenAi ?

### Laurent Bossavit - Where do bugs come from

Corriger un bug, ce n’est pas vraiment de la maintenance. C’est du rafistolage. La vraie maintenance, c’est le refactoring après la correction : remettre le code en état après l’avoir malmené en le modifiant. Une question d’entropie. Ça révèle une autre forme de dette technique : l’usure du code face aux changements, sa résistance à l’évolution (on le contrarie, on l'_upset_). 

Rappel : à côté de celle-ci, trois autres formes classiques de dette :
* L’écosystème qui bouge autour du code.
* Les erreurs involontaires.
* Les compromis délibérés : coder vite, apprendre en chemin, économiser du temps ou de l’argent.

Ainsi, plutôt que de parler de dette technique en général, mieux vaut parler de dette non gérée (_unmanaged technical debt_).