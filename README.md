# Markdown Links

***
## 1. Resumen de la librería

Esta librería se hizo para hacer más facil la identificacion de links que se encuentra en los archivos .md 
de cualquier directorio, donde nos mostrará cuantos link se encuentran en las carpetas iteradas, si estan funcionales, si son únicos o si estan rotas las urls.


## md-links
extraer los links que estan en los archivos .md de los directorios

## Instalar librería

```sh
npm i danitap-md-links
```

Si estás usando Linux y esto falla trata anteponiendo sudo

## Como usar 

Ejemplos:

```sh
$ md-links ./some/example.md --validate
./some/example.md http://algo.com/2/3/ ok 200 Link a algo
./some/example.md https://otra-cosa.net/algun-doc.html fail 404 algún doc
./some/example.md http://google.com/ ok 301 Google
```

Vemos que el _output_ en este caso incluye la palabra `ok` o `fail` después de
la URL, así como el status de la respuesta recibida a la petición HTTP a dicha
URL.

##### `--stats`

Si pasamos la opción `--stats` el output (salida) será un texto con estadísticas
básicas sobre los links.

```sh
$ md-links ./some/example.md --stats
Total: 3
Unique: 3
```

También podemos combinar `--stats` y `--validate` para obtener estadísticas que
necesiten de los resultados de la validación.

```sh
$ md-links ./some/example.md --stats --validate
Total: 3
Unique: 3
Broken: 1
```

