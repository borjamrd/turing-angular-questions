## Turing angular interview

> Important: here are some questions that I answer during my Turing interview for Angular. I passed it with 80% of correct answers but I couldn't note which were correct and which no. **Please, feel free to make any changes or pull request.**

1. Which form control class name is set to true when value is modified?

   `ng-dirty`

---

2. Given the following code
   ```
   @ViewChild('element', {static: false}) elementRef: ElementRef
   ```
   Which of the following is the correct location the viewchild elementRef available for usage in Angular?
   ==i didn't have time to write the possible answers==.

---

3. Consider the following code definition of the DemoModule
   ```
   @NgModule({
   imports: [CommonModule]
   })
   export class DemoModule {
       static forRoot(): ? {
           return {
               ngModule: DemoModule,
               providers: [DemoService]
           };
       }
   }
   ```

- [ ] LazyLoadedModule
- [x] ModuleForRoot
- [ ] ModuleWithProviders
- [ ] Observable<NgModule>
- [ ] None of the above

---

4. When you chain multiple pipes together, what order will they be executed?

- [ ] LIFO ORDER
- [ ] In parallel
- [x] In the order that you specify them
- [ ] None of the above

---

5. You are using Angular to develop a Web application, you need to send data of an Observer to its subscribers. Which method can you use?

- [ ] emit()
- [x] next()
- [ ] send()
- [ ] publish()

---

1. Which of the following wild cards can you use to define a “page not found” route?

- [ ] -
- [x] \*\*
- [ ] 404
- [ ] ^

---

7. You are using Angular to develop a Web application. You want to extract route parameters inside a component. Which service can support you to do it?

- [ ] Router
- [ ] RouterLink
- [ ] RouterLinkActive
- [x] ActivatedRoute

---

8. What is correct answer about Subject and Behaviour Subject in RxJS?

- [ ] Once you unsubscribe, BehaviourSubject can be reused and Subject can not
- [ ] If you unsubscribe to a Subject or Behaviour Subject, you will be able to get the current value or initial value
- [ ] You have to define a default value whenever you declare Behaviour Subject based upon the data type.
- [x] In Subject, each next subscriber receives only the upcoming values. In Behaviour Subject, each next subscriber receives one previos value and upcoming values.

---

9. Which of the following is TRUE about the kinds of directives in Angular?

- [x] Structural and Attribute directives
- [ ] Component, Structural and Attribute directives
- [ ] Component, Template, Structural and Attribute directives
- [ ] Only one directive

---

10. What is the expected behaviour of the following code?

    ```
        import {Component} from "@angular/core"
    import {of} from "rxjs";

    @Component({
            selector: "app-root",
            template: "<h1>Count:{{name$ | async }}</h1>"
    })

    export class AppComponent {
        count$ = of(NaN);
    }
    ```

- [ ] Change detection is triggered and this error occurs: Expression has changed after it was checked.

- [x] The app displays Count: NaN.
- [ ] A compile error is thrown: type number is not assignable to type string.
- [ ] A compie error is thrown: Can't create Observable out of NaN.

---

11. What happens when injecting a service to the constructor without access modifier (private, public or protected) or readonly?

- [x] Program compile succesfully and work normally //probada
- [ ] Compilation error
- [ ] Compilation success but the page is blank

---

12. Which of the following is TRUE about ngOnInit? (select all that apply)

- [x] ngOnInit is a life cycle hook that is called by Angular
- [ ] The ngOnInit is called after the constructor is executed
- [ ] The ngOnInit can be call many time in Angular life cycle

  ***

13. You are using Angular to develop the web application. You want to use HttpClient service in the project. How can you do?

- [ ] HttpModule
- [ ] Http
- [x] HttpClientModule // creo
- [ ] None of the avove

14. Following the source code:

    ```
    @component({
        selector: 'my-svg',
        ,
        styleUrls: [`.svg/.component.css`]
    })
    ```

    how can you use this SVG template?

- [ ] templateUrl: './svg.component.svg'
- [ ] template: './svg.component.svg',
- [x] template: `<svg *svgTemplate><path [d]="validPath"/></svg>`,
- [ ] vgTemplate: `<svg><path [d]="validPath"/></svg>`

---

15. Which of the following is incorrect statement about Pipe in Angular?

- [x] Pipes are impure by default
- [ ] There are 2 types of pipes: pure and impure
- [ ] Angular executes a pure pipe only when it detects a pure change to the input value
- [ ] None of the above

---

16. Which of the following is TRUE about the Subjects are multicast?

- [ ] They can be defined with multiple data types.
- [x] They broadcast notifications to one or more subscribers.
- [ ] They can support Web sockets for communication with the server.
- [ ] They support bi-directional communication

---

17. Which of the following helps style child component from parent component’s style file?

- [ ] ::ng-deep
- [ ] /deep/
- [ ] Encapsulation mode
- [x] All of the above

18. What is the expected behavior of the following code?

    ```
    import {Component} from '..core'
    import {of} ....

    @Component({
        selector: 'app-root',
        template: '<h1>Count: {{count$ | async}}</h1>'
    })
    export class AppComponent {
        count$ = of(NaN)
    }
    ```

- [x] The app displays Count: NaN.

---

