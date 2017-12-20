---
layout: post
title: Top picks from React Day conference
image: /images/posts/2017-12-react-day-audience.jpg
description: The main highlights of React.day conference, which took place in Berlin on December 2, 2017.
---

The ecosystem around React itself is quite stabilized, there are no such turbulent shifts as in recent years, *declarativeness* rules the code and GraphQL is the real game changer. These are some highlights that would summarize [React.day conference](http://reactday.berlin/), which took place in Berlin on December 2, 2017.

![React.day audience](/images/posts/2017-12-react-day-audience.jpg)

#### It's all about human

React developer stack has matured and conference talks adhered to it. In spite of tough discussions how to properly call APIs, you eventually end up with some sort react-redux-webpack combination. As the javascript world progressed through the years with more advanced tooling and libraries, we're no longer in need to solve trivial issues. Instead, our focus has shifted on more abstract level, closer to the user.

This thought was demonstrated by several speakers during the day, most obviously by [Kristin Baumann's](https://twitter.com/kristin_baumann) *Designing with React*. Kristin did a great job showing us how React Sketch.app can be leveraged in design, bringing real data into the process. AirBnB, company behind the tool, recently open sourced initial version of [Lona](https://github.com/airbnb/Lona), trying to go further and make it possible to generate cross-platform code & Sketch files at once. Interesting things may happen, so it's definitely worth checking out. 

#### WTFM - write the fantastic manual

The users, developers specifically, played the big role also in the lightning talk *Humanizing your documentation* by [Carolyn Stransky](https://twitter.com/carolstran). She pointed out one recurring mistake we often perpetrate. Let's take a look on docs for Redux and then React Native, how do they differ? Moreover, how do they *feel*? If you ever worked with both, I bet you perceived Redux Docs much better. That's because it does not only describe API, but also contains philosophy behind and particular use cases. Carolyn precisely explains why - we postpone writing docs for later, although we should start in the beginnings when use cases are being discussed. So let's keep this in mind next time we develop something.

#### Peculiar story of Storybook

[Norbert de Langen](https://twitter.com/norbertdelangen) is the core maintainer of Storybook and in his presentation *Building Storybook* he introduced us into backstage where a couple of diverse people placed around the globe put their free time to deliver tool used by many companies. It's always interesting to learn how little lies in front of you to become open source contributor. Norbert just walked around when Kadira company, original maintainer, went bankrupt in May, gained full rights on repository overnight and established Storybook organization.
 
If you take documentation seriously, have a look on Storybook, start using it early - when first use cases & React components are created. [@storybook/addon-jest](https://www.npmjs.com/package/@storybook/addon-jest), fresh new addon may help you on your way.

#### GraphQL: the game changer

> "Delete your twitter account to avoid hype."
> <div style="text-align: right">Kristijan Ristovski</div>

One of the most influential highlights of the day was definitely *React state management in a GraphQL era* by Kristijan Ristovski a.k.a [Kitze](https://twitter.com/thekitze). Kristijan proved to have deep knowledge of how to manage state in applications as a consultant on various projects and with high certainty can tell the difference between useful library and hype. Here are a few points we had to learn a hard way Kristijan mentioned:

- **Thread each route as a miniapp** - everybody is talking about microservices on backend, but we often magically forget it when we switch to browser environment. You simply don't need to difficulty set your routes. Instead, create small app for each route and let the page refresh when navigating. It's not wrong at all.
- Think about your target users (see, again!). Some people live in tunnels, in that case look for [redux-offline](https://www.npmjs.com/package/redux-offline), but if all your potential customers are from NY, surfing on newest iPhone model, then it's likely useless.
- **Say yes to GraphQL** - reasoning why you should care would deserve an article itself. It's the most significant step in the development in the last years, which among other things enables you to avoid making accidental breaking changes in API & writing the same repetitive *"prepare data payload, fetch, handle, dispatch"* code all over again.
- There is no strict *yes* or *no* whether you need redux along your GraphQL stack. If you feel inclined to not include redux, Apollo recently released [apollo-link-state](https://www.npmjs.com/package/apollo-link-state) to manage state in GraphQL style.

And because we actively use & love GraphQL at Kiwi.com, we couldn't resist and already implemented a simple mobile app, taking Apollo local state to its advantage. Checkout the snack below or the code on Github: [https://github.com/jaroslav-kubicek/apollo-local-state-example](https://github.com/jaroslav-kubicek/apollo-local-state-example)

<div data-snack-id="@kubajz/graphql-todo-list" data-snack-platform="ios" data-snack-preview="true" data-snack-theme="light" style="overflow:hidden;background:#fafafa;border:1px solid rgba(0,0,0,.16);border-radius:4px;height:505px;width:100%"></div>
<script async src="https://snack.expo.io/embed.js"></script>