# Box Model

Box model refers to how an element is structured. An element is made up of the content, padding, border and margin. These properties can be changed with css to alter the layout and styling of an element and how they work with other elements on a page.

Border and padding are used to style the element itself, while margin is used to define the space between and around elements on a page.

# JS Exercise

```JS

const sales = [
    { itemSold: "Football", price: 19.99, dateSold: '2018-04-07', id: 'j_123' },
    { itemSold: "Trainers", price: 159.95, dateSold: '2018-03-02', id: 't_acds1' },
    { itemSold: "Cricket bat", price: 204.97, dateSold: '2018-04-05', id: 'j_456'},
    { itemSold: "Rugby ball", price: 30.00, dateSold: '2017-04-22', id: 't_acds3' },
    { itemSold: "Hockey stick", price: 54.95, dateSold: '2017-03-19', id: 'j_999' }
]

// 1
function getTotalPrice() {
    const totalPrice = sales.reduce((totalPrice, item) => totalPrice + item.price, 0).toFixed(2);

    return totalPrice;
}

getTotalPrice();

// 2
function getItemsSoldIn2017() {
    const itemsSoldIn2017 = sales.filter(item => item.dateSold.substring(0, 4) === '2017');

    return itemsSoldIn2017;
}

getItemsSoldIn2017();

// 3
function sortItemsAlphabetically() {
    const items = sales.map(item => item.itemSold);

    const itemsAlphbetically = items.sort();

    return itemsAlphbetically;
}

sortItemsAlphabetically();

// 4
function getItemWithId(id) {
    const itemWithId = sales.find(item => item.id === id);

    return itemWithId;
}

getItemWithId('t_acds1');

```

# How to run Site
In the terminal run the following command to build css:
```
npm run scss 
```
Open site.html in your preferred browser.