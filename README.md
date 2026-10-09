# pruebas-de-software
materia de 2do semestre

ejercicio 1 :
<img width="1903" height="1032" alt="image" src="https://github.com/user-attachments/assets/ee925e3b-b19b-4972-9ea2-e67ed3302bc1" />
codigo :
import java.util.Scanner;

class Kata {
    static String greet(String name, String owner) {
        Scanner sc = new Scanner(System.in);

        if (name.equals(owner)) {
            return "Hello boss";
        } else {
            return "Hello guest";
        }
    }
}

ejercicio 2;
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/d0432dca-036f-4fe7-ae3c-4d7b739dc900" />
public class Kata {
  
  public static boolean zeroFuel(double distanceToPump, double mpg, double fuelLeft) {

            return distanceToPump <= mpg * fuelLeft;
  }
  
}

ejercicio 3 ;
<img width="1905" height="1079" alt="image" src="https://github.com/user-attachments/assets/1c24c4b7-a816-4beb-99a0-3cab96dcf876" />

public class Kata {
    public static int[] invert(int[] array) {
        for (int i = 0; i < array.length; i++) {
            array[i] = -array[i];
        }
        return array;
    }
}

ejercicio 4: 
<img width="1871" height="972" alt="image" src="https://github.com/user-attachments/assets/5af2726e-681a-4286-a494-a12a0286f3f7" />
public class StringSplit {
    public static String[] solution(String s) {
        if (s.length() % 2 != 0) {
            s += "_";
        }

        String[] result = new String[s.length() / 2];

        for (int i = 0; i < s.length(); i += 2) {
            result[i / 2] = s.substring(i, i + 2);
        }

        return result;
    }
}


ejercicio 5 :

<img width="1896" height="1017" alt="image" src="https://github.com/user-attachments/assets/0f145b52-6f96-40ab-a4ce-a644d086d728" />

public class CountingDuplicates {
    public static int duplicateCount(String text) {
        int[] frequency = new int[36];
        int duplicates = 0;

        for (char c : text.toLowerCase().toCharArray()) {
            int index = Character.isDigit(c)
                    ? c - '0' + 26
                    : c - 'a';

            if (++frequency[index] == 2) {
                duplicates++;
            }
        }

        return duplicates;
    }
}

ejercicio 6:
<img width="1873" height="926" alt="image" src="https://github.com/user-attachments/assets/d8fa88f8-63b2-414b-a0fb-f0bf4d538d57" />

public class Vowels {
    public static int getCount(String str) {
        int count = 0;

        for (int i = 0; i < str.length(); i++) {
            if ("aeiou".indexOf(str.charAt(i)) != -1) {
                count++;
            }
        }

        return count;
    }
}

ejercicio 7:
<img width="1888" height="921" alt="image" src="https://github.com/user-attachments/assets/8428ca45-22c7-466d-a372-552dfe20179a" />
public class XO {
    public static boolean getXO(String str) {
        int count = 0;

        for (int i = 0; i < str.length(); i++) {
            char c = Character.toLowerCase(str.charAt(i));

            if (c == 'x') {
                count++;
            } else if (c == 'o') {
                count--;
            }
        }

        return count == 0;
    }
}

ejercicio 8:
<img width="1887" height="928" alt="image" src="https://github.com/user-attachments/assets/b0e349c8-fcf9-4abd-a28e-fe0eb2c37326" />
public class Kata {
    public static int findEvenIndex(int[] arr) {
        int rightSum = 0;
        int leftSum = 0;

        for (int num : arr) {
            rightSum += num;
        }

        for (int i = 0; i < arr.length; i++) {
            rightSum -= arr[i];

            if (leftSum == rightSum) {
                return i;
            }

            leftSum += arr[i];
        }

        return -1;
    }
}

ejercicio 9:
<img width="1882" height="929" alt="image" src="https://github.com/user-attachments/assets/4ce623d0-393e-44ee-8d66-6a5f3e338305" />
public class Kata {
    public static int[] sortArray(int[] array) {
        int[] oddNumbers = java.util.Arrays.stream(array)
                .filter(n -> n % 2 != 0)
                .sorted()
                .toArray();

        int index = 0;

        for (int i = 0; i < array.length; i++) {
            if (array[i] % 2 != 0) {
                array[i] = oddNumbers[index++];
            }
        }

        return array;
    }
}

ejercicio 10:
<img width="1895" height="965" alt="image" src="https://github.com/user-attachments/assets/82a7d9d5-32c3-4ead-afe7-300a6c4369ee" />
**
import java.util.ArrayList;
import java.util.List;
public class MexicanWave {
    public static String[] wave(String str) {
        List<String> result = new ArrayList<>();
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) == ' ') {
                continue;
            }

            String wave = str.substring(0, i)
                    + Character.toUpperCase(str.charAt(i))
                    + str.substring(i + 1);

            result.add(wave);
        }

        return result.toArray(new String[0]);
    }
}**


