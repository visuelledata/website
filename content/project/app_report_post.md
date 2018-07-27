Automated App Reports
---------------------

### Summary:

This project is to generate automated self-written reports for my phone
usage. You can see the R code [on my GitHub
page](https://github.com/visuelledata/AppReports).

### How it works:

1.  **Data collection:**  
    All of the data is collected on my phone using a script created on
    [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en).
    This script logs the time I spend on any app, then uploads it to
    Google Sheets.

2.  **The report:**  
    The report is designed and generated in R as an HTML file. It pulls
    the data from Google Sheets, cleans the data, and then generates a
    report using it.

3.  **Sending:**  
    Every month Tasker runs a script from my phone to turn on my PC,
    then sends a message to the EventGhost (Windows automation program).
    EventGhost then runs a shell command to run the
    [create\_report.R](https://github.com/visuelledata/AppReports/blob/master/create_report.R)
    script. The report is then generated and emailed using R.

### Example report:

### Monthly app report

#### July 27, 2018

<img src="D:/rproj/AppReports/plot1.jpeg" alt="Total app usage" height="220" width="600">

Top 10 apps have changed see: Hyperion, Keep

<img src="D:/rproj/AppReports/plot2.jpeg" alt="Group of plots" height="600" width="600">

**Note:** Some of the lines don't represent apps. Many of them are names
of books, which I intentionally included.
