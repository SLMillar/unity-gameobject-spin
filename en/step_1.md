![The Game view showing a Heart GameObject spinning about its y-axis.](images/spinning-heart.gif)

In the Inspector window for the GameObject, click **Add Component** and choose **New script**, then give your script a sensible name (for example, `ItemController`).

Double-click on your new script to open it in the code editor.

Create a variable to control the `spinSpeed` and add code to spin your GameObject:

--- code ---
---
language: cs
---

    public float spinSpeed = 5.0f; 

    // Update is called once per frame
    void Update()
    {
        transform.Rotate(Vector3.forward * spinSpeed); // You can also spin backward, up, down, left, and right
    }

--- /code ---

You can rotate about the x-, y-, or z-axis by amending the direction in your code:
+ `Vector3.right` or `Vector3.left` = Rotation about the x-axis
+ `Vector3.up` or `Vector3.down` = Rotation about the y-axis
+ `Vector3.forward` or `Vector3.back` = Rotation about the z-axis

**Tip:** If you have added a Particle System to your GameObject, change the 'Simulation Space' property in the Inspector window to `World` so that it does not spin with your GameObject.
