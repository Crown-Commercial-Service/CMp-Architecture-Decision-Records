# CMp-Architecture-Decision-Records
Crown Marketplace Architecture Decision Records

CMp = Crown Marketplace
 
 CMp will record here all **[architecture decision records](doc/adr)**:
 - that need to be agreed at TDDA retrospectively
 - where those decisions are _not_ considered sensitive


## Precedence

- [CCS ADRs](https://github.com/Crown-Commercial-Service/CCS-Architecture-Decision-Records) 
decisions are considred _binding_ on CMp unless a decision is made here temporarily overturning them
- All decisions here that conflict with CCS ADRs must be approved by TDDA in a timely fashion

## Process

1. All Architecture decision records for CMp that are _not_ considered sensitive should be mastered here.
1. records should be named ADR-XXXX-\<name>.md
1. Some diagrams are stored in .dot file format - they need to be converted to `jpg` format.

## Structure

```
/doc/adr - adr files
/doc/diagrams - .dot diagram source files
/doc/images - images generated from .dot files for linking into ADRs.
```

### Diagrams

As an experiment we will store some diagrams in [.dot](https://www.graphviz.org/documentation/) language.
That allows us to change control diagrams. But it adds a generation stage which we can incorporate into our build pipeline.
Until then we can generate the files via command lines or web tools.

## Decisions

  - [0001-record-product-decisions.md](doc/adr/0001-record-product-decisions.md)
  - [0002-use-auth0-in-private-beta](doc/adr/0002-use-auth0-in-private-beta.md)
  - [0003-use-a-single-domain.md](doc/adr/0003-use-a-single-domain.md)
