# 📋 Assignment: PIN Block Application

## 🎯 Task Requirements

✅ Implement an Android application with the following functionality:

1. Allow the user to enter a **4–12 digit PIN** on screen.
    - Using the system IME and a text field is acceptable.
2. Once the PIN entry is complete, generate an [ISO-1 (Format 1) PIN Block](https://www.eftlab.com/knowledge-base/complete-list-of-pin-blocks).
3. Display the computed PIN Block on screen.
4. Ensure the application handles **configuration changes** (e.g., rotation) gracefully.
5. ⭐ **Bonus:**
    - Allow the user to enter a **PAN** (Primary Account Number) in a separate text field, in addition to the PIN.
    - Use the entered PAN to generate an [ISO-3 (Format 3) PIN Block](https://www.eftlab.com/knowledge-base/complete-list-of-pin-blocks) instead of ISO-1.

---

## How to submit

Please provide a link to the private git repository on GitHub and send an invitation to the GitHub user `xziska02` with an admin access.

## 🧰 Useful Code (for ISO-3 PIN Block)

```kotlin
private fun setHiNibbleValue(value: Byte): Byte =
    ((value.toInt() shl 4) and 0xF0).toByte()

private fun setLowNibbleValue(value: Byte): Byte =
    (value.toInt() and 0x0F).toByte()
