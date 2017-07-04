# HW_FucntionsWithReturn
Watch read and practice from the module: Functions. Write your understanding of the topic using comments and examples (at least 10 examples) to the instructor and describe them in your own words to the best of your knowledge. Put your work to GIT. Submit the GIT url to canvas.

1. According to Preston in class, he says that this example (function) is recommeneded when using Unity. Using "void" it won't print any values in the Unity Console, unless if you include a "print" function like below.

public class FuncReturn : MonoBehaviour {
  public int num1;
  public int num2;

  void Start(){
    int num = AddNumbers(num1, num2);
    print(num);
  }
}

2. According to Preston in class, he says that this function is just "Vanilla-C#", it does work, but not reccommended when using Unity. Simlar to #1, the "return" works the same as "print".

public class FuncReturn : MonoBehaviour {
  public int AddNumbers(int number1, int number2){
    int result = number1 + number2;

    return result;
  }
}

------------------------------------------------------------------------------------------------------------

NOTE: Before continuing with the examples, the script below has BOTH functions from above. When I tested with just the first example on my home computer, it says that "AddNumbers" doesn't exist in the current context. Then when I only used the second example, I don't get any errors, but the GameObject's script is just "blank" - you can't really do anything with it. BUT, when I have both of them together (as shown below), it works just fine. 

public class FuncReturn : MonoBehaviour {
  public int num1;
  public int num2;

  void Start(){
    int num = AddNumbers(num1, num2);
    print(num);
  }

  public int AddNumbers(int number1, int number2){
    int result = number1 + number2;

    return result;
  }
}
------------------------------------------------------------------------------------------------------------

3.

public class FuncReturn : MonoBehaviour {

  public int sword;
  public int magic;
  public int shield;
  public int armor;

  void Start()
  {
    int num1 = TotalAttack(sword, magic);
    int num2 = TotalDefense(shield, armor);
    print(num1 + " Attack Points & " + num2 + " Defense Points");
  }

  public int TotalAttack(int SwordAtk, int MagicAtk)
  {
    int Attack = SwordAtk + MagicAtk;
    return Attack;
  }

  public int TotalDefense(int ShieldDef, int ArmorDef)
  {
    int Defense = ShieldDef + ArmorDef;
    return Defense;
}

4.

public class FuncReturn : MonoBehaviour {

  public float cash = 0.0f;
  public float hours = 0.0f;

  void Start()
  {
    float num = cash * hours;
    print("Since your payrate is $" + cash + ", and you've worked for " + hours + " hours; you have earned " + num + " dollars.");
  }
}

5.

public class FuncReturn : MonoBehaviour {

public int GoodClone = 0;
public int EvilClone = 0;

  void Start()
  {
    int num = TotalClones(GoodClone, EvilClone);
    print("After the clone war of yourself, you started with " + GoodClone + " Good Clone(s), and " + EvilClone + " Evil Clone(s); now you have a total of " + num + " clone(s) leftover.");
  }

  public int TotalClones(int Good, int Evil)
  {
    int result = Good - Evil;
    return result;
  }
}

6.

public class FuncReturn : MonoBehaviour {

7.

public class FuncReturn : MonoBehaviour {

8.

public class FuncReturn : MonoBehaviour {

9.

public class FuncReturn : MonoBehaviour {

10.

public class FuncReturn : MonoBehaviour {