## Flujograma
  [Flujograma]https://viewer.diagrams.net/?tags=%7B%7D&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Diagrama%20md.drawio#R7V3bd6K6Gv9rXOucB7sIN%2BGRIrOHc6zOUqd79iNKVM6gOIjTdv%2F1O1yikGClBSFpTx%2BsBAzwXX7fJV%2BSnmRun%2F8Inf3mIXCh3xMF97knDXuiKOqShP7FLS9pC5BVIW1Zh56btZ0bZt7fMGvElx09Fx4KF0ZB4Efevti4DHY7uIwKbU4YBk%2FFy1aBX7zr3llDqmG2dHy69U%2FPjTZpqyYOzu1fobfe4DsDVU%2FPbB18cfYmh43jBk%2B5JsnqSWYYBFH6bftsQj%2BmHqZL%2BrsvF86eHiyEu6jKD46%2FdiN72%2F9pH76uH7%2Ftw9%2BipfTl7NmiF%2FzC0EXvnx0GYbQJ1sHO8a1z630YHHcujHsV0NH5mlEQ7FEjQI3%2Fg1H0kjHTOUYBatpEWz87Sz855qwTrmH0yuMq6XXxM%2BZ%2BmL3vHzDYwih8QReE0Hci73eRh04mCuvTdaeffgs89CiikMmtnt0HC60kFHtInzP7UZ7kr%2FejE90cgmO4hFQ36EvuZc5NCT%2FfwFsxvdtvxz9mhOiJqo%2FIe78Kkqc8c139dYzF8P43DCMPCX%2Ff8b31ricZ8T12Gxh6UcI3fB36ts7%2BN9uhPbZNe4K7Ra%2Bd9ly8G9VMirDvI3iIRfVp40VwtneW8ZknBFFFQVx5vm8GfhAmv5NcBWqujNoPURj8hLkzmriQVPU10Y1fFD6%2FKpTZWakoFHImFE9ndAEYMjY5ZFGEy1JckJy3ionKFASkOsEcBIgVIaAp3VU41N3p97mBO12EuPVh2B%2FZ4%2F%2FO6DM1tRzZ03381Q2Wx20iRtfUfZFK7WhxVQqrazNWX9JU5NUZlKizeit1BoCiVAv6DJ%2B96Efu%2B19xV3dKdjR8znpODl6yg%2FdjwKAdDAADAgQG7YIAABJf2NwSXwhs1uR22TLgEJt7pti7%2F2L9sGdz9KJfakJvuAm2i%2BPhzQ7WSlvC5bLMwVpoiqy8CgrVIVm5YLpzkKyVILJ2M0SmHfGZTdEUvVxUJF7G2uESkQKGOaYb2Ymt57qpysOD97ezSLqKibiPRT95DeW%2BpwzjvpCWH1KFBxT9d8EOEszKmhrgBiAsJHKmKXZIJewgHa7m2MFWzHsVVLERuDWqUi5v29ZOonE1RS3kOwpTaxRj3Nx%2BNBL84gqRKEeic0ii44tPBEkn55sZSBpwBklZzuBqvg5o7WCXrHaMXSqlT%2BZk%2FGhN5%2FY0wa04MHa2MRbtFod9QnzBuJ9NRqUx81X3Lz7RT5Un7l3bP5d6fd%2BM%2Bde7qYVu82hV9u1OYgXejqarlViOpq66UJWGEmiirheZXTWFdruYW%2BdMf1tSSwUU1VIiOXBjtcRCkFPL8aSUVSNnAf3b2TqaVa%2FKEaULp%2FGt7C69%2FBBSmY4Id5IoFWifceK9HMWXBKvVAd6GWUoXStRu4qotxVOFju2hRileUzYtFxOYxvSbNTdey2dwFSbIrIUJovbxVRJf2LZKykK7KqnSLipfTkvlIgFRbpqj9cZX6Xwx007ISVBqOyF94Q6w73YAij03MFXG1PxqP04%2BrKk6efadmSq5NhuBcIGPD5PZfGpM0SXfx%2BjjwRrPjP%2BggFoYxh%2FWdDqZvnnQ2jvsfeflzdx1HaitSrmrLjW4WDXEXSKdImslEbbQZoQt0iD6iRKWCmsJS1H%2FPzvy4NcxO3ACjBdXDhPi1j73gGBU6z53mW%2FBI6Ou%2BtxS44OU9XxukSI82z73JQyq43NnQt%2FPOmLXBZfoNG2zLvjctsaJq%2FZjbo1NezK%2Bexh%2BDD9c0UlTRHtqept%2BuESP4p%2Fd50cjLu5OdYNPz1jRBnfXfWNcSdGKayx3UvBZw6bIFW2KLHbjJbSdLJfo0HVyj4DKilVmNMmlD2Y45nww0NkY96aW%2BX06sx%2BNOxq4mB%2FIVQFB%2BM4HcqVPHWaqGmtxTSd1MYiA4cuP7PfJQW4EIj48D0EkR%2FXHIDDSXYfElma%2FaGJREkDLJdaYIDk9tOfWFLnwgmkMjTMicoh6lLnpHPUUzqaAyS1VxCIuEICoa%2B2qAe1Mj6ycWxBPrPoAGlBmZ9rVAJl2wT5S1AIEsghfqRYm3mzSqdxJxRyuLDhXE%2FyVO1NeWXDBGyj4AjLtDCRH32DoIXrFHmFdD0Gp6iGwNfit0KmdXVDKejYScVgum6jAE0RRLGgd%2B5k4hU5YM503bZRdKq7UwGaJeW5xNj20regFiERiASinrF1bnlvJBP4kFR15EIXriAbPEdwtvWB3t3U5nNAkkAEiqBjE6MplbtazNLQL94lSNwAQs14B6Dh3o3A2p0lpDZwGRPRDOtm3XlqEhqaPEFTSoF%2BiAe1GlQPa%2BeVLJ3BcfjXqwIueMRJ1qPT0g0djZA8NUsoFa2xOxijOH8aN%2FMu8hF3C7mS%2BZBY3XzKvV5T5gciUzA94r%2B%2BvTvjGZ2zUIzxn9f2DJuv7z0Ezu2EyFqwa5UX66xX%2Bo5xBiY1LYmw%2BTrE%2FOEUJuOZlQEd7rVb7D8pYyhPYYQy7DnaNzxitR3g6QbgJ4aonmklkLZpIQCHFCk5GSSQiMpP1amJODo43Rm18M26kunGX6EIMTVbgKy0vLIBf9C0m5fIqb%2B9f%2BOPilKUypTTp%2Bx0iJ0JmRzSDn%2FTJleP5VxaKo5%2F8sHd2VZ78YsHu%2BTHRPdPe3rkuKNtgc1qR4QVHZNWGZG8XuX3qNaEAuS6zonScQNV5zx4NqmaPNMYCuquLVyxPmHCGL0lI%2FmhEWx%2Bd0A3Qr%2FzgEH96u5%2FxfxjD5HFHrwtFIqsThgjFqq%2BeTIpI1cXQncM%2B3UBh5T3HAkPioio4OhhkRCimutBfGV6Kw0GMas3opyIyFoPovE%2Fu0qrGIBpbNSVAoL2vEkvFTsZFvyTt78m44InuuKYkowW76Re9DE4%2Fpp40Hv7U1BPOlj87SUojmUneZkFqtD0J9pEX7Gjb3%2B%2BjizzXiWDZORTUHSKKzYynGMm5J92bd97HUzAaXYetxisfasIWPYTItnlvckCFNO%2FMw5bOeyq%2Bup6wtcYBEDgr1j1Jyg3MO%2FNqgqXsjdadLyOuyawZ8bK9WrgCJ6kqOKmMgVOlclyGwAlLyqc04kDgrFq3eVtcPtJIbfDW9mZToGT3IKat%2FEmUmpiTIyqazpmdp4OXk52%2FkujnM3IXBYE1o1%2B2FChX4FZ1hRyt8Q336pWr0ISPd0Gxx4Zp90ypp0tjWrgLZL4i4A2IK1CJ0pGycfd2S6Z13kumtaqTkzW2itk0uuLh0ZraX2wzXmgknScwmxvz7%2Bm6S%2Bcqz65lmFyehQEZLtuwmCsZrrqlFXZIWJFhOk2NKwyOO2%2BZlBy8XPc9oiByfHjoXrR1jTXRBt3sqFxDlFvbHlnsNjbSLu%2FES5Y4%2Fgu5qX1ZEP59QfSTokSJPol06Ffcd3qWkAJOKg1VYjX3E9uu7VFOroPYoEpxVtjcvONyQaU0rWOVoos1cI0wqRo5leJTLzSROb0QOlkWqYZeNO4MXUjDkQtYta4X9Cjnh7cbpCtWqh9lrtgN9aOTDcnerx9AaGlVCQby1Lxtq94Wa4DQMWcEOjafW9MHe2wMSwYSqpaLk5ikQM2VyzBJExeS2tCCBzop5VWjw3ckm9FhGMSV%2FGdmICJsHgI3HmWx%2FgE%3D

