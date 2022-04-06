# Zenodo upload metadata schema

File `schema.json` contains the JSONschema schema for the metadata used when making uploads to Zenodo or Zenodo Sandbox. It was derived by hand using the following resources:
1. https://github.com/zenodo/zenodo/blob/f091af8f2d0bfac2fdaf53222160f8e037d5a0e6/zenodo/modules/deposit/static/json/zenodo_deposit/deposit_form.json
2. https://github.com/zenodo/zenodo/blob/594bad1d2c3c12c2d44a8f35950662677d51414b/tests/unit/conftest.py#L1376-L1430

Below is an example file that includes most keys:

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
            "identifier": "134514",
            "relation": "isSupplementedBy",
            "resource_type": "publication-book"
        }
    ],
    "subjects": [
        {
            "identifier": "https://somewhere.com",
            "scheme": "url",
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
