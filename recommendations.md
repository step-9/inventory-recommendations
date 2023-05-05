# Recommendations

Recommended directory structure for `inventory`
assignment.

```
inventory-your_github_id
├── .git
├── .gitignore
├── README.md
├── TODO
├── main.js
├── resources
│   ├── inventory.txt
│   └── transactions.log
├── src
│   ├── inventory.js
│   └── transaction.js
└── test
    ├── inventory-test.js
    └── transaction-test.js
```

Recommended `.gitignore`

```
TODO
*.swp
*.swo
resources/
```

Recommended `main.js`

```js
const fs = require('fs'); // do not use anywhere else
// First require node's libraries
// Then require your libraries
const { parseTransaction } = require('./src/transaction.js');
const { parseInventory } = require('./src/inventory.js');

// Ideally no other functions here

const main = function () {
  // load file here
  // parse here
  // reconcile transactions
  // display inventory
};

main();
```

Recommended structure for `transactions`

```js
[
  { from: 'Warehouse', to: 'Dispensary', quantity: 2, item: 'Paracetamol' },
  { from: 'Warehouse', to: 'Dispensary', quantity: 5, item: 'Ibuprofen' },
  { from: 'Dispensary', to: 'ICU', quantity: 2, item: 'Syringe' },
  { from: 'Warehouse', to: 'ICU', quantity: 10, item: 'Scalpel' },
];
```

Recommended structure for `inventory`

```js
{
  Warehouse: { Paracetamol: 10, Ibuprofen: 50, Syringe: 80, Scalpel: 100 },
  ICU: { Paracetamol: 0, Ibuprofen: 20, Syringe: 7, Scalpel: 8 },
  Dispensary: { Paracetamol: 50, Ibuprofen: 33, Syringe: 10, Scalpel: 80 }
}
```

---
