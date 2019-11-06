# Eventos y Delegados 

El jugador genera una explosión que hace que todos los enemigos disminuyan su tamaño y se aplica una fuerza a determinados obstáculos.

## Jugador

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

  }
  ```
  
  
## Enemigos
```csharp

using UnityEngine;
using System.Collections;

public class MiEventoScript : MonoBehaviour
{
float newscale =0.2f;
public GameObject micharacter;
    Start()
    {
    // Recuperar el jugador
      micharacter = GameObject.Find("Player");
      micharacter.onBangXXL += Reduce;
    }


    void OnDisable()
    {
        micharacter.OnBangXXL -= Reduce;
    }


    void Reduce()
    {

      transform.localScale = new Vector2(newscale, newscale);

    }
}
```

## Objetos

```csharp

using UnityEngine;
using System.Collections;

public class MiEventoScript : MonoBehaviour
{
  float newscale =0.2f;
  public GameObject micharacter;
  private Rigidbody2D rb;
  private float force = 10.0f;

    Start()
    {
    // Recuperar el jugador
      micharacter = GameObject.Find("Player");
      micharacter.onBangXXL += Fuerza;
      rb = GetComponent<Rigidbody2D>();
    }


    void OnDisable()
    {
        micharacter.OnBangXXL -= Fuerza;
    }


    void Fuerza()
    {

      rb.AddForce(transform.up * force);

    }
}
```
