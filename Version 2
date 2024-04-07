import java.util.*;
public class Version2
{
    static Scanner sc = new Scanner(System.in);
    static String blue = "\033[1;94m"; //blue text
    static String purple = "\033[1;95m";
    static String def = "\u001B[0m";  //default color
    static ArrayList<String> inventory = new ArrayList<String>();

    public static void main (String [] args)
    {
        System.out.print(purple + "📦Inventory for Dummies v.2.0 ---Made by Irish Manalo📦\n" + def);
        start();
    }
    static void start()
    {
        while (true)
        {
            //Asks for the users selection
            System.out.print("""
                    Hello! What would you like to do?
                    [A] Add an item✅
                    [C] Clear Inventory🧹
                    [D] Display items👁️
                    [S] Search for an item🔍
                    [R] Remove item/s🗑️
                    Choice:""");
            String choice = sc.next();

            if (choice.equalsIgnoreCase("A"))
            {
                addItem();
            }
            else if (choice.equalsIgnoreCase("S"))
            {
                searchItem();
            }
            else if (choice.equalsIgnoreCase("C"))
            {
                clearInv();
            }
            else if (choice.equalsIgnoreCase("D"))
            {
                displayItem();
            }
            else if (choice.equalsIgnoreCase("R"))
            {
                remove();
            }
            else
                System.out.println("☹Invalid Key☹\n");
        }
    }

    static void addItem() //For adding items in the inventory
    {
        String add;
        System.out.print("\n✅Add an item: ");
        add = sc.next();
        inventory.add(add);
        System.out.println(blue + "You have successfully added the item!\n" + def);
    }

    static void clearInv()//For clearing the items inside the inventory
    {
        if (inventory.isEmpty()) //Checks if the inventory is empty
        {
            System.out.println(blue + "🤔Looks like your inventory is empty \n😄I'll take you back to the menu\n\n" + def);
            start();
        }
        System.out.print("""
                ⚠️Are you sure you want to clear your inventory?   ⚠️
                You will loose all of the items inside the inventory
                [Y] Yes - proceed to clearing
                [N] No - let's get back to the menu
                Choice:""");
        String choice = sc.next();

        if (choice.equalsIgnoreCase("Y"))
        {
            inventory.clear();
            System.out.print(blue + "You've successfully deleted all of the items in your inventory!\n\n" + def);
        }
        else if (choice.equalsIgnoreCase("N"))
        {
            start();
        }
        else
            System.out.println("☹Invalid Key☹\n");
    }

    static void remove()//For removing items in the inventory
    {
        if (inventory.isEmpty()) //Checks if the inventory is empty
        {
            System.out.println(blue + "🤔Looks like your inventory is empty \n😄I'll take you back to the menu\n\n" + def);
            start();
        }

        System.out.print("What item do you want to delete?\n" + blue + inventory + def + "\nDelete: ");
        String choice = sc.next();

        if (inventory.contains(choice))
        {
            inventory.remove(choice);
            System.out.println(blue + "You have successfully deleted the item!" + def + "\nWould you like to display your inventory? \n [Y] Yes [N] No \nChoice: ");
            choice = sc.next();

            if (choice.equalsIgnoreCase("Y"))
            {
                displayItem();
            }
        }
        else
        {
            System.out.println("Sorry that item is not listed or wrong in spelling\n");
            start();
        }
    }
    public static void searchItem()//For searching an item inside the inventory
    {
        if (inventory.isEmpty()) //Checks if the inventory is empty
        {
            System.out.println(blue + "🤔Looks like your inventory is empty \n😄I'll take you back to the menu\n\n" + def);
            start();
        }
        else
        {
            System.out.print("\n🔍Search an item: ");
            String find = sc.next();

            int index = inventory.size();
            for (int i = 0; i < index; ) {
                if (inventory.contains(find)) {
                    System.out.println(blue + find + " found!\n" + def);
                } else {
                    System.out.println(blue + find + " not found!\n" + def);
                }
                break;
            }
        }
    }

    public static void displayItem()//For displaying items inside the inventory
    {
        if (inventory.isEmpty()) //Checks if the inventory is empty
        {
            System.out.println(blue + "🤔Looks like your inventory is empty \n😄I'll take you back to the menu" + def);
            start();
        }
        else
        {
            System.out.print("\nWould you like me to sort the items out? \n[Y] Yes [N] No \nChoice: ");

            String choice = sc.next();
            if (choice.equalsIgnoreCase("Y")) {
                Collections.sort(inventory);
                System.out.println(blue + "🛒Items Sorted: " + inventory + def + "\n");
            }
            else if (choice.equalsIgnoreCase("N")) {
                System.out.println(blue + "🛒Items Unsorted: " + inventory + def + "\n");
            }
            else
            {
                System.out.println("☹Invalid Key☹\n");
            }
        }
    }
}
