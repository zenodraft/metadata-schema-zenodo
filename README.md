# Zenodo upload metadata schema

File `schema.json` contains the JSONschema schema for the metadata used when making uploads to Zenodo or Zenodo Sandbox. It was derived by hand using the following resources:
1. https://github.com/zenodo/zenodo/blob/f091af8f2d0bfac2fdaf53222160f8e037d5a0e6/zenodo/modules/deposit/static/json/zenodo_deposit/deposit_form.json
2. https://github.com/zenodo/zenodo/blob/594bad1d2c3c12c2d44a8f35950662677d51414b/tests/unit/conftest.py#L1376-L1430

Below is an example JSON metadata file that demonstrates almost everything that is valid within the constraints of the schema (there are some additional, conditional properties that need to be present based on the value of `access_right` and of `upload_type`; the example shows just one of the possible  combinations).

```json
{
    "access_right": "open",
    "communities": [
        {
            "identifier": "zenodo"
        }
    ],
    "conference_acronym": "The conference acronym",
    "conference_dates": "The conference dates",
    "conference_place": "The conference place",
    "conference_session": "The conference session",
    "conference_session_part": "The conference session part",
    "conference_title": "The conference title",
    "conference_url": "https://theconferenceurl.org",
    "contributors": [
        {
            "affiliation": "The affiliation",
            "name": "Contributor, The",
            "orcid": "0000-0002-7064-4069",
            "type": "Other"
        }
    ],
    "creators": [
        {
            "affiliation": "The Affiliation",
            "name": "Creator, The",
            "orcid": "0000-0002-7064-4069"
        }
    ],
    "description": "The description",
    "doi": "",
    "grants": [
        {
            "id": "10.13039/501100000780::675191"
        }
    ],
    "image_type": "photo",
    "imprint_isbn": "34k1bh45b134jb5h13j4b5j13b4h",
    "imprint_place": "The imprint place",
    "imprint_publisher": "The imprint publisher",
    "journal_issue": "4",
    "journal_pages": "12.4 - D",
    "journal_title": "The journal",
    "journal_volume": "578",
    "keywords": [
        "keyword 1",
        "keyword 2",
        "keyword 3"
    ],
    "language": "ada",
    "license": "Apache-2.0",
    "notes": "some notes",
    "partof_pages": "12-345",
    "partof_title": "The partof title",
    "references": [
        "The first reference",
        "The second reference"
    ],
    "related_identifiers": [
        {
            "identifier": "ads:2011ApJS..192...18K",
            "relation": "cites",
            "resource_type": "dataset",
            "scheme": "ads"
        },
        {
            "identifier": "ark:/13030/tqb3kh97gh8w",
            "relation": "compiles",
            "resource_type": "image-diagram",
            "scheme": "ark"
        },
        {
            "identifier": "hep-th/1601.07616",
            "relation": "continues",
            "resource_type": "image-drawing",
            "scheme": "arxiv"
        },
        {
            "identifier": "PRJNA224116",
            "relation": "describes",
            "resource_type": "image-figure",
            "scheme": "bioproject"
        },
        {
            "identifier": "SAMN08289383",
            "relation": "documents",
            "resource_type": "image-other",
            "scheme": "biosample"
        },
        {
            "identifier": "10.1002/example",
            "relation": "hasPart",
            "resource_type": "image-photo",
            "scheme": "doi"
        },
        {
            "identifier": "4006381333931",
            "relation": "isAlternateIdentifier",
            "resource_type": "image-plot",
            "scheme": "ean13"
        },
        {
            "identifier": "73513537",
            "relation": "isCitedBy",
            "resource_type": "lesson",
            "scheme": "ean8"
        },
        {
            "identifier": "ENSMUST00000017290",
            "relation": "isCompiledBy",
            "resource_type": "other",
            "scheme": "ensembl"
        },
        {
            "identifier": "GCF_000001405.38",
            "relation": "isContinuedBy",
            "resource_type": "physicalobject",
            "scheme": "genome"
        },
        {
            "identifier": "4079154-3",
            "relation": "isDerivedFrom",
            "resource_type": "poster",
            "scheme": "gnd"
        },
        {
            "identifier": "mem_13102590",
            "relation": "isDescribedBy",
            "resource_type": "presentation",
            "scheme": "hal"
        },
        {
            "identifier": "10013/epic.10033",
            "relation": "isDocumentedBy",
            "resource_type": "publication-annotationcollection",
            "scheme": "handle"
        },
        {
            "identifier": "0-9752298-0-X",
            "relation": "isIdenticalTo",
            "resource_type": "publication-article",
            "scheme": "isbn"
        },
        {
            "identifier": "1422-4586-3573-0476",
            "relation": "isNewVersionOf",
            "resource_type": "publication-book",
            "scheme": "isni"
        },
        {
            "identifier": "1188-1534",
            "relation": "isObsoletedBy",
            "resource_type": "publication-conferencepaper",
            "scheme": "issn"
        },
        {
            "identifier": "0A9 2002 12B4A105 7",
            "relation": "isPartOf",
            "resource_type": "publication-datamanagementplan",
            "scheme": "istc"
        },
        {
            "identifier": "urn:lsid:ubio.org:namebank:11815",
            "relation": "isPreviousVersionOf",
            "resource_type": "publication-deliverable",
            "scheme": "lsid"
        },
        {
            "identifier": "0000-0002-1694-233X",
            "relation": "isPublishedIn",
            "resource_type": "publication-milestone",
            "scheme": "orcid"
        },
        {
            "identifier": "PMC2631623",
            "relation": "isReferencedBy",
            "resource_type": "publication-other",
            "scheme": "pmcid"
        },
        {
            "identifier": "pmid:12082125",
            "relation": "isRequiredBy",
            "resource_type": "publication-patent",
            "scheme": "pmid"
        },
        {
            "identifier": "http://purl.oclc.org/foo/bar",
            "relation": "isReviewedBy",
            "resource_type": "publication-preprint",
            "scheme": "purl"
        },
        {
            "identifier": "NZ_JXSL01000036.1",
            "relation": "isSourceOf",
            "resource_type": "publication-proposal",
            "scheme": "refseq"
        },
        {
            "identifier": "SRR6437777",
            "relation": "isSupplementedBy",
            "resource_type": "publication-report",
            "scheme": "sra"
        },
        {
            "identifier": "Q9GYV0",
            "relation": "isSupplementTo",
            "resource_type": "publication-section",
            "scheme": "uniprot"
        },
        {
            "identifier": "http://www.heatflow.und.edu/index2.html",
            "relation": "obsoletes",
            "resource_type": "publication-softwaredocumentation",
            "scheme": "url"
        },
        {
            "identifier": "urn:nbn:de:101:1-201102033592",
            "relation": "references",
            "resource_type": "publication-taxonomictreatment",
            "scheme": "urn"
        },
        {
            "identifier": "swh:1:cnt:94a9ed024d3859793618152ea559a168bbcbb5e2",
            "relation": "requires",
            "resource_type": "publication-technicalnote",
            "scheme": "swh"
        },
        {
            "identifier": "ascl:1908.011",
            "relation": "reviews",
            "resource_type": "publication-thesis",
            "scheme": "ascl"
        },
        {
            "identifier": "ascl:1908.011",
            "relation": "reviews",
            "resource_type": "publication-workingpaper",
            "scheme": "ascl"
        },
        {
            "identifier": "ascl:1908.011",
            "relation": "reviews",
            "resource_type": "software",
            "scheme": "ascl"
        },
        {
            "identifier": "ascl:1908.011",
            "relation": "reviews",
            "resource_type": "video",
            "scheme": "ascl"
        }
    ],
    "subjects": [
        {
            "identifier": "ads:2011ApJS..192...18K",
            "scheme": "ads",
            "term": "some-term"
        },
        {
            "identifier": "ark:/13030/tqb3kh97gh8w",
            "scheme": "ark",
            "term": "some-term"
        },
        {
            "identifier": "hep-th/1601.07616",
            "scheme": "arxiv",
            "term": "some-term"
        },
        {
            "identifier": "PRJNA224116",
            "scheme": "bioproject",
            "term": "some-term"
        },
        {
            "identifier": "SAMN08289383",
            "scheme": "biosample",
            "term": "some-term"
        },
        {
            "identifier": "10.1002/example",
            "scheme": "doi",
            "term": "some-term"
        },
        {
            "identifier": "4006381333931",
            "scheme": "ean13",
            "term": "some-term"
        },
        {
            "identifier": "73513537",
            "scheme": "ean8",
            "term": "some-term"
        },
        {
            "identifier": "ENSMUST00000017290",
            "scheme": "ensembl",
            "term": "some-term"
        },
        {
            "identifier": "GCF_000001405.38",
            "scheme": "genome",
            "term": "some-term"
        },
        {
            "identifier": "4079154-3",
            "scheme": "gnd",
            "term": "some-term"
        },
        {
            "identifier": "mem_13102590",
            "scheme": "hal",
            "term": "some-term"
        },
        {
            "identifier": "10013/epic.10033",
            "scheme": "handle",
            "term": "some-term"
        },
        {
            "identifier": "0-9752298-0-X",
            "scheme": "isbn",
            "term": "some-term"
        },
        {
            "identifier": "1422-4586-3573-0476",
            "scheme": "isni",
            "term": "some-term"
        },
        {
            "identifier": "1188-1534",
            "scheme": "issn",
            "term": "some-term"
        },
        {
            "identifier": "0A9 2002 12B4A105 7",
            "scheme": "istc",
            "term": "some-term"
        },
        {
            "identifier": "urn:lsid:ubio.org:namebank:11815",
            "scheme": "lsid",
            "term": "some-term"
        },
        {
            "identifier": "0000-0002-1694-233X",
            "scheme": "orcid",
            "term": "some-term"
        },
        {
            "identifier": "PMC2631623",
            "scheme": "pmcid",
            "term": "some-term"
        },
        {
            "identifier": "pmid:12082125",
            "scheme": "pmid",
            "term": "some-term"
        },
        {
            "identifier": "http://purl.oclc.org/foo/bar",
            "scheme": "purl",
            "term": "some-term"
        },
        {
            "identifier": "NZ_JXSL01000036.1",
            "scheme": "refseq",
            "term": "some-term"
        },
        {
            "identifier": "SRR6437777",
            "scheme": "sra",
            "term": "some-term"
        },
        {
            "identifier": "Q9GYV0",
            "scheme": "uniprot",
            "term": "some-term"
        },
        {
            "identifier": "http://www.heatflow.und.edu/index2.html",
            "scheme": "url",
            "term": "some-term"
        },
        {
            "identifier": "urn:nbn:de:101:1-201102033592",
            "scheme": "urn",
            "term": "some-term"
        },
        {
            "identifier": "swh:1:cnt:94a9ed024d3859793618152ea559a168bbcbb5e2",
            "scheme": "swh",
            "term": "some-term"
        },
        {
            "identifier": "ascl:1908.011",
            "scheme": "ascl",
            "term": "some-term"
        }
    ],
    "thesis_supervisors": [
        {
            "affiliation": "The affiliation",
            "name": "The name"
        }
    ],
    "thesis_university": "The university",
    "title": "Untitled",
    "upload_type": "image",
    "version": "1.2.3-b4"
}
```
