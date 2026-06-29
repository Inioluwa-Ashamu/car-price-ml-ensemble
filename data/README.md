# Data Contract

Place the advert dataset at:

```text
data/adverts.csv
```

Required modelling target:

```text
price
```

Expected feature families:

- mileage
- year or registration date
- vehicle make and model
- body type
- fuel type
- colour
- condition
- listing reference or listing date signal

The repository keeps data storage separate from modelling code so the workflow can be run against any compatible advert export.
