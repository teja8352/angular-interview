##**JavaScript coding questions**,

### 1. **Reverse a String**:

**JavaScript**
   ```js
   function reverseString(str) {
     return str.split('').reverse().join('');
   }
   ```

**TypeScript**
   ```ts
   function reverseString(str: string): string {
     return str.split('').reverse().join('');
   }
   ```
   **Explanation**: This method converts the string into an array using `split('')`, reverses the array using `reverse()`, and finally joins it back into a string using `join('')`.

---

### 2. **Check for Palindrome**:

**JavaScript**
   ```js
   function isPalindrome(str) {
     return str === str.split('').reverse().join('');
   }
   ```

**TypeScript**
   ```ts
   function isPalindrome(str: string): boolean {
     return str === str.split('').reverse().join('');
   }
   ```
   **Explanation**: A palindrome reads the same forward and backward. This function compares the string with its reversed version.

---

### 3. **Remove Duplicates from an Array**:

**JavaScript**
   ```js
   function removeDuplicates(arr) {
     return [...new Set(arr)];
   }
   ```

**TypeScript**
   ```ts
   function removeDuplicates<T>(arr: T[]): T[] {
     return [...new Set(arr)];
   }
   ```
   **Explanation**: This approach uses the `Set` object to remove duplicates and the spread operator to return the unique values as an array.

---

### 4. **Check if Two Strings Are Anagrams**:

**JavaScript**
   ```js
   function areAnagrams(str1, str2) {
     return str1.split('').sort().join('') === str2.split('').sort().join('');
   }
   ```

**TypeScript**
   ```ts
   function areAnagrams(str1: string, str2: string): boolean {
     return str1.split('').sort().join('') === str2.split('').sort().join('');
   }
   ```
   **Explanation**: Two strings are anagrams if their sorted characters are the same. This function splits both strings, sorts them, and compares the results.

---

### 5. **Find the Largest Number in an Array**:

**JavaScript**
   ```js
   function findLargest(arr) {
     return Math.max(...arr);
   }
   ```

**TypeScript**
   ```ts
   function findLargest(arr: number[]): number {
     return Math.max(...arr);
   }
   ```
   **Explanation**: The spread operator passes array elements as arguments to `Math.max()`, which returns the largest number.

---

### 6. **FizzBuzz**:

**JavaScript**
   ```js
   for (let i = 1; i <= 100; i++) {
     if (i % 3 === 0 && i % 5 === 0) console.log('FizzBuzz');
     else if (i % 3 === 0) console.log('Fizz');
     else if (i % 5 === 0) console.log('Buzz');
     else console.log(i);
   }
   ```

**TypeScript**
   ```ts
   function fizzBuzz(): void {
     for (let i = 1; i <= 100; i++) {
       if (i % 3 === 0 && i % 5 === 0) console.log('FizzBuzz');
       else if (i % 3 === 0) console.log('Fizz');
       else if (i % 5 === 0) console.log('Buzz');
       else console.log(i);
     }
   }
   ```
   **Explanation**: Prints "Fizz" for multiples of 3, "Buzz" for multiples of 5, and "FizzBuzz" for multiples of both 3 and 5.

---

### 7. **Flatten a Nested Array**:

**JavaScript**
   ```js
   function flatten(arr) {
     return arr.flat(Infinity);
   }
   ```

**TypeScript**
   ```ts
   function flatten(arr: any[]): any[] {
     return arr.flat(Infinity);
   }
   ```
   **Explanation**: The `flat()` method flattens arrays recursively when used with the `Infinity` argument.

---

### 8. **Find the First Non-Repeated Character**:

**JavaScript**
   ```js
   function firstNonRepeatedChar(str) {
     for (let char of str) {
       if (str.indexOf(char) === str.lastIndexOf(char)) return char;
     }
     return null;
   }
   ```

**TypeScript**
   ```ts
   function firstNonRepeatedChar(str: string): string | null {
     for (let char of str) {
       if (str.indexOf(char) === str.lastIndexOf(char)) return char;
     }
     return null;
   }
   ```
   **Explanation**: The function finds the first character whose first and last occurrence indices are the same.

---

### 9. **Sum of All Numbers in an Array**:

**JavaScript**
   ```js
   function sumArray(arr) {
     return arr.reduce((sum, num) => sum + num, 0);
   }
   ```

**TypeScript**
   ```ts
   function sumArray(arr: number[]): number {
     return arr.reduce((sum, num) => sum + num, 0);
   }
   ```
   **Explanation**: The `reduce()` method adds up all numbers in the array, starting from 0.

---

### 10. **Find the Fibonacci Sequence**:

**JavaScript**
   ```js
   function fibonacci(n) {
     const seq = [0, 1];
     for (let i = 2; i <= n; i++) {
       seq.push(seq[i - 1] + seq[i - 2]);
     }
     return seq;
   }
   ```

**TypeScript**
   ```ts
   function fibonacci(n: number): number[] {
     const seq = [0, 1];
     for (let i = 2; i <= n; i++) {
       seq.push(seq[i - 1] + seq[i - 2]);
     }
     return seq;
   }
   ```
   **Explanation**: Generates a Fibonacci sequence by adding the last two numbers of the series in a loop.

---

### 11. **Find the Factorial of a Number**:

**JavaScript**
   ```js
   function factorial(n) {
     if (n === 0) return 1;
     return n * factorial(n - 1);
   }
   ```

