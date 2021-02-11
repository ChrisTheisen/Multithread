# Multithread

Allow access to controls in different threads via magic delegates and reflection.  For example, accessing a GUI on a background  thread.

Examples:

Set a property, Text (lblStatus) to "Done".
  
    MultiThread.SetProperty(lblStatus, "Text", "Done");

Update tool strip text.

    MultiThread.UpdateToolStripStatus( lblDuration, $@"Duration: {duration.TotalSeconds}s" );
  
Invode a method, appends text to RichTextBox (rtbLog).
  
    MultiThread.InvokeMethod(rtbLog, "AppendText", new object[] { message });
  
Set a child property, GridView.AutoSizeMode is set to DataGridViewAutoSizeColumnMode.AllCells.

    MultiThread.SetChildProperty(grdResults, col, "AutoSizeMode", DataGridViewAutoSizeColumnMode.AllCells);
    

