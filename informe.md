# Practica 1

## main.cpp
#include <Arduino.h>

#define LED_BUILTIN 20

#define DELAY 500

void setup()
{

Serial.begin(115200);

pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{

digitalWrite(LED_BUILTIN, HIGH);

Serial.println("ON");

delay(DELAY);

digitalWrite(LED_BUILTIN, LOW);

Serial.println("OFF");

delay(DELAY);
}

# Diagrama de flujos (ejemplo)

```mermaid
graph TD;
A[Inicio] --> B[Proceso 1];
B --> C[Proceso 2];
D[Decisión];
D -->|Sí| E[Proceso 3];
D -->|No| F[Proceso 4];
E --> G[Fin];
F --> G;
```

# Diagrama de tiempos (ejemplo)

```mermaid
gantt
  title Diagrama Tiempo
  dateFormat YYYY-MM-DD
  excludes weekends

  section Diseño
    Diseño BD:DB, 2022-07-20, 7d
    Diseño Frontend:F,2022-07-20, 7d

  section Desarrollo
    Conexion DB:CDB, after DB, 1d
    Desarrollo Front:DF, after F, 4d
```

# Tiempo libre del procesador

Para determinar el tiempo libre del procesador, necesitamos restar el tiempo total por iteración del período total del bucle loop(). 

Tiempo libre del procesador = Período total del bucle - Tiempo total por iteración
= 1000 ms - 1000 ms
= 0 segundos

Es decir, el tiempo libre del procesador es 0 segundos, lo que significa que el procesador está completamente ocupado ejecutando el código en el bucle loop() y no tiene tiempo adicional disponible.
