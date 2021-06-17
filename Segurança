const int button1 = 2; //Primeiro botão no pino 2.
const int button2 = 3; //Segundo botão no pino 3.
const int button3 = 4; //Terceiro botão no pino 4.
const int button4 = 5; //Quarto botão no pino 5.
const int button5 = 6; //Quinto botão no pino 6.
const int button6 = 7; //Sexto botão no pino 7.
const int LED[] = {14,15,16,17,18,19};

const int Red = 8; //Led vermelho de não pino 8.
const int greenLed = 9; //Led verde de sim pino 9.
void checkEntered1(int button);

int code[] = {1,4,2,3,2,6}; //Senha para destravar.
                        

int entered[7]; 
                

void setup(){ //Iniciando o código.
  Serial.begin(9600);

  pinMode(button1, INPUT_PULLUP); //Setando Botão 1 como entrada.
  pinMode(button2, INPUT_PULLUP); //Setando Botão 2 como entrada.
  pinMode(button3, INPUT_PULLUP); //Setando Botão 3 como entrada.
  pinMode(button4, INPUT_PULLUP); //Setando Botão 4 como entrada.
  pinMode(button5, INPUT_PULLUP); //Setando Botão 5 como entrada.
  pinMode(button6, INPUT_PULLUP); //Setando Botão 6 como entrada.

  pinMode(Red, OUTPUT); //Setando o LED vermelho como saída.
  pinMode(greenLed, OUTPUT); //Setando o LED verde como saída.
  digitalWrite(Red, LOW); //Ligar LED vermelho
  for (int i = 0; i < 6;i++){ 
    Serial.println(code[i]); //Imprimir cada digito do código
    Serial.println(entered[i]); //Imprimir no monitor serial os códigos digitado.
                                
                                
    pinMode(LED[i],OUTPUT);
  }
}

void loop(){ //Executando o loop
  if (digitalRead(button1) == LOW){ //Se o botão 1 for precionado
    checkEntered1(1); //Chame a função checkEntered e mude o valor para 1
    
    delay(250);//Esperar um tempo para o funcionamento correto
               //Caso o contrario o botão será precionado mais de uma vez
    
  }
  else if (digitalRead(button2) == LOW){ //Se o botão 2 for precionado
    checkEntered1(2); //Chame a função checkEntered1 e mude o valor para 2
    
    delay(250); //Esperar um tempo para o funcionamento correto
               //Caso o contrario o botão será precionado mais de uma vez
    
  }
  else if (digitalRead(button3) == LOW){ //Se o botão 3 for precionado
    checkEntered1(3); //Chame a função checkEntered1 e mude o valor para 3
    
    delay(250); //Esperar um tempo para o funcionamento correto
               //Caso o contrario o botão será precionado mais de uma vez
    
  }
  else if (digitalRead(button4) == LOW){ //Se o botão 4 for precionado
    checkEntered1(4); //Chame a função checkEntered1 e mude o valor para 4
    
    delay(250); //Esperar um tempo para o funcionamento correto
               //Caso o contrario o botão será precionado mais de uma vez
    
  }
    else if (digitalRead(button5) == LOW){ //Se o botão 5 for precionado
    checkEntered1(5); //Chame a função checkEntered1 e mude o valor para 5
    
    delay(250); //Esperar um tempo para o funcionamento correto
               //Caso o contrario o botão será precionado mais de uma vez
    
  }
    else if (digitalRead(button6) == LOW){ //Se o botão 6 for precionado
    checkEntered1(6); //Chame a função checkEntered1 e mude o valor para 6
    
    delay(250); //Esperar um tempo para o funcionamento correto
               //Caso o contrario o botão será precionado mais de uma vez
    
  }
  

}

void checkEntered1(int button){ //Verifica o primeiro elemento da matriz "entered[]"
  digitalWrite(LED[button-1],HIGH);
  if (entered[0] != 0){ //Se não for zero, ele já foi inserido
    checkEntered2(button); //Passe para função checkEntered2, passando o elemento "button" declarado no inicio do código
  }
  
  else if(entered[0] == 0){ //Se for zero o botão não foi apertado ou definido
    entered[0] = button; //Defina o primeiro elemento como o botão que foi pressionado
    Serial.print("1: ");Serial.println(entered[0]); //Imprime na tela o botão, para debugar !!
  }
  
}

