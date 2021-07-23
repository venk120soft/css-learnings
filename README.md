# css-learnings
css-learnings

Working with RTL Languages like arabic which will be reading starts from right to left 

```javascript
// ex1
.privateOffersIcon {
  [dir='ltr'] & {
    padding-left: 3px;
  }
  [dir='rtl'] & {
    padding-right: 3px;
  }
  transform: translateY(3px);
}

// ex2
.licenseCount {
  margin-left: 40px;
  html[dir="rtl"] {
    margin-right: 40px;
  }
}

// ex3 Chnaging the direction wise versa
.labelWithIcon {
  display: flex;
  align-items: center;
  direction: rtl;

  html[dir="rtl"] {
    direction: ltr;
  }
  span {
    @include font-base();
  }
}

// ex4
.noData {
  display: flex;
  align-items: center;
  svg {
    margin-right: 5px;
  }
}

html[dir="rtl"] {
  .noData {
    svg {
      margin-left: 5px;
    }
  }
}
```
