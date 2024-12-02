NOM : DAGOU
PRENOM : EVARISTE JEAN 
NIVEAU : L2 B

Rapport Final - Système de Contrôle d'Accès
Introduction
Ce rapport présente le processus de conception, modélisation, vérification et optimisation d'un système de contrôle d'accès pour un bâtiment sécurisé. Le projet a été réalisé à travers plusieurs étapes, allant de la spécification des règles de sécurité à la vérification formelle du système.

Étape 1 : Spécification du Système avec la Logique Formelle
Spécifications Initiales
Le système de contrôle d'accès est conçu pour gérer l'accès à un bâtiment sécurisé en vérifiant la validité d'une carte d'accès et d'un code PIN. Les états principaux identifiés sont :

ACTION : État initial où le système attend une action.
VERIFICATION_CARTE : État de vérification de la carte.
VERIFICATION_CODE : État de vérification du code.
ACCESS_ACCORDE : État où l'accès est accordé.
ACCESS_REFUSE : État où l'accès est refusé.
ALARME : État où l'alarme est déclenchée après plusieurs tentatives échouées.
Règles Logiques
Les règles logiques qui régissent ces états peuvent être formalisées comme suit :

Accès accordé : Si la carte est valide (A) et le code est correct (B), alors l'accès est accordé. (A ∧ B → ACCESS_ACCORDE)
Accès refusé : Si la carte est invalide (¬A) ou le code est incorrect (¬B), alors l'accès est refusé. (¬A ∨ ¬B → ACCESS_REFUSE)
Alarme déclenchée : Si le nombre de tentatives échouées dépasse 3, alors l'alarme est déclenchée. (Tentatives > 3 → ALARME)
Étape 2 : Modélisation du Système avec des Automates
Automate Fini Déterministe (AFD)
Un automate a été construit pour modéliser le fonctionnement du système. Les transitions entre les états ont été définies conformément aux règles logiques spécifiées. L'automate gère les entrées de la carte et du code, et passe d'un état à un autre en fonction des résultats de ces vérifications.

Vérification des Règles Logiques
Les transitions de l'automate ont été vérifiées pour s'assurer qu'elles respectent les règles logiques définies à l'étape 1. Chaque état et transition a été soigneusement examiné pour garantir la conformité aux spécifications.

Étape 3 : Conception de Circuits Logiques
Implémentation des Règles Logiques
Les règles logiques ont été simplifiées à l'aide de l'algèbre de Boole et implémentées sous forme de circuits logiques combinatoires. Les portes logiques AND, OR et NOT ont été utilisées pour réaliser les différentes fonctions du système.

Optimisation des Circuits
Des cartes de Karnaugh ont été utilisées pour optimiser les circuits logiques, réduisant ainsi la complexité matérielle tout en maintenant la fonctionnalité.

Étape 4 : Vérification et Validation Formelle
Vérification de la Conformité
Des méthodes de model checking ont été appliquées pour vérifier automatiquement que l'automate respecte les règles de sécurité spécifiées. Des outils tels que SPIN et Z3 ont été utilisés pour analyser les propriétés de sûreté et de sécurité du système.

Identification des Contre-Exemples
Des scénarios d'attaque ont été simulés pour évaluer la robustesse du système. Les résultats ont permis d'identifier des failles potentielles, conduisant à des ajustements dans les règles ou le modèle.

Conclusion
Le système de contrôle d'accès conçu a démontré une efficacité et une fiabilité élevées tout au long du processus de développement. Les spécifications initiales ont été respectées, et le système a été validé par des tests rigoureux. Les défis rencontrés, notamment en matière de sécurité et de robustesse, ont été abordés avec succès grâce à des méthodes formelles et des optimisations. Ce projet a permis de renforcer la compréhension des concepts de logique formelle, d'automates et de circuits logiques, tout en fournissant une solution pratique pour un problème de sécurité réel.
