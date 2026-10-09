# pihole-blocklists

Listes de blocage DNS pour Pi-hole, construites à partir de rapports de threat intelligence publics.

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
