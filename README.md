# Learn-React

*npx create-react-app my-app*

## React

 JavaScript-библиотека с открытым исходным кодом для разработки пользовательских интерфейсов.
 
 ## Component 
 
Это функция, которая принимает входные данные (props) и возвращает React-элементы, описывающие, что должно появиться на экране (JSX разметку). При вызове компоненты, по умолчанию, у него есть пустой объект (props). Далее, атрибутами (свойствами), мы наполняем этот объект и передаем в другую компоненту.
Компоненты позволяют разделить пользовательский интерфейс на независимые, повторно используемые части и работать с каждой из частей отдельно.

## Props

Настраиваемые данные (объекты), которые задаются в виде атрибута компоненты и хранятся в объекте под видом Ключ : Значение.
```jsx
<Welcome name='Dima' age='25' />
```
Имеет вид находясь в объекте, который в свою очередь является параметром функции:
```jsx
props {
  name : 'Dima',
  age : 25
}
```
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

## Higher-Order Function (HOC)

Один из многих концептов функционального программирования. Функцией высшего порядка можно назвать любую обычную функцию, которая принимает другую функцию в качестве аргумента, и/или производит ещё одну функцию в качестве возвращаемого значения. Создаётся обёртка над принятой компонентой, и функция снабжает её новой логикой - данными.

## Side-effect 

Это когда функция меняет что-либо, находящееся за её границами. К примеру, функция, отправляющая fetch-запрос, создаёт сайд-эффект. Ещё одним примером сайд-эффекта является обращение к localStorage.

# React Hooks

Это функции, с помощью которых можно «подцепиться» к состоянию и методам жизненного цикла React из функциональных компонентов. 

## useState 

Предоставляет функциональным компонентам доступ к локальному состоянию React.
```jsx
const [count, setCount] = useState(0) // в скобках useState указываем начальное состояние.
```
Вызов useState возвращает 2 значения: первое значение - текущее состояние, а второе - функция, обновляющая это состояние.

React будет хранить это состояние между рендерами и передавать его функции useState. Если нужно будет изменить count, мы вызовем setCount.

## useEffect 

Даёт возможность выполнять побочные (side-effect) эффекты в функциональном компоненте. Побочными эффектами в React-компонентах могут быть: загрузка данных, оформление подписки и изменение DOM вручную. Он выполняет ту же роль, что и componentDidMount, componentDidUpdate и componentWillUnmount в React-классах, объединив их в единый API.
