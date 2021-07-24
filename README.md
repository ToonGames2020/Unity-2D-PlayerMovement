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
