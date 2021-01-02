Title: Angular + Bootstrap
Author: mkostyrko
Date: 2020-12-29
 12:00
Updated:
Category: angular
Tags: bootstrap, angular, javascript
Slug: angular-bootstrap
related_posts: 



![angular-bootstrap](https://therichpost.com/wp-content/uploads/2020/11/Add-Bootstrap-in-Angular-11.png)


### Angular + Bootstrap

[ng-bootstrap](https://ng-bootstrap.github.io/#/home)

### Instalacja


    ng add @ng-bootstrap/ng-bootstrap

### Setup

AppComponent
    import {NgbConfig} from '@ng-bootstrap/ng-bootstrap';

    export class AppComponent {
      constructor(ngbConfig: NgbConfig) {
        ngbConfig.animation = false;
      }
    }


### Przykład zastosowania (Nav)

**ts - basic nav**


    import {Component} from '@angular/core';

    @Component({
      selector: 'ngbd-nav-basic',
      templateUrl: './nav-basic.html'
    })
    export class NgbdNavBasic {
      active = 1;
    }


**html - basic-nav**

    <ul ngbNav #nav="ngbNav" [(activeId)]="active" class="nav-tabs">
      <li [ngbNavItem]="1">
        <a ngbNavLink>One</a>
        <ng-template ngbNavContent>
          <p>Raw denim you probably haven't heard of them jean shorts Austin. Nesciunt tofu stumptown aliqua, retro synth
            master cleanse. Mustache cliche tempor, williamsburg carles vegan helvetica. Reprehenderit butcher retro
            keffiyeh dreamcatcher synth. Cosby sweater eu banh mi, qui irure terry richardson ex squid. Aliquip placeat
            salvia cillum iphone. Seitan aliquip quis cardigan american apparel, butcher voluptate nisi qui.</p>
        </ng-template>
      </li>
      <li [ngbNavItem]="2">
        <a ngbNavLink>Two</a>
        <ng-template ngbNavContent>
          <p>Exercitation +1 labore velit, blog sartorial PBR leggings next level wes anderson artisan four loko
            farm-to-table craft beer twee. Qui photo booth letterpress, commodo enim craft beer mlkshk aliquip jean shorts
            ullamco ad vinyl cillum PBR. Homo nostrud organic, assumenda labore aesthetic magna delectus mollit. Keytar
            helvetica VHS salvia yr, vero magna velit sapiente labore stumptown. Vegan fanny pack odio cillum wes anderson
            8-bit, sustainable jean shorts beard ut DIY ethical culpa terry richardson biodiesel. Art party scenester
            stumptown, tumblr butcher vero sint qui sapiente accusamus tattooed echo park.</p>
        </ng-template>
      </li>
      <li [ngbNavItem]="3">
        <a ngbNavLink>Three</a>
        <ng-template ngbNavContent>
          <p>Sed commodo, leo at suscipit dictum, quam est porttitor sapien, eget sodales nibh elit id diam. Nulla facilisi.
            Donec egestas ligula vitae odio interdum aliquet. Duis lectus turpis, luctus eget tincidunt eu, congue et odio.
            Duis pharetra et nisl at faucibus. Quisque luctus pulvinar arcu, et molestie lectus ultrices et. Sed diam urna,
            egestas ut ipsum vel, volutpat volutpat neque. Praesent fringilla tortor arcu. Vivamus faucibus nisl enim, nec
            tristique ipsum euismod facilisis. Morbi ut bibendum est, eu tincidunt odio. Orci varius natoque penatibus et
            magnis dis parturient montes, nascetur ridiculus mus. Mauris aliquet odio ac lorem aliquet ultricies in eget
            neque. Phasellus nec tortor vel tellus pulvinar feugiat.</p>
        </ng-template>
      </li>
    </ul>

<div [ngbNavOutlet]="nav" class="mt-2"></div>

<pre>Active: {{ active }}</pre>

Routing:

    links = [
      { title: 'One', fragment: 'one' },
      { title: 'Two', fragment: 'two' }
    ];

    constructor(public route: ActivatedRoute) {}

---
Źródła:

[Jak dodać Bootstrapa 4 – bootstrap i Angular](https://zacznijprogramowac.net/angular/jak-dodac-bootstrapa-4-do-angulara/)
