```mermaid
classDiagram
direction LR
BankMember
BankMember : MemberId int
BankMember : MemberName string
BankMember : MemberAddress string
BankMember : MemberPhone string


Employee --|> BankMember : is a
Employee o-- Customer : has a
Employee : EmpId int
Employee : getCustomers()

Customer --|> BankMember : is a
Customer --o Account : has a
Customer : CustId int
Customer : getAccount()

Account --o Product : has a
Account : AcctId int
Account : Type char
Account : CustId int
Account : getProducts()
Account : addProduct()
Account : delProduct()




Product : ProductId int
Product : ProductType char
Product : APR int
Product : Balance int
Product : getBalance()
Product : makeWithdrawal()
Product : makeDeposit()

```
