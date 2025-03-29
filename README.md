using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Player : MonoBehaviour
{

public GameObject bulletPrefab;

    void Start()
    {
        playerSpeed = 6f;
        
    }

    void Update()
    {
        Movement();
        Shooting();

    }

    void Shooting()
    {
        if(Input.GetKeyDown(KeyCode.Space))
        {
            Instantiate(bulletPrefab, transform.position + new Vector3(0, 1, 0), Quaternion.identity);
        }
    }