**TypeScript**
   ```ts
   function factorial(n: number): number {
     if (n === 0) return 1;
     return n * factorial(n - 1);
   }
   ```
   **Explanation**: This function uses recursion to calculate the factorial of `n`. The base case is when `n` equals 0.

---

### 12. **Find the Longest Word in a String**:

**JavaScript**
   ```js
   function findLongestWord(str) {
     return str.split(' ').reduce((longest, word) => word.length > longest.length ? word : longest, '');
   }
   ```

**TypeScript**
   ```ts
   function findLongestWord(str: string): string {
     return str.split(' ').reduce((longest, word) => word.length > longest.length ? word : longest, '');
   }
   ```
   **Explanation**: The function splits the string into words and uses `reduce()` to find the longest word.

---

### 13. **Count the Occurrence of Each Character in a String**:

**JavaScript**
   ```js
   function countChars(str) {
     const count = {};
     for (let char of str) {
       count[char] = count[char] ? count[char] + 1 : 1;
     }
     return count;
   }
   ```

**TypeScript**
   ```ts
   function countChars(str: string): Record<string, number> {
     const count: Record<string, number> = {};
     for (let char of str) {
       count[char] = count[char] ? count[char] + 1 : 1;
     }
     return count;
   }
   ```
   **Explanation**: Iterates over each character, counting occurrences in an object.

---

### 14. **Find the Missing Number in an Array**:

**JavaScript**
   ```js
   function findMissing(arr) {
     const n = arr.length + 1;
     const total = (n * (n + 1)) / 2;
     const sum = arr.reduce((a, b) => a + b, 0);
     return total - sum;
   }
   ```

**TypeScript**
   ```ts
   function findMissing(arr: number[]): number {
     const n = arr.length + 1;
     const total = (n * (n + 1)) / 2;
     const sum = arr.reduce((a, b) => a + b, 0);
     return total - sum;
   }
   ```
   **Explanation**: Calculates the total sum of a complete sequence and subtracts the actual array sum to find the missing number.

---

### 15. **Check if a String Contains Only Unique Characters**:

**JavaScript**
   ```js
   function hasUniqueChars(str) {
     return new Set(str).size === str.length;
   }
   ```

**TypeScript**
   ```ts
   function hasUniqueChars(str: string): boolean {
     return new Set(str).size === str.length;
   }
   ```
   **Explanation**: The `Set` object

Continuing from where we left off:

---

### 15. **Check if a String Contains Only Unique Characters**:

**JavaScript**
   ```js
   function hasUniqueChars(str) {
     return new Set(str).size === str.length;
   }
   ```

**TypeScript**
   ```ts
   function hasUniqueChars(str: string): boolean {
     return new Set(str).size === str.length;
   }
   ```
   **Explanation**: The `Set` object stores only unique values. If the size of the set equals the length of the string, then all characters are unique.

---

### 16. **Merge Two Sorted Arrays**:

**JavaScript**
   ```js
   function mergeArrays(arr1, arr2) {
     return [...arr1, ...arr2].sort((a, b) => a - b);
   }
   ```

**TypeScript**
   ```ts
   function mergeArrays(arr1: number[], arr2: number[]): number[] {
     return [...arr1, ...arr2].sort((a, b) => a - b);
   }
   ```
   **Explanation**: The function merges two arrays using the spread operator and then sorts the result in ascending order using `sort()`.

---

### 17. **Generate a Random String**:

**JavaScript**
   ```js
   function randomString(length) {
     return Math.random().toString(36).substring(2, 2 + length);
   }
   ```

**TypeScript**
   ```ts
   function randomString(length: number): string {
     return Math.random().toString(36).substring(2, 2 + length);
   }
   ```
   **Explanation**: This code generates a random alphanumeric string by converting a random number to base-36, which contains letters and numbers, and slicing it to the desired length.

---

### 18. **Check for Balanced Parentheses**:

**JavaScript**
   ```js
   function isBalanced(str) {
     const stack = [];
     for (let char of str) {
       if (char === '(') stack.push(char);
       else if (char === ')' && stack.pop() !== '(') return false;
     }
     return stack.length === 0;
   }
   ```

**TypeScript**
   ```ts
   function isBalanced(str: string): boolean {
     const stack: string[] = [];
     for (let char of str) {
       if (char === '(') stack.push(char);
       else if (char === ')' && stack.pop() !== '(') return false;
     }
     return stack.length === 0;
   }
   ```
   **Explanation**: The stack is used to track open parentheses. For every closing parenthesis, it checks if there's a corresponding opening parenthesis in the stack.

---

### 19. **Find the Second Maximum Number in an Array**:

**JavaScript**
   ```js
   function secondMax(arr) {
     const uniqueArr = [...new Set(arr)];
     uniqueArr.sort((a, b) => b - a);
     return uniqueArr[1];
   }
   ```

**TypeScript**
   ```ts
   function secondMax(arr: number[]): number {
     const uniqueArr = [...new Set(arr)];
     uniqueArr.sort((a, b) => b - a);
     return uniqueArr[1];
   }
   ```
   **Explanation**: This function removes duplicates using `Set`, sorts the array in descending order, and returns the second element in the sorted array.

---


---

##**TypeScript Interview Questions**,

---

### 1. **Benefits of TypeScript over JavaScript**:
- **TypeScript** helps you catch errors while coding because it checks types.
- It’s like JavaScript, but with extra tools to make your code cleaner and safer.

