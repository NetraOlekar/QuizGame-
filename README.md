# QuizGame-
new repository
import java.util.Scanner;
 
public class QuizGame {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int score = 0;
        String[] questions = {
            "What is the PH value of the human body",
            "Who painted the Mona Lisa?",
            "Forming of Association in india is"
        };
        String[] options = {
            "a) 9.2 to 9.8\tb) 7.0 to 7.8\tc) 6.1 to 6.3",
            "a) Michelangelo\tb) Leonardo da Vinci\tc) Pablo Picasso",
            "a) Legal Right\tb) Illegal Right\tc) Natural Right\td) Fundamental Right"
        };
        String[] answers = {"a", "b", "a","d"};
 
        System.out.println("Welcome to  the QUIZGAME,Let's start Now");
        System.out.println("Choose the correct answer for MCQ questions:");
 
        for (int k = 0; k < questions.length; k++) {
            System.out.println("\nQuestion " + (k + 1) + ": " + questions[k]);
            System.out.println("Options: " + options[k]);
            System.out.print("Your answer: ");
            String userAnswer = sc.nextLine().toLowerCase();
 
            if (userAnswer.equals(answers[k])) {
                System.out.println("Correct!");
                score++;
            } else {
                System.out.println("Incorrect. The correct answer is: " + answers[k]);
            }
        }
 
        System.out.println("\nQuiz completed! Your final score: "
                             + score + " out of " + questions.length);
        if (score == questions.length) {
            System.out.println("Congratulations! You've won the QUIZ!");
        }
        sc.close();
    }
}
