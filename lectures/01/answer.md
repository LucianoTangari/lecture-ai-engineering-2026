# 第1回 解答

## 演習

- 講座に固有の質問（宿題の3レベル）へのモデルの回答（要約でよい）：
- 用語集の正しい意味と比べて気づいたこと：
- 表示できたトークン数（入力 / 出力）：

## 宿題

- 取り組んだレベル：基礎
- やったこと：Hice la misma pregunta ("¿Qué es RAG y para qué sirve? Explícalo en 3 oraciones.") tres veces, cambiando solo el modelo con la variable AIE_MODEL: gemini-3.5-flash-lite, gemini-3.5-flash y gemini-3.1-flash-lite.
- 結果：Los tres modelos respondieron en español y en 3 oraciones, y explicaron RAG como una técnica que combina un modelo de lenguaje con búsqueda en fuentes externas para dar respuestas más precisas y reducir las alucinaciones. gemini-3.5-flash-lite escribió un solo párrafo con palabras en negrita. gemini-3.5-flash separó cada oración en un párrafo y agregó que no hace falta reentrenar el modelo. gemini-3.1-flash-lite escribió un párrafo sin formato y detalló el proceso (buscar documentos para dar contexto antes de responder). En el primer intento, gemini-3.1-flash-lite devolvió un error 503 (modelo saturado) y funcionó al repetirlo.
- 気づき・疑問：Con una sola pregunta, las diferencias fueron de estilo y de detalle más que de contenido, así que no alcanza para decir cuál modelo es mejor. Noté que la capa gratuita puede saturarse y que repetir el pedido a veces lo resuelve. Me queda la duda de cómo cambiaría el resultado variando la temperature.

## Qué hice
Hice la misma pregunta 3 veces cambiando solo el modelo (AIE_MODEL). Pregunta: ¿Qué es RAG y para qué sirve? Explícalo en 3 oraciones.

### Modelo: gemini-3.5-flash-lite
```
[model] gemini-3.5-flash-lite
[質問] ¿Qué es RAG y para qué sirve? Explícalo en 3 oraciones.

**RAG** (Generación Aumentada por Recuperación, por sus siglas en inglés) es una técnica de inteligencia artificial que combina los modelos de lenguaje con bases de datos externas para buscar información precisa antes de responder. **Sirve** para que las respuestas de la IA sean más precisas, actualizadas y reduzcan la invención de datos falsos. En resumen, **permite** que un chatbot "consulte" documentos privados o páginas web en tiempo real para darte una respuesta basada en hechos reales y específicos.
```

### Modelo: gemini-3.5-flash
```
[model] gemini-3.5-flash
[質問] ¿Qué es RAG y para qué sirve? Explícalo en 3 oraciones.

**RAG (Generación Aumentada por Recuperación)** es una técnica de Inteligencia Artificial que combina la búsqueda de datos externos con la capacidad de redacción de un modelo de lenguaje. 

Sirve para que la IA consulte fuentes confiables, documentos privados o bases de datos específicas en tiempo real antes de responder a una pregunta. 

De esta manera, se obtienen respuestas mucho más precisas y actualizadas, evitando que el modelo invente información ("alucinaciones") y sin necesidad de reentrenarlo.
```

### Modelo: gemini-3.1-flash-lite
[model] gemini-3.1-flash-lite
```
[質問] ¿Qué es RAG y para qué sirve? Explícalo en 3 oraciones.

RAG (Generación Aumentada por Recuperación) es una técnica que permite a los modelos de lenguaje acceder a información externa y actualizada, más allá de sus datos de entrenamiento originales. Su funcionamiento consiste en buscar documentos específicos en una base de datos privada o pública para proporcionar al modelo el contexto necesario antes de generar una respuesta. Esto sirve para obtener respuestas más precisas, fiables y reducir las alucinaciones, permitiendo que la IA consulte fuentes confiables en tiempo real.
