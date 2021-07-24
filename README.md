# Unity-2D-PlayerMovement
This piece of code is what you need to move a 2D player. Paste this code into a C# script in unity. Remember, it can only be used on 2D games in C# scripts. This is the script:

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerMovement : MonoBehaviour{
    public float movementspeed;
    public Rigidbody2D rb;

    float mx;

    private void Update() {
        mx = Input.GetAxisRaw("Horizontal");
    }

    private void FixedUpdate() {
        Vector2 movement = new Vector2(mx * movementspeed, rb.velocity.y);

        rb.velocity = movement;
    }
}
