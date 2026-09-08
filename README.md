# practice-kitar

Lab 2

# Wiam Kitar

### Ty Burrell

I like Ty Burrell because of his acting in the TV Show **Modern Family**. He had the role of Phil Dunphy, a very funny character and I grew to love him. **He's a very good actor**, his acting is very **realistic** and he makes me laugh every time i watch him.

---

## My Favorite Films

1. The Odyssey
2. Spider-Man: Brand New Day
3. The Housemaid
4. The Notebook

- Save Your Tears by the Weeknd
- Hey There Delilah by Plain White T's
- Treat You Better by Shawn Mendes

[Read about my favorite city](MyCity.md)

---

## Cities I want to visit

There are so many places I want to visit around the world. If I had to pick 4 cities only, I would choose: Tokyo, Nashville, Rome and Singapore.
|City|Why I want to visit|Distance from NYC|Cost of travel from NYC|
|---|---|---|---|
|Tokyo|I would love to experience Japanese culture, try authentic Japanese food, and explore the city's mix of modern technology and traditional architecture. |6740 miles|$1000+|
|Nashville|I want to experience the city's music scene, especially its famous country music culture, while exploring the city itself.|760 miles|$200+|
|Rome|I want to see Rome's ancient history and famous landmarks and eat italian food|4270 miles|4600+|
|Singapore|I would love to experience its modern skyline, diverse cultures, food, and mix of Asian traditions and modern city life.|9530 miles|$1000+|

---

## Favorite Jokes

Gary Delaney:

> As a kid I was made to walk the plank. We couldn't afford a dog.

Tomy Cooper:

> I used to be indecisive. Now I'm not so sure.

Jack Handey:

> I want to die peacefully in my sleep like my grandfather, not screaming like the passengers in his car.

---

## Code Fencing

This snippet models a playing die with sides numbered 1 to N.

````import java.util.Random;

/**
 * Models a playing die with sides numbered 1 to N.
 * All sides have uniform probablity of being rolled.
 *
 * @author Summer CS 307 class
 */
public class Die
{   public static final int DEFAULT_SIDES = 6;

    private static Random ourRandNumGen = new Random();

    private final int iMyNumSides;
    private int iMyResult;


    /**
     * Default constructor.<p>
     * pre: none<br>
     * post: getNumSides() = DEFAULT_SIDES, getResult() = 1
     */
    public Die()
    {   this(DEFAULT_SIDES);
    }


    /**
     * Create a Die with numSides sides<p>
     * pre: numSides > 1<br>
     * post: getNumSides() = numSides, getResult() = 1<br>
     * An exception will be generated if the preconditions are not met
     */
    public Die(int numSides)
    {   assert numSides > 1 : "Violation of precondition: numSides = " + numSides + "numSides must be greater than 1";

        iMyNumSides = numSides;
        iMyResult = 1;
        assert getResult() == 1 && getNumSides() == numSides;
    }


    /**
     * Create a Die with numSides and top side and result set to result<p>
     * pre: numSides > 1, 1 <= result <= numSides<br>
     * post: getNumSides() = numSides, getResult() = 1<br>
     * An exception will be generated if the preconditions are not met
     */
    public Die(int numSides, int result)
    {   assert numSides > 1 && 1 <= result && result <= numSides : "Violation of precondition";

        iMyNumSides = numSides;
        iMyResult = result;
    }


    /**
     * roll this Die. Every side has an equal chance of being the new result<p>
     * pre: none<br>
     * post: 1 <= getResult() <= getNumSides()
     * @return the result of the Die after the roll
     */
    public int roll()
    {   iMyResult = ourRandNumGen.nextInt(iMyNumSides) + 1;

        assert ( 1 <= getResult() ) && ( getResult() <= getNumSides() );

        return iMyResult;
    }


    /**
     * return how many sides this Die has<p>
     * pre: none<br>
     * post: return how many sides this Die has
     * @return the number of sides on this Die
     */
    public int getNumSides()
    {   return iMyNumSides; }


    /**
     * get the current result or top number of this Die<p>
     * pre: none<br>
     * post: return the number on top of this Die
     * @return the current result of this Die
     */
    public int getResult()
    {   return iMyResult;   }


    /**
     * returns true if this Die and the parameter otherObj are equal<p>
     * pre: none<br>
     * post: return true if the parameter is a Die object with the same number of sides as this Die and currently has the same result.
     * @return true if the the two Dice are equal, false otherwise
     */
    public boolean equals(Object otherObj)
    {   boolean result = true;
        if(otherObj == null)
            result = false;
        else if(this == otherObj)
            result = true;
        else if(this.getClass() != otherObj.getClass())
            result = false;
        else
        {   Die otherDie = (Die)otherObj;
            result = this.iMyResult == otherDie.iMyResult
                && this.iMyNumSides == otherDie.iMyNumSides;
        }
        return result;
    }


    /**
     * returns a String containing information about this Die<p>
     * pre: none<br>
     * post: return a String with information about the current state of this Die
     * @return: A String with the number of sides and current result of this Die
     */
    public String toString()
    {   return "Num sides " + getNumSides() + " result " + getResult();
    }


}// end of Die class```

Snippet Source: <https://www.cs.utexas.edu/~scottm/cs307/javacode/codeSamples/Die.java>
````
