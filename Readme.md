<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128639435/13.1.8%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E5076)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [NavigationTypeProvider.cs](./CS/App1/Common/NavigationTypeProvider.cs)
* [StandardStyles.xaml](./CS/App1/Common/StandardStyles.xaml) (VB: [StandardStyles.xaml](./VB/App1/Common/StandardStyles.xaml))
* [MainPage.xaml](./CS/App1/MainPage.xaml) (VB: [MainPage.xaml](./VB/App1/MainPage.xaml))
* [MainPage.xaml.cs](./CS/App1/MainPage.xaml.cs) (VB: [MainPage.xaml.vb](./VB/App1/MainPage.xaml.vb))
* [Reference.cs](./CS/App1/Service References/ServiceReference1/Reference.cs) (VB: [Reference.vb](./VB/App1/Service References/ServiceReference1/Reference.vb))
* [IService1.cs](./CS/WebApplication1/IService1.cs) (VB: [IService1.vb](./VB/WebApplication1/IService1.vb))
* [Service1.svc.cs](./CS/WebApplication1/Service1.svc.cs) (VB: [Service1.svc.vb](./VB/WebApplication1/Service1.svc.vb))
<!-- default file list end -->
# How to: Load data dynamically using AsyncCollection


<p>This example demonstrates how to use <strong>GridControl</strong> with our <strong>AsyncCollection</strong>. This collection allows loading data on-demand, so it may be very useful if you obtain data from a web service and don't want to wait until all data is loaded. Its constructor receives two parameters:</p><p>1. A callback that returns the total number of items</p><p>2. A callback that returns items from required positions.</p><p>For example:<br />


```cs
var Items = new AsyncCollection<Item>(
   async () => { return 1000; },
   async (int skipCount, int takeCount) => {
       return await Service1.GetDataAsync(skipCount, takeCount);
   });
```

 </p>

<br/>


<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=how-to-load-data-dynamically-using-asynccollection-e5076&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=how-to-load-data-dynamically-using-asynccollection-e5076&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
