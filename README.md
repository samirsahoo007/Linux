# Linux

## How to POST a JSON file with curl??
  
You can post a json file with `curl` like so:

```
curl -X POST -H "Content-Type: application/json" -d @FILENAME DESTINATION
```

so for example:

```
curl -X POST -H "Content-Type: application/json" -d @../data/cats.json http://localhost:8080/mSfvMwNAfj
```

you can post a little blob of geojson, like so:

```
curl -X POST -H "Content-Type: application/json" -d '{"type":"Feature","properties":{"COUNTY":"M","PRECINCT":4505.0,"AREA":24330472.48801},"geometry":{"type":"Polygon","coordinates":[[[-122.579029970781065,45.53373981165327],[-122.579036751674209,45.533742065313575],[-122.579532751335037,45.533906068395808],[-122.579961749295705,45.534067060396104],[-122.580146749064056,45.534114065074704],[-122.581902757566823,45.534772060883959],[-122.582770766094569,45.535128058282019],[-122.583461773870638,45.535383050711246],[-122.584275765662781,45.535596050402262],[-122.584926770675438,45.535732043153857],[-122.585534768605342,45.535823041352423],[-122.586393777046183,45.535863042628513],[-122.586845771939593,45.535841037753478],[-122.587166778711079,45.535850042847976],[-122.587593783117342,45.535829037919441],[-122.587900782381638,45.535804036638346],[-122.588290773918729,45.535750036812139],[-122.588704782064923,45.535671034778389],[-122.589196776268082,45.535561035548149],[-122.589239647326053,45.535550318867173],[-122.589320708749753,45.536124484404517],[-122.589304695035338,45.537268231315537],[-122.59947923271595,45.53740953002616],[-122.599372142997979,45.537656509885132],[-122.601520781310597,45.537617244011571],[-122.601391421360532,45.543541079913162],[-122.578671442407,45.552336859399695],[-122.578672106607101,45.55230042862145],[-122.578693794893084,45.551092987187559],[-122.578713188347777,45.549969468845575],[-122.579029970781065,45.53373981165327]]]}}' http://localhost:8080/mSfvMwNAfj
```

Don't try to post a big blob, your terminal will hate you and you will hate yourself. It will go on forever and ever.

Use the syntax above (`curl -X POST -H "Content-Type: application/json" -d @FILENAME DESTINATION`) to specify a file instead.# Linux
