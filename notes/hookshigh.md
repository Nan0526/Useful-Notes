# Hooks Highlevel 理解
useState - state有关    
useEffect - side effects 相关   
useContext - context API 相关
useReducer - reducers相关

# useEffect, useCallback, useMemo三者有何区别？
技术文章： https://segmentfault.com/a/1190000039657107    
中心思想： 多用useCallback和useMemo是好习惯，如果该函数或变量作为 props 传给子组件，请一定要用，避免子组件的非必要渲染
