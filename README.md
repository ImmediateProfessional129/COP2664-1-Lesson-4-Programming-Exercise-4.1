# COP2664-1-Lesson-4-Programming-Exercise-4.1
This is a repository link of the COP2664-1 Lesson 4 Programming Exercise 4.1

// This program is designed to calculate the payments the user has to make in order to pay off their loan.

import Foundation // Imports the Foundation library.

print("Enter the loan amount: ", terminator: "") // Prints the prompt for the user to enter the loan amount.
let loanAmount = Float(readLine()!)! // Reads the user's input and converts it to a float.
print("Enter the payment amount: ", terminator: "" ) // Prints the prompt for the user to enter the payment amount.
let paymentAmount = Float(readLine()!)! // Reads the user's input and converts it to a float.
print("Enter the interest rate: ", terminator: "" ) // Prints the prompt for the user to enter the interest rate.
let interestRate = Float(readLine()!)! // Reads the user's input and converts it to a float.
var balance = loanAmount // Sets the balance to the loan amount.
var paymentCount = 0 // Sets the payment count to 0.
while balance > 0 { // Loops while the balance is greater than 0.
    balance += balance * (interestRate / 100) // Adds the interest to the balance.
    balance -= paymentAmount // Subtracts the payment amount from the balance.
    paymentCount += 1 // Increments the payment count.
}
print("Number of payments required: \(paymentCount)" ) // Prints the number of payments required.