### Example:
```ts
let name: string = 'Alice';  // Ensures 'name' is always a string
```

---

### 2. **Type Inference**:
- TypeScript is smart! It guesses the type of a variable when you assign a value, so you don’t always need to specify the type.

### Example:
```ts
let age = 30;  // TypeScript knows 'age' is a number
```

---

### 3. **Types in TypeScript**:
- Types in TypeScript define what kinds of values variables can hold. Examples: `string`, `number`, `boolean`, etc.
- **Union Type**: A variable can hold multiple types of values (e.g., string or number).
  
### Example:
```ts
let value: string | number;  // Can be either a string or a number
```

---

### 4. **Interfaces vs Types**:
- **Interfaces** define the structure of an object.
- **Types** can do the same but can also be used for more complex scenarios like unions.

### Example:
```ts
interface Person {
  name: string;
  age: number;
}

let user: Person = { name: "Alice", age: 25 };  // Must match the structure
```

---

### 5. **Generics**:
- Generics allow functions or classes to work with any data type while still ensuring type safety.

### Example:
```ts
function identity<T>(arg: T): T {
  return arg;
}

console.log(identity(5));  // Works with any type
```

---

### 6. **Decorators**:
- Decorators are functions that modify the behavior of a class or method. Commonly used in frameworks like Angular.

### Example:
```ts
function Log(target, key) {
  console.log(`${key} was called`);
}

class MyClass {
  @Log
  myMethod() {
    console.log('Method executed');
  }
}
```

---

### 7. **Null and Undefined**:
- **`null`**: A variable with no value.
- **`undefined`**: A variable that hasn’t been assigned a value yet.

### Example:
```ts
let myVar: string | null = null;  // Can be a string or null
```

---

### 8. **Difference Between `interface` and `type`**:
- **Interface**: Describes the shape of an object.
- **Type**: Can do the same but is also useful for creating more complex types like unions or intersections.

### Example:
```ts
type Status = 'success' | 'error';  // Union of literal types
```

---

### 9. **Modules in TypeScript**:
- Modules split your code into different files. You export and import code between files.

### Example:
```ts
// user.ts
export interface User { name: string; }

// main.ts
import { User } from './user';
```

---

### 10. **Inheritance**:
- **Inheritance** allows a class to inherit properties and methods from another class using `extends`.

### Example:
```ts
class Animal {
  speak() {
    console.log('Animal sound');
  }
}

class Dog extends Animal {
  bark() {
    console.log('Woof!');
  }
}
```

---

---

##**Angular coding questions**,

---

### **Components and Directives**

#### 1. **Create a custom directive to format a phone number**

**Explanation**:
A custom directive can be used to format phone numbers in the template when the input changes.

```ts
import { Directive, HostListener, ElementRef } from '@angular/core';

@Directive({
  selector: '[phoneFormat]'
})
export class PhoneFormatDirective {
  constructor(private el: ElementRef) {}

  @HostListener('input', ['$event.target.value'])
  formatPhone(value: string) {
    let formatted = value.replace(/\D/g, ''); // Remove non-digits
    if (formatted.length > 3) formatted = formatted.slice(0, 3) + '-' + formatted.slice(3);
    if (formatted.length > 6) formatted = formatted.slice(0, 7) + '-' + formatted.slice(7);
    this.el.nativeElement.value = formatted;
  }
}
```

**Explanation**:  
This directive listens for the input event on a field and automatically formats it as a phone number by removing non-digit characters and inserting hyphens.

---

#### 2. **Pass data between parent and child components**

**Explanation**:
Use `@Input()` for parent-to-child communication and `@Output()` for child-to-parent communication.

```ts
// Parent Component (parent.component.ts)
@Component({
  selector: 'app-parent',
  template: `<app-child [data]="parentData" (childEvent)="handleChildEvent($event)"></app-child>`
})
export class ParentComponent {
  parentData = 'Message from Parent';
  
  handleChildEvent(data: string) {
    console.log('Received from child:', data);
  }
}

// Child Component (child.component.ts)
@Component({
  selector: 'app-child',
  template: `<button (click)="sendToParent()">Send to Parent</button>`
})
export class ChildComponent {
  @Input() data: string;
  @Output() childEvent = new EventEmitter<string>();

  sendToParent() {
    this.childEvent.emit('Message from Child');
  }
}
```

**Explanation**:  
The parent sends data to the child using `@Input()` and receives data from the child using an `@Output()` event emitter.

---

#### 3. **Dynamically create components**

**Explanation**:
You can dynamically create a component using `ComponentFactoryResolver`.

```ts
// DynamicComponentLoader (dynamic.component.ts)
@Component({
  selector: 'app-dynamic',
  template: `<ng-template #container></ng-template>`
})
export class DynamicComponentLoader {
  @ViewChild('container', { read: ViewContainerRef }) container: ViewContainerRef;

  constructor(private resolver: ComponentFactoryResolver) {}