19. You are developing a Web application. You need to get data from parent component to child component. How can you do it?

- [x] Using @Input
- [ ] using @Viewchild
- [ ] Using service
- [ ] All of above
- [ ] None of the above

---

20. In Angular lifecycle, which method is called the first when an Angular class component is created?

- [x] constructor()
- [ ] ngOnInit()
- [ ] ngOnChanges()
- [ ] ngAfterViewInit()

---

21. Which directive can you use if you want to display views for a given router?

- [x] RouterOutlet
- [ ] RouterLink
- [ ] RouterLinkActive
- [ ] RouterState

---

22. How can you use ngFor and ngIf in the same div or tag in Angular?

- [x] No way, angular just support use ngFor or ngIf in one dive or tag
- [ ] By default, angular supponer both in the same div or tag
- [ ] By using ng-container or ng-template
- [ ] None of the above

---

23. What is correct answer about ReplaySubject and BehaviourSubject in RxJS?

- [ ] both will return the initial value or the current value on Subscription
- [ ] ReplaySubject will not take any initial value
- [ ] When initializig, BehaviourSubject is not required initial value.
- [x] None of the above.

---

24. Which of the following is the correct statement about Promise and Observable in Angular?

- [ ] Promise and Observable work with multiple values over time
- [ ] Promise use Reactive Extensions
- [ ] Promise cancellable
- [x] Observable is array whose items arrive asynchronously over time.

---

25. When using Reactive forms which is/are the recommended form(s) of binding data to a controller?

- [ ] [(ngModel)]
- [x] [formControl]="nameOfControl"
- [ ] reactiveControlName="nameOfControl"
- [ ] All of the above.

---

26. You are using Angular to develop a Web application. In the case the data model is updated outside the Zone, you need to update the view. How can you do it?

- [ ] Using the ApplicationRef.prototype.forceUpdate
- [ ] Using NgZone.prototype.update
- [ ] Using the ChangeDetectorRef.prototype.detectChanges
- [x] None of the above.

---

27. Wich of the following Angular synstaxes are used for grouping elements when using structural directive (*ngFor, *ngIf)?

- [ ] ng-group
- [x] ng-container
- [ ] ng-template
- [ ] ng-item

---

28. Which of the following is the correct statement about the Hook called to indicate that completed creating the component?

- [ ] ngAfterViewInit
- [ ] ngAfterContentInit
- [ ] ngAfterViewChecked //creo
- [ ] ngOnInit

---

29. Which of the following are ways to build forms in Angular?

- [ ] model-drive and interface-drive
- [ ] interface-driven and template-drive
- [ ] modular-driven and template-driven
- [x] template-driven and model-driven
      ==he I'm not plenty sure if the possible answers provided are correct==.

---

30. Which following is the most efficient to compile in Angular?

- [x] Ahead-of-Time (AOT) //Creo
- [ ] Just-in-Time (JIT)
- [ ] None of the above

---

31. Given the following code:

    ```
    @Directive({selector: '[...]'})
    export class HighlightDirective {
        constructor(el: ElementRef){
            //code here
        }
    }
    ```

    how do you make the background color of an element to be red?

- [x] el.nativeElement.style.backgroundColor = "red"
- [ ] el.nodeMode.style.backgroundColor = "red"
- [ ] el.withCSS({style: {backgroundCOlor: 'red'}})
- [ ] el.domNode.style.backgroundColor = "red"

---

32. What is the correct answer about the function executes a query inner animation element within an animation sequence?

- [x] animateChild
- [ ] childAnimate
- [ ] animateInner
- [ ] none of the above

---

33. Which of the following is the correct statement about the service allows to load new components at the runtime?

- [ ] ComponentFactory
- [ ] DynamicComponentFactory
- [x] DynamicFactoryLoader
- [ ] ComponentFactoryResolver

---

34. You are using Angular to develop a Web application. You are using RxJS to retrieve data via HTTP. Which of the following is TRUE about the time the request submitted to the server?

- [ ] When the code calls the makeRequest method of the observable.
- [ ] When the object containing the Observable is created.
- [x] When the Observable is subscribed to.
- [ ] When the obserable is created.

---

35. Given the following code. Where is the viewchild elementRef available for usage (not undefined)? `@viewChild(’element’,{static: false}) elementRef: ElementRef`

- [x] In ngAfterViewInit
- [ ] In ngAfterContentInit
- [ ] In ngOnInit
- [ ] All of the above

---

36. Point out the incorrect statement about BOM in Angular

- [ ] BOM has W3C Recommended standard specifications
- [x] BOM can access and manipulate the browser windorw
- [ ] BOM works a level above web page and includes browser attributes
- [ ] None of the above

---

37. You are a developer at Turing. You are using Angular to develop the Web Applicatiion. When using FormArray, which of the following is correct syntax that replaces the following syntax?

    `while(formArray.length) formArray.removeAt(0);`

- [x] formArray.clear() //creo
- [ ] formArray.invalidate()
- [ ] formArray.removeAll()
- [ ] formArray.invalid()

---

38. Which of the following is correct statement about the parent class of all Change Detectors?

- [x] ChangeDetector
- [ ] OnChange
- [ ] AbstractChangeDetector
- [ ] All of the above.
