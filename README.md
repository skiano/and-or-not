# and-or-not

_NOTE: Tests are missing_

#### Example

The following prints all the numbers between 1 and 50 that are divisible by 2, and divisible by either 3 or 4, and not less than 20.

```javascript

import aon from 'and-or-not';

const data = ['||', ['greaterThan', 'value', 80], 
                    ['greaterThan', 'value', 60]];

const interpreter = {
  greaterThan(model, key, value) {
    return model[key] > value;
  },
  lessThan(model, key, value) {
    return model[key] < value;
  }
}

const model = { value: 70 };
const predicate = aon(data, interpreter);
const bool = predicate(model);

```
