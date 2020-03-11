# versification_json
## A JSON expression of the Paratext versification.vrs file.

The aim is to find a JSON representation of the data currently stored in Paratext's versification.vrs file. The legacy format
is character-based. The JSON representation is intended to be a fairly literal replacement for that file. The main non-syntactic changes are

- Remove verse-count lines with no useful data (ie "1:1" which appears to mean that the book does not exist for this project)

- Include the name of the base versification (which, in the case of the Digital Bible Library, is always "org" (ie the org.vrs
file with "original" versification, ie BHS OT, GNT NT and "Catholic" DC.)

- Include merged verses (verse ranges) which, in the example, have been harvested from the USX files.

Historically, the mapping section has not been validated. (It would be quite hard to do this.) The current JSON examples include cases of mapping from verses that do not exist (according to the verse-count section of the versification file). This is not ideal, but the solution is not obvious, given that there are probably also incorrect mappings from verses that do exist.
