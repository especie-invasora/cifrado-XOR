# cifrado-XOR
este proyecto  fue realizado para hacer un proyecto XOR
#include <iostream>

using std :: cout;
 using std :: cin ;
  using  std :: endl; 
  
  void cifradoXOR();
  
 int main (){ 

 //int  a = 1; 
 //int b = 0;
 int option = 0 ;

 
 while(1){
     cout << "porfavor ingrse la opcion deseada";
 cout << "opcion 1 cifrado XOR," << endl;
 cout <<"opcion 2 decifrado con clave" << endl ;
 cout << "para salir del programa oprima 0" << endl;
 cin >> option;

     
     
      switch(option){
     case 1 :
     cout << "Usted a selecionado la opcion  numero 1 " << endl;
     void cifradoXOR();
     break;
     
     case 2: 
     cout <<"usted a selecionado la opcion  2 desifrado de codigo" ;
     void desifradoXOR();
     break;
     
    
     default:  
     cout << "gracias por participar, que tenga buen dia";
     break; 
     
     }
     
     //cout << "¿desea realizar algun otra operacion?, sidesa continuar oprima 1 y si no oprima 2";
     //cin >> b;
 
 }  
 
    
  
  
  }  
  
  void cifradoXOR()
{
    int ren, col, k=0, key=10;

    cout << "ingresar el tamano de la escitala: " << endl
    << "Renglones: ";
    cin >> ren;
    cout << "Columnas: ";
    cin >> col;

    char escitala[ren][col];
    char texto[ren*col];
    char keys[ren][col];

    for (int i = 0; i < ren; i++)
    {
        for (int j = 0; j < col; j++)
        {
            keys[i][j] = key;
        }
    }
    
    cout << "Escriba el texto a decifrar: " << endl;
    cin >> texto;

    for (int i = 0; i < ren; i++)
    {
        for (int j = 0; j < col; j++)
        {
            escitala[i][j] = texto[k++] ^ keys[i][j];
        }
    }
    
    cout << "El texto decifrado es: " << endl;
    for (int i = 0; i < ren; i++)
    {
        for (int j = 0; j < col; j++)
        {
            cout << escitala[i][j];
        }
    }
}