  loadComponent(component: Type<any>) {
    const factory = this.resolver.resolveComponentFactory(component);
    this.container.clear(); // Clear previously loaded components
    this.container.createComponent(factory); // Load the new component
  }
}
```

**Explanation**:  
This example dynamically creates a component using `ComponentFactoryResolver` and inserts it into the `ViewContainerRef`.

---

### **Services and Dependency Injection**

#### 4. **Create a singleton service**

**Explanation**:
Angular services are singletons by default when provided in the root injector (`providedIn: 'root'`).

```ts
@Injectable({
  providedIn: 'root'
})
export class SingletonService {
  constructor() {}
}
```

**Explanation**:  
This service is provided at the root level, ensuring that only one instance exists throughout the application.

---

#### 5. **Implement a service with dependency injection**

**Explanation**:
You can inject services into components or other services using Angular’s dependency injection system.

```ts
@Injectable()
export class DataService {
  getData() {
    return 'Data from service';
  }
}

// Inject DataService into a component
@Component({
  selector: 'app-example',
  template: `{{ data }}`
})
export class ExampleComponent implements OnInit {
  data: string;

  constructor(private dataService: DataService) {}

  ngOnInit() {
    this.data = this.dataService.getData();
  }
}
```

**Explanation**:  
`DataService` is injected into `ExampleComponent`, allowing it to access the service’s methods.

---

### **Forms and Validation**

#### 6. **Form validation for an email field**

**Explanation**:
You can use Angular’s reactive forms to implement form validation.

```ts
@Component({
  selector: 'app-email-form',
  template: `
    <form [formGroup]="emailForm">
      <input formControlName="email" placeholder="Email">
      <div *ngIf="email.invalid && email.touched">Invalid Email</div>
    </form>
  `
})
export class EmailFormComponent implements OnInit {
  emailForm: FormGroup;

  constructor(private fb: FormBuilder) {}

  ngOnInit() {
    this.emailForm = this.fb.group({
      email: ['', [Validators.required, Validators.email]]
    });
  }

  get email() {
    return this.emailForm.get('email');
  }
}
```

**Explanation**:  
The form checks whether the email field is valid (required and formatted correctly) using Angular's built-in validators.

---

#### 7. **Dynamically add/remove form controls**

**Explanation**:
You can add or remove controls from a form dynamically using `FormArray`.

```ts
@Component({
  selector: 'app-dynamic-form',
  template: `
    <form [formGroup]="form">
      <div formArrayName="items">
        <div *ngFor="let item of items.controls; let i=index">
          <input [formControlName]="i" placeholder="Item {{i + 1}}">
          <button (click)="removeItem(i)">Remove</button>
        </div>
      </div>
      <button (click)="addItem()">Add Item</button>
    </form>
  `
})
export class DynamicFormComponent implements OnInit {
  form: FormGroup;

  constructor(private fb: FormBuilder) {}

  ngOnInit() {
    this.form = this.fb.group({
      items: this.fb.array([])
    });
  }

  get items() {
    return this.form.get('items') as FormArray;
  }

  addItem() {
    this.items.push(this.fb.control(''));
  }

  removeItem(index: number) {
    this.items.removeAt(index);
  }
}
```

**Explanation**:  
This example dynamically adds or removes input fields in a form using `FormArray`.

---

#### 8. **Custom form validation (password confirmation)**

**Explanation**:
A custom validator checks if the password and confirm password fields match.

```ts
@Component({
  selector: 'app-password-form',
  template: `
    <form [formGroup]="passwordForm">
      <input formControlName="password" placeholder="Password">
      <input formControlName="confirmPassword" placeholder="Confirm Password">
      <div *ngIf="passwordForm.errors?.passwordMismatch">Passwords do not match</div>
    </form>
  `
})
export class PasswordFormComponent implements OnInit {
  passwordForm: FormGroup;

  constructor(private fb: FormBuilder) {}

  ngOnInit() {
    this.passwordForm = this.fb.group({
      password: [''],
      confirmPassword: ['']
    }, { validators: this.passwordMatchValidator });
  }

  passwordMatchValidator(form: FormGroup) {
    return form.get('password').value === form.get('confirmPassword').value
      ? null
      : { passwordMismatch: true };
  }
}
```

**Explanation**:  
The custom validator checks if the `password` and `confirmPassword` fields are equal.

---

### **Observables and RxJS**

#### 9. **Handle multiple API calls with `forkJoin`**

**Explanation**:
`forkJoin` combines multiple observables and waits for all to complete before emitting the results.

```ts
forkJoin([
  this.http.get('/api/data1'),
  this.http.get('/api/data2')
]).subscribe(([data1, data2]) => {
  console.log(data1, data2);
});
```

**Explanation**:  
This code makes two API calls concurrently and processes the results together.

---

#### 10. **Create a simple observable**

**Explanation**:
You can create an observable using the `Observable` constructor.

```ts
const observable = new Observable(observer => {
  observer.next('First value');
  observer.next('Second value');
  observer.complete();
});

observable.subscribe(value => {
  console.log(value);
});
```

**Explanation**:  
The observable emits values and completes. The subscriber logs the emitted values.

---

#### 11. **Implement debouncing with RxJS**

**Explanation**:
Debouncing limits the number of API calls or events by delaying the execution.

```ts
import { fromEvent } from 'rxjs';
import { debounceTime, map } from 'rxjs/operators';

const searchInput = document.getElementById('search');
const search$ = fromEvent(searchInput, 'input').pipe(
  debounceTime(300),
  map(event => event.target.value)
);

