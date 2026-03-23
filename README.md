# CS501midterm_Q2
# Question 2: ViewModel + Unidirectional Data Flow

## Description

This task refactors a simple counter application to follow proper Android architecture using a ViewModel and unidirectional data flow. Instead of managing state inside the composable, the state is moved to a ViewModel to improve separation of concerns and lifecycle handling.

---

## Screenshot

(SS2/2nd_mid.png)


---

## Implementation Details

### ViewModel

* A `CounterViewModel` is created to manage the counter state
* The counter value is stored inside the ViewModel
* A function `increment()` is defined to update the state

### Composable (`CounterScreen`)

* The composable reads state directly from the ViewModel:

  ```kotlin
  val count by viewModel.count
  ```
* The UI displays the current count value
* Button clicks call the ViewModel function:

  ```kotlin
  viewModel.increment()
  ```

---

## Unidirectional Data Flow

1. State is stored in the ViewModel
2. UI reads the state
3. User actions trigger ViewModel functions
4. State updates trigger recomposition

---

## Key Features

* ViewModel-based state management
* Unidirectional data flow
* Automatic recomposition
* State survives screen rotation

---

## AI Usage Disclosure

* **Tool Used:** ChatGPT
* **How it was used:** Assisted in writing the README and fixing small bugs/issues
* **Extent of Use:** Used only for support; all implementation was done independently

---
