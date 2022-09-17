# Hello Coder..!! New Article is Here..!!

![css](img%201.jpg)

## **CSS SELECTORS**


>_In **CSS,** selectors are used to target the **HTML** elements on our web pages that we want to style. There are a wide variety of CSS selectors available, allowing for fine-grained precision when selecting elements to style. In this article and its sub-articles we'll run through the different types in great detail, seeing how they work._

## **Table of Contant :** 

**[1. What is Selectors.](##heading--1)**

**[2. Selector lists](##heading--2)**

**[3. Types of selectors](##heading--3)**

- **[ Type, class, and ID selectors](##heading--3-1)**
- **[Attribute selectors](##heading--3-2)** 

- **[Pseudo-classes and pseudo-elements](##heading--3-3)**

- **[Combinators](##heading--3-4)**

**[4. Summary](##heading--4)**

***
# **what is a selector ?**
***

![selectors](img%202.png)

You have met selectors already. A CSS selector is the first part of a CSS Rule. It is a pattern of elements and other terms that tell the browser which HTML elements should be selected to have the CSS property values inside the rule applied to them. The element or elements which are selected by the selector are referred to as the subject of the selector.

```
h1{
    color: blue;
    background-color: yellow;
}

p{
    color: red;
}
```

In earlier articles you met some different selectors, and learned that there are selectors that target the document in different ways — for example by selecting an element such as **h1,** or a **class** such as **.special.**

In CSS, selectors are defined in the CSS Selectors specification; like any other part of CSS they need to have support in browsers for them to work. The majority of selectors that you will come across are defined in the Level 3 Selectors specification, which is a mature specification, therefore you will find excellent browser support for these selectors.

***
## **Selector lists**
***
If you have more than one thing which uses the same CSS then the individual selectors can be combined into a selector list so that the rule is applied to all of the individual selectors. For example, if I have the same CSS for an **h1** and also a **class** of **.special**, I could write this as two separate rules.

```
h1 {
    color: blue;
}

.special {
    color: blue;
}
```

I could also combine these into a selector list, by adding a comma between them.

```
h1,
.special {
    color: blue;
}
```

White space is valid before or after the comma. You may also find the selectors more readable if each is on a new line.

```
h1,
.special {
    color: blue;
}
```

In the live example below try combining the two selectors which have identical declarations. The visual display should be the same after combining them.

## **Interactive editor**
```
<h1>Type selectors</h1>
<p>Veggies es bonus vobis, proinde vos postulo essum magis <span>kohlrabi welsh onion</span> daikon amaranth tatsoi tomatillo
    melon azuki bean garlic.</p>

<p>Gumbo beet greens corn soko <strong>endive</strong> gumbo gourd. Parsley shallot courgette tatsoi pea sprouts fava bean collard
    greens dandelion okra wakame tomato. Dandelion cucumber earthnut pea peanut soko zucchini.</p>

<p>Turnip greens yarrow ricebean rutabaga <em>endive cauliflower</em> sea lettuce kohlrabi amaranth water spinach avocado
    daikon napa cabbage asparagus winter purslane kale. Celery potato scallion desert raisin horseradish spinach
</p>
```

```    
span {
    background-color: yellow;
}

strong {
    color: rebeccapurple;
}

em {
    color: rebeccapurple;
}
```

><h1>Type selectors</h1>
><p>Veggies es bonus vobis, proinde vos postulo essum magis <span>kohlrabi welsh onion</span> daikon amaranth tatsoi tomatillomelon azuki bean garlic.</p>

><p>Gumbo beet greens corn soko <strong>endive</strong> gumbo gourd. Parsley shallot courgette tatsoi pea sprouts fava bean collardgreens dandelion okra wakame tomato. Dandelion cucumber earthnut pea peanut soko zucchini.</p>

><p>Turnip greens yarrow ricebean rutabaga <em>endive cauliflower</em> sea lettuce kohlrabi amaranth water spinach avocadodaikon napa cabbage asparagus winter purslane kale. Celery potato scallion desert raisin horseradish spinach
</p>


When you group selectors in this way, if any selector is syntactically invalid, the whole rule will be ignored.

In the following example, the invalid class selector rule will be ignored, whereas the h1 would still be styled.

```
h1 {
  color: blue;
}

..special {
  color: blue;
}
```

When combined however, neither the **h1** nor the class will be styled as the entire rule is deemed invalid.

```
h1,
.special {
  color: blue;
}
```

***
## **Types of selectors**
***

There are a few different groupings of selectors, and knowing which type of selector you might need will help you to find the right tool for the job. In this article's subarticles we will look at the different groups of selectors in more detail.

- ### **Type, class, and ID selectors**

### Type selectors

>A type selector is sometimes referred to as a tag name selector or element selector because it selects an HTML tag/element in your document. In the example below, we have used the **span, em and strong** selectors.

This group includes selectors that target an HTML element such as an **h1**

```
h1 {
}
```

### Class selectors

>The class selector starts with a dot **(.)** character. It will select everything in the document with that class applied to it. In the live example below we have created a class called highlight, and have applied it to several places in my document. All of the elements that have the class applied are highlighted.

It also includes selectors which target a class:
```
.box {
}
```

### ID selectors

>An ID selector begins with a **#** rather than a dot character, but is used in the same way as a class selector. However, an **ID** can be used only once per page, and elements can only have a single id value applied to them. It can select an element that has the id set on it, and you can precede the ID with a type selector to only target the element if both the element and ID match. You can see both of these uses in the following example:

or, an ID:

```
#unique {
}
```

- ### **Attribute selectors**
>This group of selectors gives you different ways to select elements based on the presence of a certain attribute on an element:

```
a[title] {
}
```
>Or even make a selection based on the presence of an attribute with a particular value:

```
a[href="https://example.com"]
{
}
```

- ### **Pseudo-classes and pseudo-elements**
>This group of selectors includes pseudo-classes, which style certain states of an element. The **:hover** pseudo-class for example selects an element only when it is being hovered over by the mouse pointer:

```
a:hover {
}
```

>It also includes pseudo-elements, which select a certain part of an element rather than the element itself. For example, **::first-line** always selects the first line of text inside an element

```
p::first-line {
}
```

- ### **Combinators**

>The final group of selectors combine other selectors in order to target elements within our documents. The following, for example, selects paragraphs that are direct children of **article** elements using the child combinator (>):

```
article > p {
}
```

***
## **Summary**
***
In this article we've introduced CSS selectors, which enable you to target particular HTML elements.

## Thanks for Reading.