search$.subscribe(value => {
  console.log('Search:', value);
});
```

**Explanation**:  
The input event is debounced, meaning the event is triggered after the user stops typing for 300ms.

---

### **HttpClient**

#### 12. **Handle HTTP errors globally with `HttpInterceptor`**

**Explanation**:
An `HttpInterceptor` can intercept requests or responses to handle errors globally, such as logging errors or redirecting to an error page. You can handle HTTP errors globally by intercepting HTTP requests and responses.

```ts
@Injectable()
export class ErrorInterceptor implements HttpInterceptor {
  intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
    return next.handle(req).pipe(
      catchError((error: HttpErrorResponse) => {
        console.error('Error occurred:', error);
        return throwError(error); // Rethrow error for further handling
      })
    );
  }
}
```

**Explanation**:  
This interceptor catches HTTP errors, logs them, and rethrows them for further handling.

---

#### 13. **Make an API call using `HttpClient`**

**Explanation**:
Angular’s `HttpClient` is used for making API calls, and it automatically handles JSON responses.

```ts
@Injectable()
export class ApiService {
  constructor(private http: HttpClient) {}

  getData() {
    return this.http.get('/api/data');
  }
}

// In your component
@Component({
  selector: 'app-example',
  template: `<div *ngIf="data">{{ data }}</div>`
})
export class ExampleComponent implements OnInit {
  data: any;

  constructor(private apiService: ApiService) {}

  ngOnInit() {
    this.apiService.getData().subscribe(response => {
      this.data = response;
    });
  }
}
```

**Explanation**:  
The service `ApiService` makes an API call using `HttpClient.get()`, and the result is displayed in the component once received.

---

### **Pipes**

#### 14. **Create a custom pipe to filter an array of objects by a specific field**

**Explanation**:
A custom pipe can be used to filter an array based on a specific property of the objects.

```ts
@Pipe({
  name: 'filterByField'
})
export class FilterByFieldPipe implements PipeTransform {
  transform(items: any[], field: string, value: any): any[] {
    return items.filter(item => item[field] === value);
  }
}

// Usage in template
<ul>
  <li *ngFor="let item of items | filterByField: 'status': 'active'">{{ item.name }}</li>
</ul>
```

**Explanation**:  
This custom pipe filters the array `items` by the field `status` and only displays items with the value `'active'`.

---

#### 15. **Write a pipe that transforms a string into uppercase letters**

**Explanation**:
This pipe transforms the input string to uppercase using `toUpperCase()`.

```ts
@Pipe({
  name: 'uppercase'
})
export class UppercasePipe implements PipeTransform {
  transform(value: string): string {
    return value.toUpperCase();
  }
}

// Usage in template
<p>{{ 'hello world' | uppercase }}</p>
```

**Explanation**:  
The pipe simply converts the input string to uppercase and is applied in the template using the `|` (pipe) operator.

---

### **Lifecycle Hooks**

#### 16. **Component with `ngOnInit` and `ngAfterViewInit`**

**Explanation**:
Lifecycle hooks help control a component's initialization and view rendering process.

```ts
@Component({
  selector: 'app-lifecycle',
  template: `<p>Check the console for lifecycle logs</p>`
})
export class LifecycleComponent implements OnInit, AfterViewInit {
  ngOnInit() {
    console.log('ngOnInit: Component Initialized');
  }

  ngAfterViewInit() {
    console.log('ngAfterViewInit: View Initialized');
  }
}
```

**Explanation**:  
`ngOnInit` is triggered after component initialization, while `ngAfterViewInit` runs after the view is fully initialized.

---

#### 17. **Use `ngOnDestroy` to clean up subscriptions**

**Explanation**:
`ngOnDestroy` is used to clean up resources, such as unsubscribing from observables, when a component is destroyed.

```ts
@Component({
  selector: 'app-cleanup',
  template: `Cleanup Demo`
})
export class CleanupComponent implements OnInit, OnDestroy {
  private subscription: Subscription;

  ngOnInit() {
    this.subscription = interval(1000).subscribe(val => console.log(val));
  }

  ngOnDestroy() {
    this.subscription.unsubscribe(); // Clean up the subscription
    console.log('Component destroyed, subscription cleaned up');
  }
}
```

**Explanation**:  
Here, the `ngOnDestroy` hook unsubscribes from the observable to avoid memory leaks when the component is destroyed.

---

### **State Management**

#### 18. **Manage state across components using a service**

**Explanation**:
You can share data between components using a service and observables to keep the data reactive.

```ts
@Injectable({
  providedIn: 'root'
})
export class StateService {
  private dataSubject = new BehaviorSubject<string>('Initial Data');
  data$ = this.dataSubject.asObservable();

  updateData(newData: string) {
    this.dataSubject.next(newData);
  }
}
```

**Explanation**:  
This service uses `BehaviorSubject` to store and emit shared data across components. Components can subscribe to `data$` to receive updates.

---

#### 19. **Share data between unrelated components**

**Explanation**:
Use a shared service to communicate between unrelated components.

```ts
// Component A
@Component({
  selector: 'app-component-a',
  template: `<button (click)="sendData()">Send Data</button>`
})
export class ComponentA {
  constructor(private stateService: StateService) {}

  sendData() {
    this.stateService.updateData('Data from Component A');
  }
}

// Component B
@Component({
  selector: 'app-component-b',
  template: `<p>Data: {{ data }}</p>`
})
export class ComponentB implements OnInit {
  data: string;

  constructor(private stateService: StateService) {}

