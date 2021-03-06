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

3. In this example, it has two different functions below "void Start ()". One is for "TotalAttack" (sword & magic), and the other for "TotalDefense" (shield & armor). Each integer is combined in their functions, and prints the total number for each function.

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

4. Similar to #1, floats are used instead of integers, and are multiplied instead of being added.

public class FuncReturn : MonoBehaviour {

  public float cash = 0.0f;
  public float hours = 0.0f;

  void Start()
  {
    float num = cash * hours;
    print("Since your payrate is $" + cash + ", and you've worked for " + hours + " hours; you have earned " + num + " dollars.");
  }
}

5. Similar to #1 & #2, the result of the total amount of clones is from "GoodClone" subtracting "EvilClone" instead of adding. And for some reason, if the value of "EvilClone" is higher than the "GoodClone" when subtracting, it will print a negative number.

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

6. Based on today's class (7/5/2017). Creating & using GameObjects in Unity (and its PlayMode), if you have one that's just holding this script, and other GameObjects named "enemy" touch the Collider, then the console will print "Adding Health". If it's not named "enemy", then it won't print "Adding Health".

public class FuncReturn : MonoBehaviour {

  void OnTriggerEnter (Collider _col)
  {
    print(_col.name);
    if(_col.name != "enemy")
    {
      _col.gameObject.SetActive(false);
    }
    else
    {
      print("Adding Health");
    }
  }

7. Based on today's class (7/5/2017). This is one way to create "placeholders" in the script for Unity's Inspector, but this is also meant to "UseData" and print it on the Unity Console. To see the way it works, for example, you have the "_s" next to "string", that "string" is also at the top of the script, which has the function 'myName = "Tony";', and one of the functions below the "void Start ()" is "UseData(myName);". So where it says 'print(_s + ", Hello.");', the console will read "Tony, Hello.".

public class FuncReturn : MonoBehaviour {

  public string myName = "Tony";
	public int myScore = 2;
  
	void Start () {
		UseData(myName);
		UseData(myScore);
	}
	
  void UseData(string _s)
	{
		print(_s + ", Hello.");
	}
	
  void UseData (int _i)
	{
		print(_i * 10);
	}

8. Similar to #1 & #2.

public class FuncReturn : MonoBehaviour {
  public int Fruit;
  public int Apparel;
  public int Entertainment;

  void Start(){
    int num = TotalItems(Fruit, Apparel, Entertainment);
    print(num);
  }

  public int TotalItems(int Food, int Clothes, int VideoGames){
    int result = Food + Clothes + VideoGames;

    return result;
  }
}

9. Similar to #1 & #2, only this time it has an if statement. You can plug in the values for both RedCards & BlackCards, but if the TotalCards is equal to num (which is assigned to 26), then it will print in the console.

public class FuncReturn : MonoBehaviour {

  public int RedCards;
  public int BlackCards;
  public int num = 26;

  void Start(){
    int num = TotalCards(RedCards, BlackCards);
    if(num == TotalCards)
    {
    	print("We have all 26 cards together");
    }
  }

  public int TotalCards(int Red, int Black){
    int result = Red + Black;

    return result;
  }
}

10. Based on today's class (7/5/2017). This "set" of examples shows different functions, such as when a video game is loading. "Awake" basically gets the game running or loading, "OnEnabled" is for loading the stages, characters, etc.; "Start" is, of course, starting the game. "OnDisabled" is when you are turning the "game" off. Now with the "Trigger" functions, if you have one of them hold this script, and while in PlayMode, if you move another GameObject into it, it will print "Enter". Afterwards (if you have "OnTriggerStay"), it will print "Staying" in the console while the GameObject is inside of the G.O. holding this script. Then it will print "Exit" once it leaves.

public class FuncReturn : MonoBehaviour {

	void Awake() 
	{
		print("Awake");
	}
	
	
	void OnEnable()
	{
		print("Enabled");
	}

	void Start()
	{
		print("Start");
	}

	void OnDisable()
	{
		print("Disabled");
	}

	void OnTriggerEnter()
	{
		print("Enter");
	}
	
	void OnTriggerStay()
	{
		print("Staying");
	}

	void OnTriggerExit()
	{
		print("Exit");
	}

}
