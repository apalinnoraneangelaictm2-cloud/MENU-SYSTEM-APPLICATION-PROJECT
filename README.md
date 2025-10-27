package menudrivengroup5;
import java.util.*;
public class MenuDrivenApp {
   // Cute Pastel Colors
   public static final String RESET = "\033[0m";
   public static final String PINK = "\033[95m";
   public static final String CYAN = "\033[96m";
   public static final String YELLOW = "\033[93m";
   public static final String GREEN = "\033[92m";
   public static final String PURPLE = "\033[35m";
   public static final String WHITE = "\033[97m";
   public static final String BLUE = "\033[94m";
   public static final String BG_PINK = "\033[105m";
   public static final String BG_WHITE = "\033[47m";
   public static final String BG_CYAN = "\033[106m";
   public static final String BG_RED = "\033[41m";
   public static final String BOLD = "\033[1m";
  
   static Scanner sc = new Scanner(System.in);
   static int option;
   static double num1, num2, radius, Cm, result, result2;
   static boolean exit = false;
   
   public static void main(String[] args) throws InterruptedException {
       loading();
       Clearscreen();
       StartScreen();
       while (!exit) {
           try {
               option = sc.nextInt();
               if (option > 3 || option < 0) {
                   Clearscreen();
                   CuteError();
               }
           } catch (InputMismatchException e) {
               sc.nextLine();
           }
       }
   }
   
