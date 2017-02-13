# Exercise 6: Visualizing in Power BI Desktop

Duration: 20 mins

Synopsis: In this exercise, attendees will construct a report in Power BI Desktop Client that uses the map visualization to illustrate the predicted delays, using the data originally scored using Machine Learning, but summarized in a table using Spark on HDInsight.

This exercise has 4 tasks:

* [Task 1: Connect to the Lab VM](#task-1-connect-to-the-lab-vm)
* [Task 2: Connect to the HDInsight Spark Using Power BI Desktop](#task-2-connect-to-the-hdinsight-spark-using-power-bi-desktop)
* [Task 3: Create Power BI Report](#task-3-create-power-bi-report)

## Task 1: Connect to the Lab VM

1. **NOTE:** If you are already connected to your Lab VM, skip to [Task 2](#task-2-connect-to-the-hdinsight-spark-using-power-bi-desktop).
1. From the left side of the Azure portal, click on **All resources**.
2. In the **Filter items...** box, type in **lab**.
3. Select your lab VM. Keep in mind the name of the virtual machine will begin with the "app name" you provided when setting up this workshop environment (in the prerequisite deployment).
2. At the top of the blade for your VM, click on **Connect**.

    ![Screenshot](images/connect_to_the_lab_vm_1.png)

3. Download and open the RDP file.
1. When the **Remote Desktop Connection** screen appears, check the **Don't ask me again...** box and click on **Connect** button.

    ![Screenshot](images/ex02_connect_to_the_lab_vm_2.png)

1. Log in with the following credentials:
   - User name: **cortana**
   - Password: **Password.1!!**

## Task 2: Connect to the HDInsight Spark Using Power BI Desktop

1. Launch Power BI Desktop using the shortcut on the Desktop of the Lab VM.
2. Click on **Get Data** from the left side of the welcome window.

    ![Screenshot](images/connect_to_the_hdinsight_spark_using_power_bi_desktop_0.png)

1. Click on the **Azure** from the left and select **Azure HDInsight Spark (Beta)** from the new **Get Data** window. Click on the **Connect** button on the bottom right corner.

    ![Screenshot](images/connect_to_the_hdinsight_spark_using_power_bi_desktop_1.png)

1. Click **Continue** on the bottom right corner of the new window.
2. Type or copy/paste the **URL** of your Azure HDInsight Spark cluster, which can be found from the address bar when connected to the Azure HDInsight Spark cluster in previous Exercise 5. It should look something like this example: [**https://jcholab199spark.azurehdinsight.net**](https://jcholab199spark.azurehdinsight.net).
3. Click the **OK** button.
4. When prompted, enter the cluster user name and password and then click **Connect**.
   - User name: **cortana**
   - Password: **Password.1!!**

2. When the dialog box disappears, look for the **flightdelaysummary** in the list and check the box next to it.

    ![Screenshot](images/connect_to_the_hdinsight_spark_using_power_bi_desktop_3.png)

2. Click on the **Load** button from the bottom right corner of the window. It will take couple of minutes to load the data into the Power BI Desktop client.

## Task 3: Create Power BI Report

1. Once the data load is completed, you will find the **flightdelaysummary** to the right side of the screen under the **Fields** area.

    ![Screenshot](images/create_power_bi_report_0.png)

1. From the **Visualizations** area, which is left to the **Fields** area, click the **Globe** icon to add a Map visualization to the report design surface.

    ![Screenshot](images/create_power_bi_report_1.png)

1. With the Map visualization still selected, in the **Fields** area at right, expand the tabled called **flightdelayssummary**.

    ![Screenshot](images/create_power_bi_report_2.png)

1. Click and drag the field labeled **OriginLatLong** and drop it into the **Location** field located just below visualizations.

    ![Screenshot](images/create_power_bi_report_3.png)

1. Next, drag the field labeled **NumDelays** and drop it into the **Size** field.

    ![Screenshot](images/create_power_bi_report_4.png)

1. Your map should look something like the following:

    ![Screenshot](images/create_power_bi_report_5.png)

1. Unselect the Map visual by clicking on the white space on the report page.
2. From the **Visualizations** area, which is left to the **Fields** area, click the **Stacked Column Chart** icon to add a bar chart visualization to the report design surface.

    ![Screenshot](images/create_power_bi_report_6.png)

1. With the **Stacked Column Chart** visualization still selected, in the Fields area at right, expand the tabled called **flightdelayssummary**.

    ![Screenshot](images/create_power_bi_report_7.png)

1. Click and drag the field labeled **Day** and drop it into the **Axis** field located just below visualizations.

    ![Screenshot](images/create_power_bi_report_8.png)

1. Next, drag the field labeled **AvgDelayProbability** and drop it into the **Value** field.

    ![Screenshot](images/create_power_bi_report_9.png)

1. Grab the corner of the new **Stacked Column Chart** Visual and drag it out by making wide as the bottom of your report design surface.
2. Your report should look something like the following:

    ![Screenshot](images/create_power_bi_report_10.png)

1. Unselect the Stacked Column Chart visual by clicking on the white space on the report page.
2. From the **Visualizations** area, which is left to the **Fields** area, click the **Treemap** icon to add this visualization to the report design surface.

    ![Screenshot](images/create_power_bi_report_11.png)

1. With the **Treemap** visualization still selected, in the Fields area at right, expand the tabled called **flightdelayssummary**.

    ![Screenshot](images/create_power_bi_report_12.png)

1. Click and drag the field labeled **OriginAirportCode** and drop it into the **Group** field located just below visualizations.

    ![Screenshot](images/create_power_bi_report_13.png)

1. Next, drag the field labeled **NumDelays** and drop it into the **Value** field.

    ![Screenshot](images/create_power_bi_report_14.png)

1. Grab the corner of the new **Treemap** Visual and drag it out by making wide as the top of your report design surface. Your report should look similar to the following:

    ![Screenshot](images/create_power_bi_report_15.png)

1. You can cross filter the visualizations on the report by click on the one of the other visuals within the report as shown below.

    ![Screenshot](images/create_power_bi_report_16.png)

1. You can save this Power BI report by click on Save icon from the top left corner of the screen.

Next Exercise: [Exercise 7 - Deploy Intelligent Web App](07 Exercise 7 - Deploy Intelligent Web App.md)