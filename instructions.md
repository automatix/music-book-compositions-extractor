Context:

I have some music books for children. There is a short sequence played for each piece. I would like to get the full versions.

Input:

A list of music pieces (in any language) or an image with such a list.

Erwarteter Output:
Expected Output:

Liste die Musikstücke zunächst in JSON auf.
List the music pieces in JSON first.

JEDES Musikstück-Listenelement soll wie folgt aussehen:
EACH music piece list element should look like this:

{
  "orig": {
  "language": <two-letter abbreviation of the original language>
  }
}

[] "<Name in the original language>" (in parentheses "<Name of the parent piece>", if any) Composer in their language

{
  "orig": {
  "language": <two letters code of the original language>
  }
}

[] "<name in the original language>" (in braces "<name of the parent piece>", if any) and the composer in his language

- data
  -- [RU] name (and, if any, the parent piece in parentheses!) and the composer in Russian
  -- [RU] name (and, if any, the parent piece in parentheses!) and the composer in German
  -- [RU] name (and, if any, the parent piece in parentheses!) and the composer in English
- links
  -- ...
  -- ...
  -- ...


Task:

0. If the input is an image, run OCR first.

1.

That means, all data and links should be bundled in one entry (and not first a list with names of all pieces, then the links to all pieces).

Provide at least one (better several) YouTube link(s) for each. (Check that they are really working links!)

Format:

Write the links as URLs. If it is a piece with lyrics (e.g. an aria from an opera), the first link in the original language. 

Example:

[FR] „Près des Remparts de Séville“ ("Carmen")
data:
[RU] „У стен Севильи“ ("Кармен") - Ж. Бизе
[DE] „An den Mauern von Sevilla“ ("Carmen ") - G. Bizet
[EN] „By the Walls of Seville“ ("Carmen") - G. Bizet
links:
[FR] https://www.youtube.com/watch?v=__ETBoAsCxk

Side note: Please note the desired formatting:

<name of the piece> (<parent piece>) dash <full name of the composer>
For example:
[FR] „An den Mauern von Sevilla“ ("Carmen ") - G. Bizet
