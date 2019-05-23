# Slovenian Open Office Dictionary (ispell)


## Adding to Postgres db

Copy .affix, .dict and .stop to $sharedir/tsearch_data

You can get the sharedir via `pg_config --sharedir`

then run 

```
CREATE TEXT SEARCH DICTIONARY slovene_ispell (
    TEMPLATE = ispell,
    DictFile = sl_SI,
    AffFile = sl_SI,
    Stopwords = slovene);
```

