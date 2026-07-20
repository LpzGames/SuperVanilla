# SuperVanilla V1.1 (Personalized Version)

> [!IMPORTANT]
> **Esta es una versión personalizada.**
> El repositorio base y original pertenece a [AoC-Gamers](https://github.com/AoC-Gamers/supervanilla).
> He realizado ajustes específicos de configuración y plugins para adaptarlos a las necesidades de mi servidor el cual está pensado en usarse
para partidas públicas o privadas, los cambios son:
> - Se desactivó la obligación de dar !ready en cada mapa.
> - Se habilitó sólo 1 botiquín para cada superviviente en cada mapa (no hay píldoras).
> - Se desactivó el poder disparar desde las escaleras.
> - Se extendió el tiempo de spawn de los infectados a 18 seg.
> - Se habilitó los plugins 'playerjoinMessage' y 'advertisements'.
> - Se desactivó el plugin 'autopause' el cual pausaba la partida cuando un jugador se crasheaba.
> - Se desactivó el plugin 'lerpmonitor' el cual te mandaba a espectador si usabas lerps 100.
> - Se desactivó la restricción que expulsaba a los jugadores que tenian habilitado el comando '+mat_hdr_level 0'.

---

[EN] [translation](https://translate.google.com/translate?sl=es&tl=en&u=https://github.com/AoC-Gamers/supervanilla)

SuperVanilla es una configuración competitiva para Left 4 Dead 2 que ajusta varios aspectos del juego para hacerlo más equilibrado y divertido.

## Características

### Diferencia con ZoneMod
- Witch y Tank aparecen en todos los capítulos.
- No se aplica reducción de daño a las armas 'cuerpo a cuerpo' usadas en chargers.
- Se permite aparición de armas T2 y T3 en el mapa.
- Se reemplaza el sistema de bonus de zonemod por el oficial.
- Se permiten wallkicks.
- Se elimina la limitación de infectados comúnes por superviviente vomitado.
- Se eliminan las restricciones de hordas de infectados comunes provocadas por eventos del mapa (mapinfo.txt).

En cada modo de juego, la cantidad de infectados comunes aumenta de la siguiente manera:
```sh
* Modo 1v1: 5 (base) + 2 (adicionales): 7 comunes
* Modo 2v2: 10 (base) + 4 (adicionales): 14 comunes
* Modo 3v3: 18 (base) + 3 (adicionales): 21 comunes
* Modo 4v4: 30 (base) + 4 (adicionales): 34 comunes
```

Las hordas provocadas por infectados y autos también siguen este ajuste:
```sh
* Modo 1v1: 12 (base) + 2 (adicionales): 7 comunes
* Modo 2v2: 25 (base) + 4 (adicionales): 29 comunes
* Modo 3v3: 32 (base) + 3 (adicionales): 35 comunes
* Modo 4v4: 50 (base) + 4 (adicionales): 54 comunes
```

Correcciones a la witch
```sh
* La *Witch* puede perseguir a las víctimas hasta zonas seguras.
* Se corrige su patrullaje cuando deambula por el mapa.
* Se evita que pierda su objetivo aleatoriamente.
```

### Límites de armas
Se establece un límite de 2 armas por grupo:

| Rifles | Shotgun | Snipers |
| --- | --- | --- |
| rifle | autoshotgun | hunting_rifle |
| rifle_desert | shotgun_spas | sniper_scout |
| rifle_sg552 |  | sniper_awp |
|  |  | sniper_military |

### Daño de armas
- Se aplica una reducción del 20% de daño al Tank para las siguientes armas:
```sh
| hunting_rifle | autoshotgun | shotgun_spas | rifle | rifle_desert | rifle_ak47 | rifle_sg552 |
```

- Se aplica una reducción del 30% de daño al Tank para:
```sh
| sniper_military |
```

- Se aplica una amplificación del 10% de daño al Tank para:
```sh
| sniper_scout | sniper_awp |
```

- Se modifica las estadísticas base de la 'sniper_scout'.
```sh
* Daño base: 105 -> 125 dmg
* Duración de recarga: 2.9s -> 2.0s
* Capacidad del cargador: 15 -> 10 balas
```

- Se modifica las estadísticas base de la 'sniper_awp'.
```sh
* Daño Base: 115 -> 145 dmg
* Duración de recarga: 3.66s -> 2.5s
* Capacidad del cargador: 20 -> 10 balas
```

## Instalación
1. SuperVanilla requiere el proyecto base [L4D2-Competitive-Rework](https://github.com/SirPlease/L4D2-Competitive-Rework). Descárgalo e instálalo primero.
2. Descarga los archivos desde el [repositorio de GitHub](https://github.com/AoC-Gamers/supervanilla).
3. Extrae los archivos en la carpeta principal de tu servidor.
4. Configura los archivos según tus necesidades (ver [Configuración](wiki/Configuración.md)).
5. Reinicia el servidor para aplicar los cambios.

## Configuración

### Agregar modo de juego
Para habilitar *SuperVanilla* en las votaciones del servidor, edita el archivo `addons/sourcemod/configs/matchmodes.txt` y agrega:

```plaintext
"MatchModes"
{
    "Super Vanilla Configs"
    {
        "svanilla"
        {
            "name" "Super Vanilla"
        }
        "sv3v3"
        {
            "name" "3v3 Super Vanilla"
        }
        "sv2v2"
        {
            "name" "2v2 Super Vanilla"
        }
        "sv1v1"
        {
            "name" "1v1 Super Vanilla"
        }
    }
}
```
Luego, reinicia el servidor para aplicar los cambios.

## Contribuciones
Gracias por tu interés en contribuir a *SuperVanilla*, Puedes reportar problemas o sugerir mejoras a través de la [página de issues](https://github.com/AoC-Gamers/supervanilla/issues) o enviando un *pull request* en el [repositorio de GitHub](https://github.com/AoC-Gamers/supervanilla/pulls).

## Licencia
*SuperVanilla* está licenciado bajo la licencia **CC-BY-SA 3.0**. Para más información, consulta el [texto completo de la licencia](http://creativecommons.org/licenses/by-sa/3.0/legalcode).
