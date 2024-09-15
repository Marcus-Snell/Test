```mermaid
classDiagram
direction LR
BankMember
BankMember : MemberId int
BankMember : MemberName string
BankMember : MemberAddress string
BankMember : MemberPhone string
BankMember : CreateNewAcct()
BankMember: CloseAcct()
BankMember : ViewAcct()

Employee --|> BankMember : is a
Employee o-- Customer : has a
Employee : EmpId int
Employee : getCustomer()

Customer --|> BankMember : is a
Customer --o Account : has a
Customer : CustId int

Account --o Product : has a
Account : AcctId int
Account : Type char
Account : CustId int
Account : getProducts()
Account : addProduct()
Account : DeleteProduct()

Product : ProductId int
Product : ProductType char
Product : APR int
Product : Balance int
Product : getBalance()
Product : makeWithdrawal()
Product : makeDeposit()

```
