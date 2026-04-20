using Unity.Android.Types;
using UnityEditor.Experimental.GraphView;
using UnityEngine;
using UnityEngine.InputSystem;

public class GameManager : MonoBehaviour
{
    [SerializeField]private int vida = 20;
    [SerializeField] private bool tieneLlave = false;
    void Start()
    {
        Debug.Log(gameObject.name);
        Debug.Log(gameObject.transform);
    }
    

    // Update is called once per frame
    void Update()
    {
         //imput.getkeydown(keycode.w)
        if(Keyboard.current.spaceKey.wasPressedThisFrame)
        {
            Debug.Log("la barra espaciadora fue presionada : ) ");
            if (tieneLlave == true && vida >= 5)
            {
                Debug.Log("puede entrar a la mazmorra");
            }
            else
            {
                Debug.Log("Git gud");
            }
             
         }
    }
}
