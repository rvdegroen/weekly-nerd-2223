# About

Ik ga deze pagina in het engels typen, omdat ik dan niet alles hoef te vertalen, omdat de spreker engels sprak. Deze gastcollege vond plaats bij de opleiding front-end. Het gastcollege werd gehouden door FDND.

# Campspace

The person that was speaking, was named Susan. Campspace connects outside of the digital world: it's for looking for a camping space. It's basically like an Airbnb but for camping.

## Data

With data you can make your static HTML more dynamic and we can do that with templating.

What she was showing was how she was looping through the data.

You can also read about blogs on the website. All of this data is in a database. What she was showing was the database. I think they have it in PHP or PHPStorm or MySQL. She was also talking about using an .exe list within the database.

Sometimes there's so much data, which you cannot endlessy add into the table, so one value is connected to a different table within the database.

## Backend

All of the sortering and filtering is happening in the backend.

1. She was showing paths and how the filtering information shows up in the web adress.
2. The database uses one dimensional CSS.
3. They're using the framework Symphony.
4. They use elasticsearch. You can use different URL's for example for images. It helps you structure your data.
5. There are two types of datasets within elasticsearch: for presentation and for (filtering) backend. For example the height of an image is for backend not relevant information.
6. They're getting the data in JSON format.

### Elasticsearch and filtering

She showed how we can filter with a `get` request in the browser. For example, we went to look for dutch campsites, then we can put in our code something like `match = nl`. Then when we check it on the website, when we're looking for dutch campsites, we see in the URL that `search=NL` was added.

This code below is wrong, but it's to prove a small example of what she had in elasticsearch and how she was filtering them (output was a `JSON`):

```

GET slug/_search {
    "query": [
        "match": NL;
    ]
}

```

# Take-aways from this presentation

1. Technology wise, don't re-invent it but tweak it. For example: every page has a body, a heading etc. but the content is different.
2. Name your variables and whatever good enough.
3. Code alot of things in english, because it's easier to find stuff.

# Reflectie

Ik vond het wel snel gaan, dus dat is een teken dat ik het wel interessant vond. Verder vond ik ook dat het moeilijk te volgen was. Het geluid was gewoon niet zo helder en door het accent was het wat lastiger te begrijpen, maar ik heb het zoveel mogelijk proberen te volgen. Sommige dingen die ik niet snapte, probeerde ik te begrijpen, alhoewel dit niet altijd makkelijk was. Hierdoor raakte ik soms ook weer de draad kwijt van de presentatie. Ik heb mijn notities hierboven vooral als rode draad gebruikt en dat heeft eigenlijk wel geholpen.
