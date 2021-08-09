# Learn-React

*npx create-react-app my-app*

## React

 JavaScript-библиотека с открытым исходным кодом для разработки пользовательских интерфейсов.
 
 ## Component 
 
Это функция, которая принимает входные данные (props) и возвращает React-элементы, описывающие, что должно появиться на экране (JSX разметку). При вызове компоненты, по умолчанию, у него есть пустой объект (props). Далее, атрибутами (свойствами), мы наполняем этот объект и передаем в другую компоненту.
Компоненты позволяют разделить пользовательский интерфейс на независимые, повторно используемые части и работать с каждой из частей отдельно. Компоненты React можно помещать в другие компоненты.

## Props

Настраиваемые данные (объекты), которые задаются в виде атрибута компонента и хранятся в объекте под видом Ключ : Значение.
```jsx
props {
  name : 'Dima',
  age : 25
}
```
Передаются в компонент данным образом.
```jsx
<Welcome name='Dima' age='25' />
```

Props всегда передаются от родительского элемента к дочернему. 

## JSX (JavaScript XML) 

Расширение (синтаксис) языка JavaScript. JSX производит «элементы» React и позволяет писать HTML код внутри JavaScript файла. 

## CallBack

Это функция, которая должна быть выполнена после того, как другая функция завершит работу.
```jsx
const addPost = () => { 
  alert(text)
}
```
Мы можем вызвать её стандартным способом addPost(). Либо же передать её внутрь другой функции.
```jsx
<button onClick={addPost}>Отправить</button>
```

## Pure Function 

Функция, которая не пытается изменить свои аргументы и всегда возвращает один и тот же результат для одних и тех же входных данных. Все React-компоненты должны вести себя как чистые функции в плане своих свойств.

## Side-effect 

Это когда функция меняет что-либо, находящееся за её границами. К примеру, функция, отправляющая fetch-запрос, создаёт сайд-эффект. Ещё одним примером сайд-эффекта является обращение к localStorage.

## Higher-Order Function (HOC)

Один из многих концептов функционального программирования. Функцией высшего порядка можно назвать любую обычную функцию, которая принимает другую функцию в качестве аргумента, и/или производит ещё одну функцию в качестве возвращаемого значения. Создаётся обёртка над принятой компонентой, и функция снабжает её новой логикой - данными.

# React Hooks

Это функции, с помощью которых можно «подцепиться» к состоянию и методам жизненного цикла React из функциональных компонентов. Появились в версии 16.8.

## useState 

Предоставляет функциональным компонентам доступ к локальному состоянию React.
```jsx
const [count, setCount] = useState(0) // в скобках useState указываем начальное состояние.
```
Вызов useState возвращает 2 значения: первое значение - текущее состояние, а второе - функция, обновляющая это состояние.

React будет хранить это состояние между рендерами и передавать его функции useState. Если нужно будет изменить count, мы вызовем setCount.

## useEffect 

Даёт возможность выполнять побочные (side-effect) эффекты в функциональном компоненте. Побочными эффектами в React-компонентах могут быть: загрузка данных, оформление подписки и изменение DOM вручную. Он выполняет ту же роль, что и componentDidMount, componentDidUpdate и componentWillUnmount в React-классах, объединив их в единый API.

```jsx
// Аналогично componentDidMount и componentDidUpdate:
  useEffect(() => {
    // Обновляем заголовок документа с помощью API браузера
    document.title = `Вы нажали ${count} раз`;
  });
````

Используя этот хук, React будет делать что-то после рендера. React запомнит функцию (то есть «эффект»), которая передается и вызовет её после того, как внесёт все изменения в DOM.

Принимает 2 параметра, анонимную функцию и массив зависимостей.
В массиве зависимостей, мы указываем переменную за которой нужно следить, чтобы перерисовывать компоненту, каждый раз, когда переменная меняется. (componentDidUpdate )
Пустой массив зависимостей, указывает на то, что не нужно незачем следить, а вызвать функцию только один раз, когда компонента отрисуется (componentDidMount). Если не указать второй параметр (массив), то функция будет вызываться при каждом изменении в компоненте.

# React-Router

*yarn add react-router-dom*

## UseHistory

Каждый Router создает объект history который хранит путь и перерисовывает интерфейс сайта когда происходят какие то изменения пути.

У UseHistory есть следующие методы: 

history.push - добавляет новую запись в историю.
history.replace - заменяет текущий путь в истории.

# React Hook Form 7

*yarn add react-hook-form*
