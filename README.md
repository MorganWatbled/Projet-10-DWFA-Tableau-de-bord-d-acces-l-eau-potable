# DWFA — Tableau de bord d'accès à l'eau potable

Mission de consulting data pour l'ONG DWFA (Drinking Water For All), visant à orienter le choix d'un pays et d'un domaine d'investissement suite à une demande de financement auprès d'un bailleur de fonds.

---

## Contexte / besoin métier

DWFA a pour ambition de donner accès à l'eau potable à tout le monde, à travers trois domaines d'expertise :
- la création de services d'accès à l'eau potable,
- la modernisation de services existants,
- le consulting auprès d'administrations/gouvernements sur les politiques d'accès à l'eau.

L'association a sollicité un financement auprès d'un bailleur de fonds sur la base de ces trois domaines. Si ce financement est accordé, il permettra d'investir dans l'un des trois domaines, dans un pays encore à déterminer.

Thibaut Renard, chef de mission, a demandé la construction d'un tableau de bord permettant d'identifier les pays rencontrant des difficultés d'accès à l'eau potable et ceux sur lesquels concentrer les efforts, à travers des indicateurs représentatifs des trois domaines d'expertise.

## Données (source, qualité, limites)

**Sources :** dataset collecté par un data engineer de DWFA, accompagné d'un dictionnaire des données ; sources complémentaires (OMS, FAO) disponibles pour approfondir certains indicateurs si nécessaire.

**Qualité :** les données ont été organisées sous forme de plusieurs tables, reliées entre elles via un **schéma en étoile**, ce qui structure clairement les indicateurs autour des dimensions d'analyse (pays, zone rurale/urbaine, genre).

**Limites :**
- Le pays cible n'étant pas encore déterminé au moment de l'analyse, le tableau de bord reste construit pour une lecture comparative entre pays plutôt que pour un focus unique.
- Les vues détaillées (liaisons entre données, répartition rural/urbain et masculin/féminin) dépendent de la granularité disponible dans le dataset fourni par le data engineer ; certains pays peuvent être moins bien couverts que d'autres sur ces axes.

## Démarche (choix, outils, étapes)

1. Prise de connaissance du cahier des charges pour établir les priorités des différentes vues du tableau de bord.
2. Modélisation des données sous forme de tables reliées par un **schéma en étoile**, pour servir de socle à l'ensemble de l'étude.
3. Construction du tableau de bord en **3 vues**, organisées du général au détaillé :
   - **Vue Monde** : informations générales sur l'accès à l'eau potable à l'échelle mondiale.
   - **Vue détaillée** : exploration plus fine des liaisons entre les différentes données.
   - **Vue rural/urbain et genre** : analyse de l'accès à l'eau potable en donnant de l'importance aux écarts rural/urbain et masculin/féminin.
4. Intégration des données dans l'application/le tableau de bord final.

**Outil :** Power BI.

## Résultats + impact / recommandations

- Un schéma en étoile reliant l'ensemble des tables de données, servant de socle à l'étude.
- Un tableau de bord Power BI structuré en 3 vues complémentaires, permettant une lecture progressive : du panorama mondial jusqu'aux écarts rural/urbain et de genre.
- La vue rural/urbain et genre met en évidence les inégalités d'accès à l'eau potable selon le lieu de résidence et le sexe, un axe clé pour orienter le choix du domaine d'investissement de DWFA (création vs modernisation de services, par exemple selon que l'écart rural/urbain domine ou non).
- **Impact attendu :** aider DWFA à orienter sa décision d'investissement (pays et domaine d'expertise) une fois le financement du bailleur de fonds confirmé, en s'appuyant sur une lecture à la fois globale et détaillée des inégalités d'accès à l'eau potable.

## Limites + prochaines pistes

- L'analyse s'appuie sur un instantané de données ; une mise à jour régulière serait nécessaire si le tableau de bord doit continuer à orienter les décisions après l'attribution du financement.
- Le choix final du pays et du domaine reste une décision stratégique de DWFA : le tableau de bord fournit un support d'aide à la décision, pas une décision automatisée.
- Un enrichissement avec des données OMS/FAO plus récentes ou plus granulaires permettrait d'affiner encore la vue rural/urbain et genre, notamment pour les pays où le dataset initial est moins complet.

---

*Projet réalisé dans le cadre de la mission consultant Data Analyst pour l'ONG DWFA (Drinking Water For All), sous la responsabilité de Thibaut Renard, chef de mission.*
