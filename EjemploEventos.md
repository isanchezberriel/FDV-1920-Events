#Eventos y Delegados 


```csharp

using UnityEngine;
using System.Collections;

public class MiEventoScript : MonoBehaviour
{

  public GameObject micharacter;
  public delegate void Bomb();
  public event Bomb onBombXXL;
    Start()
    {


    }

    Update(){
      //Cuando se dan las condiciones, el jugador tira la bomba, se envía else {
      //mensaje a los suscriptores
      }
      if(bomb){
        onBombXXL();
      }

    }

  }```
