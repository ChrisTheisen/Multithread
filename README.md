# Multithread

Allow access to controls in different threads via magic delegates and reflection.  For example, accessing a GUI on a background  thread.

Use: 

    ControlName: Object that might be on a different Thread.
    Value: Method or Property to access.
    OptionalProperty: Child-object of ControlName that has Method or Property Value.  Accepts Null.
    OptionalArg: Object array used in setting or executing Value.  Accepts Null.

    MultiThread.ControlAction(Control ControlName, string Value, object OptionalMember, object[] OptionalParameters)


Examples:

Sets a Label Text (lblStatus) to "Done".
  
    MultiThread.ControlAction(lblStatus, "Text=Done", null, null);
  
Sets the background color of a button(btnStop) to Red.
  
    MultiThread.MultiThread.ControlAction(btnStop, "BackColor=", null, new object[] { Color.Red });
  
Adds a filename to a ListBox items.
  
    MultiThread.ControlAction(lstResults, "Add()", lstResults.Items, new object[] { File + "\t\t" + MatchLine.Trim() });
