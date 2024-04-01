# PD_EduardBravo

# main.cpp
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

`graph TD;` establece que estamos creando un gráfico de flujo con orientación de arriba a abajo (de arriba hacia abajo).
`A[Inicio] --> B[Proceso 1];` indica una conexión entre el nodo "Inicio" y el nodo "Proceso 1".
`B --> C[Proceso 2];` indica una conexión entre el nodo "Proceso 1" y el nodo "Proceso 2", y así sucesivamente.
`D[Decisión];` crea un nodo de decisión llamado "Decisión".
`D -->|Sí| E[Proceso 3];` indica una conexión desde el nodo "Decisión" al nodo "Proceso 3" etiquetada como "Sí".
`D -->|No| F[Proceso 4];` indica una conexión desde el nodo "Decisión" al nodo "Proceso 4" etiquetada como "No".
`E --> G[Fin];` indica una conexión desde el nodo "Proceso 3" al nodo "Fin".
`F --> G;` indica una conexión directa desde el nodo "Proceso 4" al nodo "Fin".