  ngOnInit() {
    this.stateService.data$.subscribe(data => {
      this.data = data;
    });
  }
}
```

**Explanation**:  
Both `ComponentA` and `ComponentB` use `StateService` to share and react to data changes.

---

### **Change Detection**

#### 20. **Component with `OnPush` change detection strategy**

**Explanation**:
The `OnPush` strategy only checks for changes when the input properties change, optimizing performance.

```ts
@Component({
  selector: 'app-on-push',
  template: `<p>{{ data }}</p>`,
  changeDetection: ChangeDetectionStrategy.OnPush
})
export class OnPushComponent {
  @Input() data: string;
}
```

**Explanation**:  
This component will only detect changes when the input property `data` changes, thus reducing unnecessary change detection cycles.

---

#### 21. **Manually trigger change detection**

**Explanation**:
You can manually trigger change detection using `ChangeDetectorRef`.

```ts
@Component({
  selector: 'app-manual-detection',
  template: `<button (click)="update()">Update</button><p>{{ data }}</p>`
})
export class ManualDetectionComponent {
  data: string = 'Initial Data';

  constructor(private cdr: ChangeDetectorRef) {}

  update() {
    this.data = 'Updated Data';
    this.cdr.detectChanges(); // Manually trigger change detection
  }
}
```

**Explanation**:  
`detectChanges()` triggers change detection manually, updating the template even if the change detection strategy is `OnPush`.

---

### **Testing**

#### 22. **Unit test for a service using Jasmine and Karma**

**Explanation**:
Jasmine and Karma are used to test Angular services.

```ts
describe('MyService', () => {
  let service: MyService;

  beforeEach(() => {
    TestBed.configureTestingModule({
      providers: [MyService]
    });
    service = TestBed.inject(MyService);
  });

  it('should return correct value', () => {
    expect(service.getData()).toBe('expected value');
  });
});
```

**Explanation**:  
This test checks if the `MyService` returns the expected value when `getData()` is called.

---

#### 23. **Mock HTTP call in a unit test for `HttpClient` service**

**Explanation**:
Mock HTTP calls using `HttpTestingController` to simulate responses in unit tests.

```ts
describe('ApiService', () => {
  let service: ApiService;
  let httpMock: HttpTestingController;

  beforeEach(() => {
    TestBed.configureTestingModule({
      imports: [HttpClientTestingModule],
      providers: [ApiService]
    });
    service = TestBed.inject(ApiService);
    httpMock = TestBed.inject(HttpTestingController);
  });

  it('should fetch data successfully', () => {
    const mockData = { name: 'Test' };

    service.getData().subscribe(data => {
      expect(data).toEqual(mockData);
    });

    const req = httpMock.expectOne('/api/data');
    expect(req.request.method).toBe('GET');
    req.flush(mockData);
  });

  afterEach(() => {
    httpMock.verify(); // Ensure no outstanding requests
  });
});
```

**Explanation**:  
The test mocks the HTTP request and response, verifying that the service's `getData()` method fetches the correct data.

---

### **Lazy Loading**

#### 24. **Lazy load a module in Angular**

**Explanation**:
Lazy loading improves performance by loading modules only when required, instead of during initial loading.

Lazy loading defers the loading of a module until it's needed, improving the initial load time of the application.

```ts
const routes: Routes = [
  { path: 'feature', loadChildren: () => import('./feature/feature.module').then(m => m.FeatureModule) }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule {}
```

**Explanation**:  
This code defines a route for the `FeatureModule`, which is lazy-loaded when the user navigates to the `/feature` path, optimizing the initial loading performance of the application.

---

#### 25. **Lazy load child routes in Angular**

**Explanation**:
Child routes can also be lazy-loaded to further break down the application into smaller, more efficient bundles.

```ts
// feature-routing.module.ts
const routes: Routes = [
  { path: '', component: FeatureComponent },
  { path: 'child', loadChildren: () => import('./child/child.module').then(m => m.ChildModule) }
];

@NgModule({
  imports: [RouterModule.forChild(routes)],
  exports: [RouterModule]
})
export class FeatureRoutingModule {}
```

**Explanation**:  
In this example, the `ChildModule` is lazily loaded only when the user navigates to `/feature/child`, improving application performance.

---

### **Angular Animations**

#### 26. **Fade-in/Fade-out animation using Angular’s animation API**

**Explanation**:
Angular animations allow you to define complex transitions between component states.

```ts
import { trigger, state, style, animate, transition } from '@angular/animations';

@Component({
  selector: 'app-fade',
  template: `<div [@fadeInOut]="'in'">Fade Animation</div>`,
  animations: [
    trigger('fadeInOut', [
      transition(':enter', [style({ opacity: 0 }), animate('600ms', style({ opacity: 1 }))]),
      transition(':leave', [animate('600ms', style({ opacity: 0 }))])
    ])
  ]
})
export class FadeComponent {}
```

**Explanation**:  
This animation fades in the component when it is rendered (`:enter`) and fades out when it is removed from the DOM (`:leave`).

---

#### 27. **Animate a route transition between components**

**Explanation**:
Route transitions can be animated using Angular’s built-in animation triggers.

```ts
@Component({
  selector: 'app-root',
  template: `<div [@routeAnimation]="getRouterOutletState(o)" [@.disabled]="!enableAnimations"></div>`,
  animations: [
    trigger('routeAnimation', [
      transition('* <=> *', [
        style({ opacity: 0 }),
        animate('0.5s ease-in-out', style({ opacity: 1 }))
      ])
    ])
  ]
})
export class AppComponent {
  getRouterOutletState(outlet: RouterOutlet) {
    return outlet.isActivated ? outlet.activatedRoute : '';
  }
}
```

**Explanation**:  
This code sets up a fade animation for transitions between different routes, improving the overall user experience during navigation.

---

### **Angular Material**

#### 28. **Material data table with pagination and sorting**

**Explanation**:
Angular Material provides a `MatTable` component for displaying data along with `MatPaginator` and `MatSort` for pagination and sorting.

```ts
@Component({
  selector: 'app-table',
  template: `
    <table mat-table [dataSource]="dataSource" matSort>
      <!-- Columns go here -->
    </table>
    <mat-paginator [pageSize]="10"></mat-paginator>
  `
})
export class TableComponent implements OnInit {
  dataSource = new MatTableDataSource(ELEMENT_DATA);

  @ViewChild(MatPaginator) paginator: MatPaginator;
  @ViewChild(MatSort) sort: MatSort;

  ngOnInit() {
    this.dataSource.paginator = this.paginator;
    this.dataSource.sort = this.sort;
  }
}
```

**Explanation**:  
This creates a Material data table with pagination and sorting functionality.

---

#### 29. **Material dialog component for a modal popup**

**Explanation**:
The Angular Material `MatDialog` can be used to create a modal popup.

```ts
@Component({
  selector: 'app-dialog',
  template: `<button (click)="openDialog()">Open Dialog</button>`
})
export class DialogComponent {
  constructor(public dialog: MatDialog) {}

  openDialog() {
    this.dialog.open(DialogContentComponent);
  }
}

@Component({
  selector: 'app-dialog-content',
  template: `<h1>Dialog Content</h1>`
})
export class DialogContentComponent {}
```

**Explanation**:  
This code opens a modal dialog with custom content using the `MatDialog` service from Angular Material.

---

### **Guards and Authentication**

#### 30. **Create a route guard to restrict access based on authentication status**

**Explanation**:
Route guards in Angular can prevent unauthorized users from accessing certain routes.

```ts
@Injectable({
  providedIn: 'root'
})
export class AuthGuard implements CanActivate {
  constructor(private authService: AuthService, private router: Router) {}

  canActivate(): boolean {
    if (this.authService.isAuthenticated()) {
      return true;
    } else {
      this.router.navigate(['/login']);
      return false;
    }
  }
}
```

**Explanation**:  
This guard checks if the user is authenticated. If not, it redirects them to the login page.

---

#### 31. **AuthGuard to check if a user has a valid token before navigating**

**Explanation**:
This guard checks if a valid authentication token is present before allowing route navigation.

```ts
@Injectable({
  providedIn: 'root'
})
export class TokenGuard implements CanActivate {
  constructor(private authService: AuthService, private router: Router) {}

  canActivate(): boolean {
    if (this.authService.hasValidToken()) {
      return true;
    } else {
      this.router.navigate(['/login']);
      return false;
    }
  }
}
```

**Explanation**:  
This guard checks if the user has a valid token by calling a method from the `AuthService`. If the token is invalid, the user is redirected to the login page.

---

### **Performance Optimization**

#### 32. **Lazy loading images in Angular**

**Explanation**:
Lazy loading images ensures that only images within the visible viewport are loaded, improving performance.

```ts
<img [src]="image" loading="lazy" />
```

**Explanation**:  
The `loading="lazy"` attribute allows browsers to defer loading images until they are about to enter the viewport, improving page load times.

---

#### 33. **Optimize a large list using `trackBy` in `ngFor`**

**Explanation**:
`trackBy` optimizes rendering large lists by keeping track of changes in the list and preventing unnecessary re-rendering.

```ts
<ul>
  <li *ngFor="let item of items; trackBy: trackById">{{ item.name }}</li>
</ul>

trackById(index: number, item: any): number {
  return item.id;
}
```

**Explanation**:  
By using `trackBy`, Angular can track items by their unique identifier (`id`), ensuring that only modified elements are re-rendered, improving performance.

---

### **HTTP and Interceptors**

#### 34. **`HttpInterceptor` to append an authentication token**

**Explanation**:
An interceptor can modify outgoing requests, such as appending an authentication token to the headers.

```ts
@Injectable()
export class AuthInterceptor implements HttpInterceptor {
  constructor(private authService: AuthService) {}

  intercept(req: HttpRequest<any>, next: HttpHandler): Observable<HttpEvent<any>> {
    const authToken = this.authService.getToken();
    const authReq = req.clone({
      setHeaders: {
        Authorization: `Bearer ${authToken}`
      }
    });
    return next.handle(authReq);
  }
}
```

**Explanation**:  
This interceptor adds an `Authorization` header containing the token to each outgoing request.

---

#### 35. **Retry logic with `HttpClient` and RxJS**

**Explanation**:
You can use `retry()` from RxJS to retry failed HTTP requests a specified number of times.

```ts
this.http.get('/api/data').pipe(
  retry(3), // Retry the request up to 3 times
  catchError(error => {
    console.error('Request failed');
    return throwError(error);
  })
).subscribe(data => console.log(data));
```

**Explanation**:  
The `retry()` operator attempts to resend the HTTP request up to 3 times before throwing an error.

---

### **Reusable Components**

#### 36. **Reusable dropdown component**

**Explanation**:
A reusable dropdown component accepts a list of options and emits the selected value.

```ts
@Component({
  selector: 'app-dropdown',
  template: `
    <select (change)="onSelect($event)">
      <option *ngFor="let option of options" [value]="option">{{ option }}</option>
    </select>
  `
})
export class DropdownComponent {
  @Input() options: string[] = [];
  @Output() selected = new EventEmitter<string>();

  onSelect(event: Event) {
    const value = (event.target as HTMLSelectElement).value;
    this.selected.emit(value);
  }
}
```

**Explanation**:  
This component emits the selected value when an option is chosen, making it reusable across the application.

---

#### 37. **Reusable toast notification component**

**Explanation**:
A reusable toast notification component displays messages on the screen. A toast notification component can be used to display alerts or messages to the user, which disappear after a few seconds.

```ts
@Component({
  selector: 'app-toast',
  template: `
    <div *ngIf="message" class="toast">{{ message }}</div>
  `,
  styles: [`
    .toast {
      position: fixed;
      bottom: 10px;
      right: 10px;
      background-color: #333;
      color: #fff;
      padding: 10px;
      border-radius: 5px;
    }
  `]
})
export class ToastComponent {
  @Input() message: string;

  constructor() {
    setTimeout(() => this.message = '', 3000); // Hide the toast after 3 seconds
  }
}
```

**Explanation**:  
This reusable toast component shows a message for 3 seconds before hiding itself.

---

### **Dependency Injection**

#### 38. **Inject multiple providers using dependency injection**

**Explanation**:
You can inject multiple services or configurations into a service using Angular's dependency injection.

```ts
@Injectable()
export class MultiProviderService {
  constructor(
    private httpClient: HttpClient,
    private logger: LoggerService
  ) {}

  fetchData() {
    this.logger.log('Fetching data...');
    return this.httpClient.get('/api/data');
  }
}
```

**Explanation**:  
Here, `MultiProviderService` injects both `HttpClient` and `LoggerService`, demonstrating how multiple providers can be injected.

---

#### 39. **Use `useClass` and `useFactory` in dependency injection**

**Explanation**:
`useClass` and `useFactory` allow customization of how services are provided.

```ts
@Injectable()
export class MockDataService {
  getData() {
    return 'Mock Data';
  }
}

@NgModule({
  providers: [
    { provide: DataService, useClass: MockDataService }, // useClass example
    { provide: LoggerService, useFactory: () => new LoggerService('AppLogger') } // useFactory example
  ]
})
export class AppModule {}
```

**Explanation**:  
`useClass` replaces `DataService` with `MockDataService`. `useFactory` allows creating an instance of `LoggerService` with a custom parameter.

---

### **Router**

#### 40. **Implement a route resolver to fetch data before navigation**

**Explanation**:
A route resolver fetches data before the user navigates to a particular route.

```ts
@Injectable()
export class DataResolver implements Resolve<any> {
  constructor(private dataService: DataService) {}

  resolve(): Observable<any> {
    return this.dataService.getData();
  }
}

const routes: Routes = [
  {
    path: 'data-route',
    component: DataComponent,
    resolve: { data: DataResolver }
  }
];
```

**Explanation**:  
`DataResolver` fetches data from `DataService` before navigating to the `DataComponent`.

---

#### 41. **Handle query parameters and route parameters together**

**Explanation**:
You can retrieve both query and route parameters in a component by subscribing to the `ActivatedRoute` service.

```ts
@Component({
  selector: 'app-route-example',
  template: `Route Param: {{ routeParam }} | Query Param: {{ queryParam }}`
})
export class RouteExampleComponent implements OnInit {
  routeParam: string;
  queryParam: string;

  constructor(private route: ActivatedRoute) {}

  ngOnInit() {
    this.route.paramMap.subscribe(params => {
      this.routeParam = params.get('id');
    });
    this.route.queryParamMap.subscribe(queryParams => {
      this.queryParam = queryParams.get('search');
    });
  }
}
```

**Explanation**:  
This component handles both route parameters (`/route/:id`) and query parameters (`?search=...`) by subscribing to the `paramMap` and `queryParamMap`.

---

### **Internationalization (i18n)**

#### 42. **Implement Angular’s i18n for localization**

**Explanation**:
Angular provides built-in support for i18n (internationalization) to translate applications into multiple languages.

```html
<!-- src/app.component.html -->
<p i18n>Hello World</p>
```

1. Mark up the text for translation using the `i18n` attribute.
2. Use the Angular CLI to extract translations:  
   `ng extract-i18n`
3. Add translations in the generated `messages.xlf` file.
4. Compile the app for a specific language using:  
   `ng serve --configuration=fr`

**Explanation**:  
This example shows how to mark content for translation and prepare the app for localization.

---

#### 43. **Dynamically change the language of an Angular app**

**Explanation**:
To dynamically change the language, you can reload the application or use a translation library like `ngx-translate`.

```ts
@Component({
  selector: 'app-language-switcher',
  template: `
    <button (click)="changeLanguage('en')">English</button>
    <button (click)="changeLanguage('fr')">French</button>
  `
})
export class LanguageSwitcherComponent {
  constructor(private translate: TranslateService) {}

  changeLanguage(lang: string) {
    this.translate.use(lang); // Switch language dynamically
  }
}
```

**Explanation**:  
Here, `ngx-translate` allows you to dynamically switch between languages at runtime without reloading the app.

---

These answers include detailed explanations and code snippets for each of the Angular concepts, helping you understand both the concept and its practical implementation. Let me know if you need more details on any specific topic!
