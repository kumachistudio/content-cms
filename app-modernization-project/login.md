---
layout: default
---

# login
 The login component architecture involved:
 1. creating a reusable login form component that takes in data from the datalist service. The component is made use of in the login-page component which calls the said service.
 2. In the login-page component, the functionality of the login form is only triggered if there's actual data in the dataList brought in by the datalist service. But to me this is wrong architecture:- Because it provides bad user experience. No one would like to look at a blank screen when trying to access their app. Alternatively the login state should be improved by letting the login form appear but if there is no data from datalist service/ database, a nice error message can be shown  telling the user to connect the database.
 This line of code comes from the login-page.component.html
 <app-sd-login-form [dataList]="dataList" *ngIf="dataList.length !== 0"> </app-sd-login-form>
 3. On the topic of Template driven vs Reactive Forms. In simple scenarios like this one, the template driven approach served the purpose. Although template driven forms require minimal code and they're asynchronous in nature, I wouldn't advise members to go for it because Reactive forms give more advantages as the forms get complicated. Such as:- handling a event based on a debounce time, handling events when the components are distinct until changed or even adding elements dynamically
 