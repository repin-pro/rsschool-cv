## Roman Repin

## My Contact Info

* Address: Russia, Moscow, Zelenograd city
* Phone: +7 995 5007773
* E-mail: roman@repin.pro
* VkontakteID: repin_pro
* GitHub: repin-pro
* CodePen: repin-pro
* Telegram: roman_repin

## Summary

At the moment I am undergoing frontend developer training, I plan to bring HTML, CSS, JS, React/VUE to a professional level. I am also interested in web design and brand development, I study on geekbrains and skillbox platforms.

## Skills

* HTML,
* CSS (Framework Bootstrap, Preprocessor SCSS, BEM methodology),
* JavaScript (Fundamentals,Functional Programming, OOP, Asynchronous JavaScript, ES6+,DOM),
* React JS, Redux (I'm starting to study),
* Version control: Git (remote service GitHub),
* Module Bundlers: Gulp, Webpack,
* Windows OS, Linux(Ubuntu),
* Figma, Adobe (Illustrator, Photoshop) (at the web designer level),
* Editors: VSCode.

## Code examples

```javascript
async function serverGetProducts() {
  try {
    let response = await fetch(SERVER_URL + '/api/products', {
      method: "GET",
      headers: { 'Content-Type': 'application/json' }
    })
    if (response.status === 404) {
      errorWin();
      errorWindows.textContent = 'Список пуст';
      setTimeout(() => {
        errorWin();
      }, 3000);
    }
    if (response.status === 500) {
      errorWin();
      errorWindows.textContent = 'Произошла ошибка, повторная попытка подключения';
      serverGetProducts();
      setTimeout(() => {
        errorWin();
      }, 3000);
    }
    if (response.status === 200) {
      const resultWindows = document.querySelector('.result');
      const data = await response.json();

      for (let i = 0; i < data.products.length; i++) {
        const element = data.products[i];
        let card = document.createElement('div');
        card.className = "card";

        let cardImage = document.createElement('img');
        cardImage.className = 'card-img-top';
        cardImage.src = `${element.image}.jpg`;
        cardImage.alt = `${element.image}.jpg`;

        resultWindows.append(card);
        card.append(cardImage);

        let cardBody = document.createElement('div');
        cardBody.className = 'card-body';
        card.append(cardBody);

        let cardTitle = document.createElement('h5');
        cardTitle.className = 'card-title';
        cardBody.append(cardTitle);
        cardTitle.innerHTML = `${element.name}`;

        let cardText = document.createElement('p');
        cardText.className = 'card-text';
        cardBody.append(cardText);
        cardText.innerHTML = `${element.price}`;

      }
    }
  }
  catch (error) {
    errorWin();
    errorWindows.textContent = 'неожиданная ошибка программы';
    setTimeout(() => {
      errorWin();
    }, 3000);
  }
}
```

## Education

* National Research University "MIET"
    * engineer by specialty: "software of computer technology and automated systems"

* Skillbox
    * frontend developer
    * Web design

* Geekbrains
    * Graphic Designer

## Languages
* Russian - native speaker.
* English - A1 (A2 in process…)