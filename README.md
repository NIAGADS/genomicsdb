# NIAGADS ALzheimer's GenomicsDB
monorepo for refactored NIAGADS Alzheimer's Genomics Database

> this is a new project under development

## Projects (Proposed)

### Client

#### records (Python)

> models defining GenomicsDB records: genes, variants (SNVs, INDELs & SVs), datasets, spans

> each `<record_type>` directory includes:

* a Pydantic model
* XML files linking records and record attributes (incl. tables) to database queries

> plus shared library (`lib`) 

* **TODO: possibly promote to own project to support `ADVP`**

* scripts for converting models to JSON, typescript interfaces, and JSON schema
* for use with NIAGADS API; typescript files for use with `genomicsdb-monorepo[client-app]`
* code for parsing and validating the XML files
* for use with NIAGADS API


#### table-configurations (JavaScript)

> `NIAGADS/niagads-viz-js[table]` configurations for record `table attributes`

* for use w/both `genomicsdb-monorepo[client-app]` and `to_view` converter in NIAGADS API response models
* separate project to make it easier to import into JavaScript applications
* same structure (one-directory per-record type) as records project


#### client-app (JavaScript/next.js)

* main GenomicsDB application


### Backend (migration from NIAGADS/GenomicsDBData)

#### Preprocessing/Data analysis

#### load (Python/Perl) 

