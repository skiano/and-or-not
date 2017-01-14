# and-or-not

_NOTE: Code is currently untested!_

#### Example

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
