<h1 align="center">pihole-blocklists</h1>

<p align="center">
  <b>Listes de blocage DNS pour Pi-hole, construites à partir de rapports de threat intelligence publics</b>
</p>

<p align="center">
  <a href="https://github.com/Matt-uSk/pihole-blocklists/stargazers"><img src="https://img.shields.io/github/stars/Matt-uSk/pihole-blocklists?label=%C3%89toiles&color=f5a623&logo=github&logoColor=white" alt="Stars"></a>
  <a href="https://github.com/Matt-uSk/pihole-blocklists/commits/main"><img src="https://img.shields.io/github/last-commit/Matt-uSk/pihole-blocklists?label=Mise%20%C3%A0%20jour&color=2ea44f" alt="Last commit"></a>
  <a href="#utilisation"><img src="https://img.shields.io/badge/Pi--hole-compatible-96060C?logo=pihole&logoColor=white" alt="Pi-hole"></a>
  <a href="https://ko-fi.com/mattusk"><img src="https://img.shields.io/badge/Ko--fi-Offrir%20un%20caf%C3%A9-FF5E5B?logo=ko-fi&logoColor=white" alt="Ko-fi"></a>
</p>

## Listes

| Liste | Contenu | URL à ajouter dans Pi-hole (Adlists) |
|---|---|---|
| `darksword/domains.txt` | Domaines d'exploit, C2 et hôtes iframe du kit d'exploitation iOS DarkSword et de sa variante P7 (230 domaines) | `https://raw.githubusercontent.com/Matt-uSk/pihole-blocklists/main/darksword/domains.txt` |
| `darksword/ips.txt` | Adresses IP de la même infrastructure, à bloquer au pare-feu (non utilisable par Pi-hole) | — |

## Source

- iVerify Threat Intelligence — *Sleep, Beacon, Steal, Repeat - The Story of P7 DarkSword Variant* (8 octobre 2026)
  https://www.iverify.com/blog/darksword-variant-threat-research

## Notes

- Les domaines parents dédiés à l'attaquant sont ajoutés en plus des sous-domaines observés.
- Les plateformes mutualisées (azurewebsites.net, pages.dev, qzz.io, dpdns.org, eu.cc, 8s.lv, st2.al) ne sont **pas** bloquées en entier : seuls les sous-domaines malveillants exacts sont listés.
- `bauking.ch` figure dans les C2 du rapport ; il pourrait s'agir d'un site légitime compromis.

## Utilisation

Pi-hole → *Adlists* → coller l'URL raw → puis `pihole -g` (ou *Update Gravity*).

## Soutenir le projet

Ce projet est gratuit. S'il te rend service, tu peux m'offrir un café sur **[Ko-fi](https://ko-fi.com/mattusk)** ☕ — merci !
