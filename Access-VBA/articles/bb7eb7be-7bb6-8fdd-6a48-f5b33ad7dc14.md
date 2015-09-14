
# Form.OnCurrent Property (Access)

 **Last modified:** July 28, 2015

Sets or returns the value of the  **On Current** box in the **Properties** window of a form. Read/write **String**.

## Syntax

 _expression_. **OnCurrent**

 _expression_A variable that represents a  **Form** object.


## Remarks

This property is helpful for programmatically changing the action Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered. 

The  **Current** event occurs when the focus moves to a record, making it the current record, or when the form is refreshed or requeried.

The  **OnCurrent** value will be one of the following, depending on the selection chosen in the **Choose Builder** window (accessed by clicking the **Build** button next to the **On Apply Filter** box in the form's **Properties** window):


- If Expression Builder is chosen, the value will be "= _expression_", where  _expression_ is the expression from the Expression Builder window.
    
- If Macro Builder is chosen, the value is the name of the macro. 
    
- If Code Builder is chosen, the value will be "[Event Procedure]". 
    
If the  **On Current** box is blank, the property value is an empty string.


## Example

The following example associates the  **Current** event with the macro "Current_Macro" for the "Order Entry" form.


```
Forms("Order Entry").OnDeactivate = "Current_Macro" 

```


## See also


#### Concepts


 [Form Object](72ef9219-142b-b690-b696-3eba9a5d4522.md)
#### Other resources


 [Form Object Members](e1976b58-28ca-8f76-cdf3-6732cb06ce6c.md)