   public static void StartScreen() throws InterruptedException {
       System.out.println("\n\n\n");
       System.out.println(PINK +"\t\t\t\t\tâ•”â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•—");
       System.out.println(PINK + "\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(PINK + "\t\t\t\t\tâ•‘          â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡          â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘            â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡            â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘              â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡              â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘                â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡                â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘                  â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡                  â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(CYAN + "\t\t\t\t\tâ•‘                        âˆ§ï¼¿âˆ§                             â•‘" + RESET);
       System.out.println(CYAN + "\t\t\t\t\tâ•‘                      (ï½¡ï½¥Ï‰ï½¥ï½¡)ï¾‰                         â•‘" + RESET);
       System.out.println(CYAN + "\t\t\t\t\tâ•‘                      /    ã¥â™¡                           â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(YELLOW + BOLD + "\t\t\t\t\tâ•‘              âœ¿ KAWAII MENU SYSTEM âœ¿                     â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(WHITE + BOLD +"\t\t\t\t\tâ•‘                  [1] ðŸ“‹ Menu                            â•‘");
       System.out.println(WHITE + BOLD +"\t\t\t\t\tâ•‘                  [2] ðŸ’– About Us                        â•‘");
       System.out.println(WHITE + BOLD +"\t\t\t\t\tâ•‘                  [3] ðŸ‘‹ Exit                            â•‘");
       System.out.println(PINK + "\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(PINK + "\t\t\t\t\tâ•‘                  â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡                  â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘                â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡                â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘            â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡            â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘          â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡          â•‘" + RESET);
       System.out.println("\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(PINK +"\t\t\t\t\tâ•šâ•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•");
       System.out.print("\n" + PINK + BOLD + "\t\t\t\t\t\tChoose your option: " + RESET);
       
       try {
           option = (int) getUserInput1();
           switch (option) {
               case 1:
                   Start();
                   break;
               case 2:
                   Aboutus();
                   break;
               case 3:
                   Exit();
                   break;
               default:
                   Clearscreen();
                   CuteError();
                   break;
           }
       } catch (InputMismatchException e) {
           Clearscreen();
           sc.nextLine();
           CuteError();
       }
   }
   
   public static void Start() throws InterruptedException {
       Clearscreen();
       System.out.println("\n\n\n");
       System.out.println("\t\t\t\t\tâ•”â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•—");
       System.out.println("\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘         â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…         â•‘" + RESET);
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘           â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…           â•‘" + RESET);
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘             â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…             â•‘" + RESET);
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘               â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…               â•‘" + RESET);
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘                 â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…                 â•‘" + RESET);
       System.out.println("\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(PINK + "\t\t\t\t\tâ•‘                      âˆ§,,,âˆ§                              â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘                    ( Ì³â€¢ Â· â€¢ Ì³)                            â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\t\tâ•‘                    /    ã¥â™¡                             â•‘" + RESET);
       System.out.println("\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(CYAN + BOLD + "\t\t\t\t\tâ•‘                 âœ¨ FEATURES MENU âœ¨                      â•‘" + RESET);
       System.out.println("\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(YELLOW + "\t\t\t\t\tâ•‘              [1] âœ¨ Calculator                          â•‘" + RESET);
       System.out.println(YELLOW + "\t\t\t\t\tâ•‘              [2] ðŸ“ Conversion                          â•‘" + RESET);
       System.out.println(YELLOW + "\t\t\t\t\tâ•‘              [3] ðŸ”¢ Odd & Even                          â•‘" + RESET);
       System.out.println(YELLOW + "\t\t\t\t\tâ•‘              [4] â­• Circle Magic                        â•‘" + RESET);
       System.out.println(YELLOW + "\t\t\t\t\tâ•‘              [5] ðŸ”™ Back                               â•‘" + RESET);
       System.out.println(YELLOW + "\t\t\t\t\tâ•‘              [6] ðŸ‘‹ Exit                               â•‘" + RESET);
       System.out.println("\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘                 â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…                 â•‘" + RESET);
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘               â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…               â•‘" + RESET);
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘             â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…             â•‘" + RESET);
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘           â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…           â•‘" + RESET);
       System.out.println(PURPLE + "\t\t\t\t\tâ•‘         â˜…â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â”â˜…         â•‘" + RESET);
       System.out.println("\t\t\t\t\tâ•‘                                                          â•‘");
       System.out.println("\t\t\t\t\tâ•šâ•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•");
       System.out.print("\n" + WHITE + BOLD + "\t\t\t\t\t\tChoose your option: " + RESET);
       
       try {
           option = (int) getUserInput1();
           switch (option) {
               case 1:
                   Clearscreen();
                   Calculator();
                   break;
               case 2:
                   Clearscreen();
                   Conversion();
                   break;
               case 3:
                   Clearscreen();
                   OddEven();
                   break;
               case 4:
                   Clearscreen();
                   CircleCalc();
                   break;
               case 5:
                   Clearscreen();
                   StartScreen();
                   break;
               case 6:
                   Clearscreen();
                   Exit();
                   break;
               default:
                   Clearscreen();
                   CuteError();
                   break;
           }
       } catch (InputMismatchException e) {
           Clearscreen();
           sc.nextLine();
           CuteError();
       }
   }
   
   public static void loading() throws InterruptedException {
       String[] faces = {"(â—¡ Ï‰ â—¡)", "( â—¡ Ï‰ â—¡ )", "( â—¡  Ï‰  â—¡ )", "( â—¡ Ï‰ â—¡ )", "(â—¡ Ï‰ â—¡)"};
       
       for (int cycle = 0; cycle < 3; cycle++) {
           for (int frame = 1; frame <= 10; frame++) {
               Clearscreen();
               System.out.println("\n\n\n");
               System.out.println(PINK + "\t\t\t\tâ•”â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•—");
               System.out.println(PINK + "\t\t\t\tâ•‘                                                                    â•‘");
               System.out.println(PINK + BOLD + "\t\t\t\tâ•‘               â™¡âœ¿.ï½¡.:* KAWAII LOADING SCREEN *.:ï½¡.âœ¿â™¡                â•‘" + RESET);
               System.out.println(PINK +  "\t\t\t\tâ•‘                                                                    â•‘");
               System.out.println(PINK + "\t\t\t\tâ•‘                              ï¼lã€                                 â•‘" + RESET);
               System.out.println(PINK + "\t\t\t\tâ•‘                            ï¼ˆï¾Ÿï½¤ ï½¡ ï¼—                               â•‘" + RESET);
               System.out.println(PINK + "\t\t\t\tâ•‘                              l  ~ãƒ½                                â•‘" + RESET);
               System.out.println(PINK + "\t\t\t\tâ•‘                              ã˜ã—f_,)ãƒŽ                            â•‘" + RESET);
               System.out.println(PINK + "\t\t\t\tâ•‘                                                                    â•‘");
               System.out.println(YELLOW + "\t\t\t\tâ•‘                             " + faces[frame % faces.length] + "                            â•‘" + RESET);
               System.out.println(PINK + "\t\t\t\tâ•‘                                                                    â•‘");
               System.out.print(GREEN + "\t\t\t\tâ•‘    LOADING: [");
               for (int i = 0; i < 20; i++) {
                   if (i < (frame * 2)) {
                       System.out.print("â™¥");
                   } else {
                       System.out.print("â™¡");
                   }
               }
               System.out.println("] " + (frame * 10) + "% â•‘" + RESET);
               System.out.println(PINK + "\t\t\t\tâ•‘                                                                    â•‘");
               System.out.print(PURPLE + BOLD + "\t\t\t\tâ•‘                           Loading");
               for (int i = 0; i < (frame % 4); i++) {
                   System.out.print(".");
               }
               for (int i = 0; i < (3 - (frame % 4)); i++) {
                   System.out.print(" ");
               }
               System.out.println("                     	     â•‘" + RESET);
               System.out.println(PINK + "\t\t\t\tâ•‘                                                                    â•‘");
               String[] messages = {
                   "Preparing kawaii interface...",
                   "Loading cute animations...",
                   "Setting up pastel colors...",
                   "Initializing heart decorations...",
                   "Activating kawaii mode...",
                   "Loading adorable features...",
                   "Preparing cute calculations...",
                   "Setting up magical circles...",
                   "Loading conversion magic...",
                   "Almost ready! â™¡"
               };
               System.out.println(YELLOW + "\t\t\t\tâ•‘           	" + messages[frame - 1] + "                       â•‘" + RESET);
               System.out.println(PINK + "\t\t\t\tâ•‘                                                                    â•‘");
               System.out.println(PINK + "\t\t\t\tâ•šâ•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•");
               System.out.println(PINK + "\t\t\t\t\t\t    â™¡ â™¡ â™¡ â™¡ â™¡ â™¡ â™¡ â™¡ â™¡ â™¡ â™¡ â™¡ â™¡ â™¡" + RESET);
               Thread.sleep(300);
           }
       }
       
       Clearscreen();
       System.out.println("\n\n\n");
       System.out.println(GREEN + BOLD + "\t\t\t\tâ•”â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•—" + RESET);
       System.out.println(GREEN + "\t\t\t\tâ•‘                                                                    â•‘" + RESET);
       System.out.println(GREEN + BOLD + "\t\t\t\tâ•‘                        âœ¨ LOADING COMPLETE! âœ¨                     â•‘" + RESET);
       System.out.println(GREEN + "\t\t\t\tâ•‘                                                                    â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\tâ•‘                             âˆ§ï¼¿âˆ§                                   â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\tâ•‘                           (ï½¡ï½¥Ï‰ï½¥ï½¡)ï¾‰â™¡                                â•‘" + RESET);
       System.out.println(PINK + "\t\t\t\tâ•‘                           /    ã¥                                  â•‘" + RESET);
       System.out.println(GREEN + "\t\t\t\tâ•‘                                                                    â•‘" + RESET);
       System.out.println(YELLOW + "\t\t\t\tâ•‘                    Welcome to Kawaii Menu System!                  â•‘" + RESET);
       System.out.println(GREEN + "\t\t\t\tâ•‘                                                                    â•‘" + RESET);
       System.out.println(GREEN + "\t\t\t\tâ•šâ•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•" + RESET);
       Thread.sleep(1500);
   }
   
   public static void Aboutus() throws InterruptedException {
       Clearscreen();
       System.out.println("\n\n\n");
       System.out.println(GREEN + "\t\t\tâ•”â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•â•—");
       System.out.println(GREEN + "\t\t\tâ•‘                                                             â•‘");
       System.out.println(CYAN + "\t\t\tâ•‘           â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡            â•‘" + RESET);
       System.out.println(CYAN + "\t\t\tâ•‘             â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡               â•‘" + RESET);
       System.out.println(CYAN + "\t\t\tâ•‘               â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡                 â•‘" + RESET);
       System.out.println(CYAN + "\t\t\tâ•‘                 â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡                    â•‘" + RESET);
       System.out.println(CYAN + "\t\t\tâ•‘                   â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡_â™¡                      â•‘" + RESET);
       System.out.println(GREEN + "\t\t\tâ•‘                                                             â•‘");
       System.out.println(PINK + "\t\t\tâ•‘                           âˆ§ï¼¿âˆ§                              â•‘" + RESET);
       System.out.println(PINK + "\t\t\tâ•‘                          (ï½¡ï½¥Ï‰ï½¥ï½¡)                            â•‘" + RESET);
       System.out.println(PINK + "\t\t\tâ•‘                          /    ã¥â™¡                           â•‘" + RESET);
       System.out.println(GREEN + "\t\t\tâ•‘                                                             â•‘");
       System.out.println(YELLOW + BOLD + "\t\t\tâ•‘                      ðŸ’– ABOUT US ðŸ’–                         â•‘" + RESET);
       System.out.println(GREEN + "\t\t\tâ•‘                                                             â•‘");
       System.out.println(GREEN + "\t\t\tâ•‘                  Menu Drive System Application              â•‘" + RESET);
       System.out.println(GREEN + "\t\t\tâ•‘      This Application helps you do simple equations         â•‘" + RESET);
       System.out.println(GREEN + "\t\t\tâ•‘           Just like a simple Scientific Calculator!         â•‘" + RESET);
       System.out.println(GREEN + "\t\t\tâ•‘                                                             â•‘");
       System.out.println(PINK + BOLD +"\t\t\tâ•‘                    âœ¨ Developers âœ¨                         â•‘");
       System.out.println(PINK + BOLD +"\t\t\tâ•‘                â€¢ Romay        â€¢ Apalin                      â•‘");
       System.out.println(PINK + BOLD +"\t\t\tâ•‘                â€¢ Villanueva   â€¢ Cualbar                     â•‘");
       System.out.println(PINK + BOLD +"\t\t\tâ•‘                â€¢ Bobis        â€¢ Jardio                      â•‘");
       System.out.println(PINK + BOLD +"\t\t\tâ•‘                â€¢