void checkEntered2(int button){ //Verifica o segundo elemento da matriz entered[]
  digitalWrite(LED[button-1],HIGH);
  if (entered[1] != 0){ //Se não for zero, ele já foi inserido
    checkEntered3(button); //Passe para função checkEntered3, passando o elemento "button" declarado no inicio do código
  }
  
  else if(entered[1] == 0){ //Se for zero o botão não foi apertado ou definido
    entered[1] = button; //Defina o segundo elemento como o botão que foi pressionado
    Serial.print("2: ");Serial.println(entered[1]); //Imprime na tela o botão, para debugar !!
  }
  
}

void checkEntered3(int button){  //Verifica o terceiro elemento da matriz entered[]
  digitalWrite(LED[button-1],HIGH);
  if (entered[2] != 0){ //Se não for zero, ele já foi inserido
    checkEntered4(button); //Passe para função checkEntered4, passando o elemento "button" declarado no inicio do código
  }
  
  else if (entered[2] == 0){ //Se for zero o botão não foi apertado ou definido
    entered[2] = button; //Defina o terceiro elemento como o botão que foi pressionado
    Serial.print("3: ");Serial.println(entered[2]); //Imprime na tela o botão, para debugar !!
  }
  
}

void checkEntered4(int button){  //Verifica o quarto elemento da matriz entered[]
  digitalWrite(LED[button-1],HIGH);
  if (entered[3] != 0){ //Se não for zero, ele já foi inserido
    checkEntered5(button); //Passe para função checkEntered5, passando o elemento "button" declarado no inicio do código
  }
  
  else if (entered[3] == 0){ //Se não for zero, ele já foi inserido
    entered[3] = button; //Defina o quarto elemento como o botão que foi pressionado
    Serial.print("4: ");Serial.println(entered[3]); //Imprime na tela o botão, para debugar !!
  }
  
}


void checkEntered5(int button){  //Verifica o quinto elemento da matriz entered[]
  digitalWrite(LED[button-1],HIGH);
  if (entered[4] != 0){ //Se não for zero, ele já foi inserido
    checkEntered6(button); //Passe para função checkEntered6, passando o elemento "button" declarado no inicio do código
  }
  
  else if (entered[4] == 0){ //Se for zero o botão não foi apertado ou definido
    entered[4] = button; //Defina o quinto elemento como o botão que foi pressionado
    Serial.print("5: ");Serial.println(entered[4]); //Imprime na tela o botão, para debugar !!
  }
  
}

void checkEntered6(int button){ //Verifica o sexto elemento da matriz entered[]
  digitalWrite(LED[button-1],HIGH);
  if (entered[5] == 0){ //Se não for zero, ele já foi inserido
    entered[5] = button; //Defina o sexto e ultimo elemento como o botão que foi pressionado
    Serial.print("6: ");Serial.println(entered[5]); //Imprime na tela o botão, para debugar !!
    delay(100); //Tempo para processar
    compareCode(); //Chamar a função "compareCode"
  }
}

void compareCode(){ //Compara o codigo inserido pelo usuario com o código declarado na matriz.
  for (int i = 0; i<6;i++){ 
    Serial.println(entered[i]);
  }
  if ((entered[0]==code[0]) && (entered[1]==code[1]) && (entered[2]==code[2]) && (entered[3]==code[3]) && (entered[4]==code[4])&& (entered[5]==code[5])){ //if all the elements of each array are equal
    digitalWrite(Red, LOW); // Desligue os LED vermelho
    digitalWrite(greenLed, HIGH); //Ligue o LED verde
    delay(1000); //Espere um tempo
    digitalWrite(greenLed, LOW); //Desligue o LED verde


    
    for (int i = 0; i < 7; i++){ //Esse próximo loop é só para fins debugação.
      entered[i] = 0;
      
    }
   
    loop(); 
  }
  
  else { //Caso o código inserido esteja errado
    
    digitalWrite(Red,HIGH);
    delay(1000);
    digitalWrite(Red,LOW);
    Serial.println("Red OFF");
    for (int i = 0; i < 7; i++){ //Esse próximo loop é só para fins debugação.
      entered[i] = 0;
     
    }
    
  }
  close_all();
}



void close_all(){
digitalWrite(LED[0],LOW);
digitalWrite(LED[1],LOW);
digitalWrite(LED[2],LOW);
digitalWrite(LED[3],LOW);
digitalWrite(LED[4],LOW);
digitalWrite(LED[5],LOW);
}
