## Fra km/s til m/s @unplugged
<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/ESERODanmark/isstravellingdistance/blob/master/ikon_issDist.png?raw=true" alt="DampVibrations" width="300"/>
  <img src="https://github.com/ESERODanmark/multicounter/blob/master/clickTip.gif?raw=true" alt="ClickTip" width="300"/>
</div>


## Fra km/s til m/s

Denne ændring går ud fra at du allerede har lavet "hvor langt fløj ISS". Se evt. tip.

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid= beregnetTid / 1000
    afstand = beregnetTid * 7.77
    basic.showNumber(afstand)
    basic.showString(" km")})
```

## Ændring af hastighed
Ændr 7.77 i `||variable.set afstand to||` til den hastighed du vil regne ud fra. I eksemplet skriver vi 2.

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid= beregnetTid / 1000
    afstand = beregnetTid * 2
    basic.showNumber(afstand)
    basic.showString(" km")})
```

## Ændring fra km til m
Ændr km  i `||basic.showString(" km")||` til m `||basic.showString(" m")||`. Dit resultat har nu enheden meter.

```blocks
input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid= beregnetTid / 1000
    afstand = beregnetTid * 2
    basic.showNumber(afstand)
    basic.showString(" m")})
```

## Tillykke!
Nu regner din @boardname@ afstanden ud i meter, hvis du bevæger dig med 2 meter per sekund. Tryk på færdig!


```template
input.onButtonPressed(Button.A, function () {
    startTime = input.runningTime()
    basic.showLeds(`
    . . . . .
    . . # . .
    . . # . .
    . . # . .
    . . . . .
    `)
})

input.onButtonPressed(Button.B, function () {
    slutTid = input.runningTime()
    beregnetTid = slutTid - startTid
    beregnetTid= beregnetTid / 1000
    afstand = beregnetTid * 7.77
    basic.showNumber(afstand)
    basic.showString(" km")})
```