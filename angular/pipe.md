---
title: Pipe
description: This is a post 
date: 2020-11-04
duration: ~30 mins
sections: Task 1
tags:
layout: layouts/post.njk
---


###### Prerequisite #1: Create a transaction data in component

``` js
    transactions = [
        {id: 1, accountNo:123, amount: 100, transactionType:"CREDIT"},
        {id: 2, accountNo:123, amount: 200, transactionType:"DEBIT"},
        {id: 3, accountNo:123, amount: 300, transactionType:"CREDIT"}
    ];
```

```html
    <h3> Transaction Details </h3>
            Filter: Transaction Type:
                <select id="" [(ngModel)]="transactionTypeFilter">
                    <option value="">--ALL--</option>
                    <option value="CREDIT">CREDIT</option>
                    <option value="DEBIT">DEBIT</option>
                </select>


    <table class="table table-bordered">
                <thead>
                    <tr>
                        <th> Id </td>
                        <th>Account No</th>
                        <th>Transaction Type</th>
                        <th> Amount </th>
                    </tr>

                </thead>
                <tbody>
                    <tr *ngFor="let obj of transactions ;let i=index;">
                        
                        <td>{{obj.id}}</td>
                        <td>{{obj.accountNo}}</td>
                        <td>{{obj.transactionType}}</td>
                        <td>{{obj.amount}}</td>
                    </tr>
                </tbody>
            </table>
```



###### Task 1: Create Pipe 

``` js
  ng generate pipe transactionType
```


###### Task 1.1: Default TransactionType Pipe Code 

``` js
    import { Pipe, PipeTransform } from '@angular/core';

    @Pipe({
    name: 'transactionType'
    })
    export class TransactionTypePipe implements PipeTransform {

        transform(value: unknown, ...args: unknown[]): unknown {
            
            return null;
        }

    }

```


###### Task 2: Change transform method parameters

``` js
   transform(items: any[], selectedTransactionType: string): any[] {
    console.log('Transaction Type Pipe:' , selectedTransactionType);
   }
```

###### Task 2.1: Validate input array and selectedTransactionType

``` js
   transform(items: any[], selectedTransactionType: string): any[] {
        if(!items) return [];
        if(!selectedTransactionType ) return items;
   }
```


###### Task 2.2: Implement Filtering logic

``` js
  
  let filteredData =  items.filter( it => {
      return it.transactionType == selectedTransactionType;
    });
  console.log(filteredData);
```

###### Task 2.3: Full Code

``` js
   transform(items: any[], selectedTransactionType: string): any[] {
    console.log('Transaction Type Pipe:' , selectedTransactionType);

    if(!items) return [];
    if(!selectedTransactionType ) return items;
    
    return items.filter( it => {
      return it.transactionType == selectedTransactionType;
    });
  }
```





###### Task 6: Add the pipe in html

Replace
```html
    <tr *ngFor="let obj of transactions ;let i=index;">
```
to
```html
    <tr *ngFor="let obj of (transactions | transactionType: transactionTypeFilter) ;let i=index;">
```

###### Task 7: Implement CommentsSearch Pipe and Combine Pipes in html

```html
     Search By Comments:
        <input type="text" name="comments" [(ngModel)]="searchComment" />

    <tr *ngFor="let obj of (transactions | transactionType: transactionTypeFilter | comments: searchComment) ;let i=index;">
```

```js
    export class CommentsPipe implements PipeTransform {

    transform(items: any[], searchComment: string): any[] {
        if(!items) return [];
        if(!searchComment) return items;
        console.log('Comments  Pipe:' , searchComment);
        return items.filter( it => {
        return it.comments.startsWith( searchComment);
        });
    }

    }
```