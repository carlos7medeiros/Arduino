# 🚦 Simulação de Semáforo com Arduino

Projeto de simulação de um semáforo simples utilizando **Arduino UNO**, LEDs e componentes básicos de eletrônica. O código controla a ordem dos sinais: verde, amarelo e vermelho, com tempos definidos, simulando o comportamento de um semáforo de trânsito real.

## 📸 Demonstração

> 💡 Você pode adicionar aqui uma imagem do circuito montado ou um GIF do funcionamento.

![Demonstração do Projeto](imagens/demonstracao.gif)

## 🧰 Materiais Utilizados

- Arduino UNO (ou compatível)
- 1 LED vermelho
- 1 LED amarelo
- 1 LED verde
- 3 resistores de 220Ω
- Protoboard
- Cabos jumper
- (Opcional) Software de simulação como Tinkercad ou Proteus

## ⚙️ Esquema de Funcionamento

O semáforo executa o seguinte ciclo continuamente:

1. ✅ **Verde** aceso por 5 segundos
2. ⚠️ **Amarelo** aceso por 2 segundos
3. 🛑 **Vermelho** aceso por 5 segundos

## 🔌 Ligações

| Componente  | Pino Arduino | Observações         |
|-------------|--------------|---------------------|
| LED Verde   | 8            | Com resistor de 220Ω|
| LED Amarelo | 9            | Com resistor de 220Ω|
| LED Vermelho| 10           | Com resistor de 220Ω|
| Todos os LEDs | GND         | Terminal negativo via resistor|

## 💻 Código Fonte

```cpp
int ledVerde = 8;
int ledAmarelo = 9;
int ledVermelho = 10;

void setup() {
  pinMode(ledVerde, OUTPUT);
  pinMode(ledAmarelo, OUTPUT);
  pinMode(ledVermelho, OUTPUT);
}

void loop() {
  digitalWrite(ledVerde, HIGH);
  delay(5000);
  digitalWrite(ledVerde, LOW);

  digitalWrite(ledAmarelo, HIGH);
  delay(2000);
  digitalWrite(ledAmarelo, LOW);

  digitalWrite(ledVermelho, HIGH);
  delay(5000);
  digitalWrite(ledVermelho, LOW);
}
```

## ▶️ Como Usar

1. Monte o circuito conforme o esquema.
2. Abra a **IDE do Arduino**.
3. Copie e cole o código acima.
4. Conecte a placa Arduino ao computador.
5. Selecione a placa e porta correta no menu `Ferramentas`.
6. Envie o código para o Arduino.

## 📚 Aprendizados

- Manipulação de saídas digitais com `digitalWrite()`
- Uso de `delay()` para temporização
- Lógica de automação básica com `loop()`
- Noções iniciais de projetos com Arduino

## 🧑‍💻 Autor

- **Carlos Medeiros**  
- Estudante de Tecnologia em Sistemas para Internet  
- Instituto Federal do Sudeste de Minas Gerais – Campus Barbacena  
- 📅 Julho de 2025

## 📄 Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

## 🌐 Contato

Se tiver dúvidas, sugestões ou quiser trocar ideias:

- Email: cmcarlosmedeiros63@gmail.com
- GitHub: [@carlos7medeiros](https://github.com/carlos7medeiros)
