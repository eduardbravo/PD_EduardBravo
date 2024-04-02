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

`graph TD;`
`A[Inicio] --> B[Proceso 1];`
`B --> C[Proceso 2];`
`D[Decisión];`
`D -->|Sí| E[Proceso 3];`
`D -->|No| F[Proceso 4];`
`E --> G[Fin];`
`F --> G;`
