# PrintReceipt

Correct way to print multi pages receipt with cut-off 

# CSS 
````@media print 
{
    #print-area {
        width: 700px;
        margin-left: -150px;
    }
    div.page-break {
        display: block !important;
        page-break-before: always;
    }
}

@page {
    margin: 3mm 3mm 3mm 3mm;
}

@media all {
    .page-break {
        display: none;
    }
}````

# HTML

````<div id="print-area" style="display:none;">
   <!-- first page print content here -->
    <div class="page-break"></div>
   <!-- second page print content here -->
</div>````

# Settings 

Control Panel > Printers > Preferences > Document Settings tab > Page Source set to <Page[Feed , Cut]>
