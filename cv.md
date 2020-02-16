# Resume
## Aliaksei Krachkouski, contact info:
|Name:                     | Contacts: |
--------------------------|---------------------------------
| First Name: **Aliaksei** | Telegram: @akrachkowski |
| Last Name: **Krachkouski** | Phone: +375 33 902-92-50 |
|| Mail: a.krachkowski@gmail.com|

## Profile
I am an enthusiast, responsible and hardworking IT specialist. Working earlier in technical support, I developed such qualities as: resistance to stress, sociability, quick completion of tasks. I can work well both in a team environment and on my own initiative. I can work well under pressure and adhere to strict deadlines. I love to learn something new that will help me in my future career.
## Skills
* SQL
* PL/SQL
* JavaScript
* HTML/CSS
## Code Examples
```javascript
(function () {
    const storage = new HashStorage();

    // --------- get/set values of controls ------------

    function getDrinkName() {
        const drinkNameInput = document.getElementById("drink-name");
        if (!!drinkNameInput) {
            return drinkNameInput.value;
        }
    }

    function getDrinkAlco() {
        const drinkAlcoCheckbox = document.getElementById("drink-alco");
        if (!!drinkAlcoCheckbox) {
            return drinkAlcoCheckbox.checked;
        }
    }


    function getDrinkDescription() {
        const drinkDescriptionInput = document.getElementById("drink-description");
        if (!!drinkDescriptionInput) {
            return drinkDescriptionInput.value;
        }
    }

    function setAllDrinksResult(text) {
        const allDrinksLabel = document.getElementById("all-drinks");
        if (!!allDrinksLabel) {
            allDrinksLabel.innerText = text;
        }
    }

    // --------- button events -------------

    function addDrink() {
        const drinkName = getDrinkName();
        const drinkDescription = getDrinkDescription();
        const drinkIsAlco = getDrinkAlco();
        if (!!drinkName) {
            const drink = storage.getValue(drinkName);
            if (!!drink) {
                setAllDrinksResult(`напиток ${drinkName} уже есть в списке`);
            } else {
                storage.addValue(drinkName, {
                    description: drinkDescription,
                    isAlco: drinkIsAlco
                });
                setAllDrinksResult(`напить ${drinkName} добавлен`);
            }
        } else {
            setAllDrinksResult("Введите название напитка");
        }
    }



    function getDrink() {
        const drinkName = getDrinkName();
        if (!drinkName) {
            setAllDrinksResult("Введите название напитка");
            return;
        }
        const drink = storage.getValue(drinkName);
        if (!!drink) {
            setAllDrinksResult(`
            напиток: ${drinkName}; 
            алкогольный: ${drink.value.isAlco ? 'да' : 'нет'}; 
            рецепт: ${drink.value.description || '-'}`);
        } else {
            setAllDrinksResult(`напиток ${drinkName} не найден`);
        }
    }

    function deleteDrink() {
        const drinkName = getDrinkName();
        if (!!drinkName) {
            const isSuccess = storage.deleteValue(drinkName);
            setAllDrinksResult(isSuccess ? `напиток ${drinkName} удалён` : `напиток ${drinkName} не найден или уже был удалён`);
        } else {
            setAllDrinksResult("Введите название напитка");
        }
    }

    function getAllDrinks() {
        const drinks = storage.getKeys();
        if (!drinks.length) {
            setAllDrinksResult('список напитков пуст');
        } else {
            setAllDrinksResult(`Напитки: ${drinks.toString(',')}`)
        }
    }


    // ---------- add events  --------------

    const addBtn = document.getElementById('add-drink');
    if (!!addBtn) {
        addBtn.addEventListener('click', addDrink);
    }

    const getBtn = document.getElementById('get-drink');
    if (!!getBtn) {
        getBtn.addEventListener('click', getDrink);
    }

    const delBtn = document.getElementById('delete-drink');
    if (!!delBtn) {
        delBtn.addEventListener('click', deleteDrink);
    }

    const getAllBtn = document.getElementById('get-all-drinks');
    if (!!getAllBtn) {
        getAllBtn.addEventListener('click', getAllDrinks);
    }

})();
```
## Work experience 
| Company Name| Working at a company | Position|
|----------------------|-------------|--------|
| Rasvikom service LLC | 09/2017 - present| Technical Support Engineer|
| B-Logic ALC | 09/2018 - present | Technical Support Engineer|

## Education
|Place of Study |Subject of study  | Training period|
|--|--|--|
|IT-Academy|JS-courses | 04/2019-09/2019
|Union-Jack|English(B2 level)|09/2018-05/2019
|Finastra company| Angular, Java|02/2018-08/2018
|Belarusian State University. Faculty of Radiophysics and Computer Technology||09/2012-07/2017
 
## English

At first I studied at the university, after which I took a basic course in Streamline, I constantly study it myself through books, watching films in English, etc.
Recently completed a training course in Union Jack. I evaluate the current level as **B1**.