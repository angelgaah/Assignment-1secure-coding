#Assignment-1secure-coding

// Create a class Bank with fields accountType and accountBalance
class Bank {
    String accountType;
    double accountBalance;

// Create a method deposit that adds to the accountBalance and return the value
    double deposit(double amount) {
        accountBalance += amount;
        return accountBalance;
    }
// Create a method withdrawal that subtracts from the accountBalance and return the value
    double withdrawal(double amount) {
        accountBalance -= amount;
        return accountBalance;
    }

    // Create a parameterized constructor that sets the accountType and accountBalance
    Bank(String accountType, double accountBalance) {
        this.accountType = accountType;
        this.accountBalance = accountBalance;
    }

    // Create a method display to print "The account type is (accountType) and balance is (accountBalance)
    void display() {
        System.out.println("The account type is " + accountType + " and balance is " + accountBalance);
    }
}

// Create a class Insurance that inherits from the Bank class
class Insurance extends Bank {
    //Create a method cover that prints "You are covered"
    void cover() {
        System.out.println("You are covered");
    }

    // Constructor calling parent class constructor
    Insurance(String accountType, double accountBalance) {
        super(accountType, accountBalance);
    }
}

public class Main {
    public static void main(String[] args) {
        // In the main method create an instance of the Bank class
        Bank bank = new Bank("Gabriel Samunda", 230770);

        // Invoke display method
        bank.display();

        // Create an instance of the Insurance class
        Insurance insurance = new Insurance("Gabriel Samunda", 230770);
        insurance.display();
        insurance.cover();
    }
}
