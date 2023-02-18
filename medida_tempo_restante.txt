Próxima Corrida = 
VAR Dias =
CALCULATE(
    DATEDIFF(
        TODAY(),
        MIN(dCorridas[date]),
        DAY
    ),
    dCorridas[date] >= TODAY()
)
RETURN
SWITCH(
    TRUE(),
    Dias = 0, "Hoje",
    Dias = 1, "Amanhã",
    Dias & " dias"
)
