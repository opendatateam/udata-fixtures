# udata-fixtures

This project holds fixtures for a basic set of data to load locally,
to have a few examples to work with while developping on the
[udata](https://github.com/opendatateam/udata) project.

## Generating the results.json file



The current fixtures in [results.json](results.json) are generated using the
`generate-fixtures-files` command in the
[udata](https://github.com/opendatateam/udata) repository.

This command needs a `FIXTURE_DATASET_SLUGS` setting lising all the datasets
to pull. You can specify this in the
[udata.cfg](https://udata.readthedocs.io/en/stable/getting-started/#configure-udata)
file:

```
FIXTURE_DATASET_SLUGS = [
    "barometre-des-resultats-de-laction-publique",
    "base-sirene-des-entreprises-et-de-leurs-etablissements-siren-siret",
    "donnees-relatives-aux-personnes-vaccinees-contre-la-covid-19-1",
    "demandes-de-valeurs-foncieres",
    "logements-sociaux-et-bailleurs-par-region",
    "base-adresse-locale-de-la-commune-de-garein",
    "cuisses-de-grenouille-et-escargots-frogs-legs-and-snails",
    "marches-publics-de-la-metropole-de-lyon",
    "defibrillateurs-presents-sur-la-commune-de-sixt-sur-aff-en-2018",
    "dpe-logements-avant-juillet-2021",
    "mairie-de-montluel-borne-de-recharge-pour-vehicules-electriques",
    "vehicules-a-faibles-et-a-tres-faibles-emissions-de-la-prefecture-de-region-auvergne-rhones-alpes",
    "base-adresse-nationale",
    "reseau-de-transport-en-commun-transagglo-de-dlva",
    "nombre-de-personnes-rickrollees-sur-data-gouv-fr",
]
```

To generate the [results.json](results.json) file, use the following command:

```
$ udata generate-fixtures-file http://data.gouv.fr
```

> [!NOTE]
> This command needs to be run in the [udata](https://github.com/opendatateam/udata)
> repository, once it is [fully set up](https://udata.readthedocs.io/en/stable/getting-started/)
