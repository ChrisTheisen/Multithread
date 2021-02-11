# Multithread

Allow access to controls in different threads via magic delegates and reflection.  For example, accessing a GUI on a background  thread.

Use: 

    ControlName: Object that might be on a different Thread.
    Value: Method or Property to access.
    OptionalProperty: Child-object of ControlName that has Method or Property Value.  Accepts Null.
    OptionalArg: Object array used in setting or executing Value.  Accepts Null.

    MultiThread.ControlAction(Control ControlName, string Value, object OptionalMember, object[] OptionalParameters)


Examples:

Set a property, Text (lblStatus) to "Done".
  
    MultiThread.SetProperty(lblStatus, "Text", "Done");

Update tool strip text.

    MultiThread.UpdateToolStripStatus( lblDuration, $@"Duration: {duration.TotalSeconds}s" );
  
Invode a method, appends text to RichTextBox (rtbLog).
  
    MultiThread.InvokeMethod(rtbLog, "AppendText", new object[] { message });
  
Set a child property, GridView.AutoSizeMode is set to DataGridViewAutoSizeColumnMode.AllCells.

    MultiThread.SetChildProperty(grdResults, col, "AutoSizeMode", DataGridViewAutoSizeColumnMode.AllCells);
    

