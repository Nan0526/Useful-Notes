# 学习笔记
汇总一下经常用的的commands，省了每次都去stack overflow了

| # | 笔记 | Description |
| ---- | -------------- | ----------------- |
| | **Git，github 等等** | |
| 1 | [在readme里面添加图片](./notes/addImg.md)|不仅仅是readme，是所有.md文件 |
| 2 | [Locally && Remotely更改 commits history](./notes/editCommit.md)| 1. 删除已经push的commits 2.删除没有push的commits（TODO）|
| 3 | [git pull/git fecth](./notes/pull.md)| `git pull` is shorthand for `git fetch` followed by `git merge FETCH_HEAD`|
| 4 | [Ignore files that have already be pushed](./notes/ignoreFile.md)|对于没有tracked/committed/pushed files, 我们只需要在.gitignore 里面添加就好了。但是对于已经tracked files, 应该怎么做呢？|
| 5 | [Git撤销操作](./notes/gitCheckOutFile.md) |撤销 unstaged/staged/commited/pushed changes|
| 6 | [Git Branches遇到各种senario](./notes/gitBranch.md) |1. 在一个branch里新建的file也出现在了其他branch|
| 7 | [Phabricator Stacked Diff Workflow](./notes/Stacked_Diffs.md) |Create stacked diffs|
| 8 | [Change upstream](./notes/changeUpstream.md)| Change upstream, rebase child branch to master|
| 9 | [把local连接到github和heroku](./notes/heroku.md)| 创建remotes, 链接remotes|
| 10 | [一些有用的命令](./notes/commands.md)|1. 在bash，查看和set environment variables|
| 11 | [Set alias](./notes/alias.md)| 1.设置alias,如 `gst` |
| 12 | [arc 命令](./notes/arc.md)|1. update 一个revision 2. land 一个revison |
| | **Python, framework, 以及相关数据库** | |
| 1 | [Connect Postgres server to Flask](./notes/postgres.md)| 在Flask里面使用PostgresSQL  |
| 2 | [Flask db](./notes/db.md)| 1.Flask db migration相关命令 <br> 2.一些常用commands的使用和理解 <br> 3. Entity Relationship| 
| 3 | [PYTHONPATH](./notes/import.md) | 梳理一下import路径问题 |
| 4 | [Postgres Commands](./notes/postgress_commands.md)| 常见postgres commands|
| 5 | [Heroku Setup](./notes/herokuapp.md)| 1. 常见的heroku commands <br> 2.Heroku app setup step by step|
| 6 | [Python Unit Tests](./notes/unittests.md) |1. `mock.ANY`就可以实现类似于 `assert_called_with_partion_args`这样的功能 |
| | **Frontend** | |
| 1 | [Template inheritance](./notes/templates.md)| flask html里面的`block`, `extend`, `super`.. 等代表什么呢？|
| 2 | [Bootstrap](./notes/bootstrap.md) | 1. 如何导入bootstrap? |
| 3 | [Images](./notes/images.md) | 1. 前端如何serve pictures？|
| 4 | [Class vs ID](./notes/class_and_id.md) | HTML中 class和ID 区别|
| 5 | [jQuery](./notes/jquery.md)| 1.DOM Traversal and Manipulation <br> 2.Event Handling <br> 3.Ajax |
| 6 | [Bind](./notes/react.md)| 1. this指向 2. bind()函数 |
| 7 | [Next JS](./notes/nextjs.md)|1. Pages 2. Routing 3. `next/router` 主要是了解dynamic routing | 
| 8 | [Hook](./notes/hook.md)|1. 经常看到的`useState` 2. `useSelector` 3. `useDispatch` 4. `useMemo`|
| 9 | [Graphql Schema](./notes/graphql.md)|1. Object Types 2. The `Query` type 3. The `Mutation` type |
| 10 | [Graphql - Connect to data source](./notes/datasource.md)|1. 通过REST API 2. 通过Database |
| 11 | [Graphql - Query Resolvers](./notes/resolver.md)|1. 理解！是一个function, 对应的key 是object/query type里面的一个field|
| 12 | [Graphql - Client Side](./notes/graphql_client.md)|1. 理解 server, client 2. useQuery, useMutation hook 3. Fragment|
| 13 | [Graphql - Code Gen](./notes/codegen.md)| To generate TypeScript types for your queries and mutations |
| 14 | [Redux](./notes/redux.md)|1. Redux Store 2. Reducer functions 3. Dispatch functions|
| 15 | [Typescript - Interface vs Type](./notes/interface.md)|1. Interfaces are restricted to an object type 2. You can merge interfaces but not types|
| 16 | [Javascript 零散知识点](./notes/javascript.md)|1. class 里的get method 2. static method |
| | **React** | |
| 1 | [React - Component](./notes/component.md) |1. `React.Componenet` 有两种 function / class 2. Props & State 3. Life cycle|
| 2 | [Promise](./notes/promise.md)| 感觉是把一个async function包装成 sync-like|
| 3 | [Fundamentals](./notes/fundamentals.md) | 一些基础知识: functional/class component; props/state|
| 4 | [Event](./notes/event.md)|1. Event handling 2.Binding Event Handlers |
| 5 | [Flow](./notes/flow.md)|1. types(primary types, function types...)|
| 6 | [Conditional Rendering](./notes/crendering.md)|1. if/else 2.Element variables 3.Ternary conditional operator 4.Short circuit operator |
| 7 | [List Rendering](./notes/listrendering.md)|1. `map()` method, 注意传入的是method! 2. Lists and Keys|
| 8 | [Styling and CSS basics](./notes/reactcss.md)|1. 使用CSS file 2. Inline Styling 3. CSS module |
| 9 | [Basics of Form Handling](./notes/formhandling.md)|主要的那三步骤，还有需要记住的event handlers|
| 10 | [Lifecycle](./notes/lifecycle.md)|1.Lifecycle Methods 2.Mounting Lifecycle Methods 3.Updating Lifecycle mthods |
| 11 | [Fragments](./notes/fragments.md)|很好理解，React Fragments grouped the child elements without adding extra node to DOM|
| 12 | [PureComponent](./notes/purecomponent.md)|只有在prevState和prevProps改变的时候才会re-render |
| 13 | [Memo](./notes/memo.md)|是function component里的PureComponent. (PureComponent只存在于class component里面）|
| 14 | [Refs](./notes/refs.md)| 运用ref，可以直接access到DOM tree的某一个Node|
| 15 | [Higher order components](./notes/hoc.md)|高阶组件(HOC) takes one component and returns another component|
| xx| [Context](./notes/context.md)| |
| | **React Hooks** | |
| 1 |[基本概念](./notes/hooksintro.md)| Why hooks?|
| 2 |[useState](./notes/useState.md)|注意useState with Object和useState with array的特殊处理 |
| 3 |[useEffect](./notes/useEffect.md)|1. 跟side effects相关 2. useEffect在每次render的时候都会被fire! |
| 4 |[useContext]| |
| 5 |[useReducer](./notes/useReducer.md)|1.是用来state management |
| 6 |[useCallback](./notes/useCallback.md)|1. 啥时候用：passing callback functions to child components的时候 <br> 2.作用是memorize 那些functions，不用每次render的时候都重新生成新的 |
| 7 |[useMemo](./notes/useMemo.md)||
|xx |[Hooks Highlevel 理解](./notes/hookshigh.md)|1. 每个Hook名字之后的含义 2.useEffect, useCallback, useMemo三者有何区别？|
| | **React Redux** | |
| 1 | [基本概念](./notes/reduxintro.md)|1. Three core concepts 2. Three principles - store, action 和 reducer|
| 2 | [Actions](./notes/action.md)|Actions: plain JS objects with a `type` property |
| 3 | [Reducers](./notes/reducer.md)|本质是一个function! input:`(prevSate, action)`. output: `nextState` |
| | **Graphql** | |
| 1 | [基本概念](./notes/apollobasic.md)| 快速setup: 1. schema 2. backend server 3. client |
| 2 | [resolvers](./notes/resolvers.md)| 1. 一个graphql query的journey 2. resolver怎么写，是什么 |
| 3 | [mutations](./notes/mutations.md)| 1. 什么是mutation 2. resolve a mutation 3. `useMutation` hook|
| | **Frontend Testing** | |
| 1 | [ShallowWrapper Debug](./notes/shallowwrapperdebug.md)| Test的时候想知道wrapper里面是什么东西 |
| | **Clean Code**| |
| 1 | 导语 | 略过 |
| 2 | [Meaningful names](./notes/meaningful_names.md)|1. name要尽量clear，避免歧义 <br> 2.class最好是名词，method最好是动词 |
| 3 | [Functions](./notes/functions.md)|1. Do one thing. 2. Same level of abstractions 3. Dry 4.arguments |
| 4 | [Comments](./notes/comments.md)|1.Don’t Use a Comment When You Can Use a Function or a Variable <br> 2. Some comments are necessary or beneficial. |
| | **Computer Networds**| |
| 1 | [Packet Switching](./notes/packet_switching.md)|1. 简单介绍 |
| 2 | [IP](./notes/ip.md)|1. IP是什么 |
| | **Docker** | |
| 1 | [Dockerfile](./notes/dockerfile.md)| 1. create dockerfile | 
| 2 | [Makefile](./notes/makefile.md)| 1. `.PHONY` 是什么 |
| 3 | [Docker compose file](./notes/docker_compose.md)| 0. docker compose 是用来compose multiple container的！<br> 1. `docker-compose run` <br> 2. `docker-compose build` |
| 4 | [Run a bash](./notes/docker_bash.md)|1. Use a container ID 2. Use an image ID |
| | **Linux Commands**| |
| 1 | [Cat](./notes/cat.md)| cat vs vim, cat是如何读写files的|
| | **Open Policy Agent** | |
| 1 | [OPA](./notes/opa.md) | 简单介绍OPA 基本概念，1. OPA 怎么用 2. Rego 3. Running OPA|
| 2 | [Rego](./notes/rego.md) | Policy Language |
| | **Cyber Security** | |
| 1 | [Security Goals](./notes/security_goals.md)| Security Goals |
| | **Other Notes** | |
| 1 | [MySQL show status](./notes/show_status.md)|How to show open database connections |
| 2 | [Gevent](./notes/gevent.md)|1.gevent.threadpool 2. gevent.pool.Pool |
| 3 | [Get an object's attributes](./notes/dir.md)|1. use `dir()`|
