# December 6th, 2023 Labs
## Lab 1 
Implement the BankAccount class that is outlined below.

Implement each class method according to the method's given Javadoc comment.

You do not need to write any code that calls your methods. Your methods will be called and tested by the Tester.java program. The Tester.java program expects a single input integer between 1 and 2. The Tester.java program then runs one of its two built-in test cases.

```java
/**
   This class represents bank accounts that
   have an owner, a type, and a balance.
*/
class BankAccount
{
   private String owner;
   private int type;  // 0 for savings, 1 for checking, 2 for CD
   private double balance;

   /**
      Construct a BankAccount with the given owner's name,
      of type savings, and with a balance of zero.

      @param owner  the String name of the owner
   */
   public BankAccount(String owner)
   {
      this.owner = owner;
      this.type = 0;
      this.balance = 0.0;
   }
   
   /**
      Construct a BankAccount with the given owner's name,
      of the given type, and with a balance of zero.

      @param owner  the String name of the owner
      @param type   integer value that determines the account type
   */
   public BankAccount(String owner, int type)
   {
      this.owner = owner;
      this.type = type;
      this.balance = 0;
   }
   
   /**
      Construct a BankAccount with the given owner's name,
      of the given type, and with the given balance.

      @param owner    the String name of the owner
      @param type     integer value that determines the account type
      @param balance  the intial balance of this account
   */
   public BankAccount(String owner, int type, double balance)
   {
      this.owner = owner;
      this.type = type;
      this.balance = balance;
   }
   
   /**
      Deposit the given amount into this account.
     
      @param money  amount of money to add to this account's balance
   */
   public void deposit(double money)
   {
      this.balance += money;
   }

   /**
      Withdraw the given amount from this account. If there is not enough
      money in this account, then withdraw as much as possible, but do not
      let the balance become negative.
     
      @param money  amount of money to deduct from this account's balance
      @return the amount that was withdrawn (which may be less than the requested amount)
   */
   public double withdraw(double money)
   {
      double withdrawnMoney = 0;
      if (this.balance < money)
      {
         withdrawnMoney = this.balance;
         this.balance = 0;
      }
      else
      {
         withdrawnMoney = money;
         this.balance -= money;
      }
      return withdrawnMoney;
   }

   /**
      Transfer the given amount of money from the given BankAccount
      to this BankAccount.
     
      Note: The other account may not have enough money. In that case
      transfer as much as possible.

      @param other  the BankAccount to transfer money from
      @param money  amount of money to deduct from the other account and deposit in this account
      @return the amount transferred (which may be less than the requested amount)
   */
   public double transferFrom(BankAccount other, double money)
   {
      double transfer = other.withdraw(money);
      this.deposit(transer);
      return transfer;
   }

   /**
      Transfer the given amount of money from this BankAccount
      to the given BankAccount.

      Note: This account may not have enough money. In that case
      transfer as much as possible.

      @param other  the BankAccount to transfer money into
      @param money  amount of money to deduct from this account and deposit in the other account
      @return the amount transferred (which may be less than the requested amount)
   */
   public double transferTo(BankAccount other, double money)
   {
      double transfer = this.withdraw(money);
      other.deposit(transer);
      return transfer;
   }


   public String toString()
   {
      String typeName;
      if (this.type == 0)
         typeName = "Savings";
      else if (this.type == 1)
         typeName = "Checking";
      else
         typeName = "CD";

      String result =  "BankAccount of type: " + typeName + "\n";
      result += "Owned by: " + owner + "\n";
      result += "with balance: " + balance;

      return result;
   }
}
```