## 230310 React Router

KDT-React-Tutorial 프로젝트의 sixthapp 참조.

### React Router 기본

- `<BrowserRouter></BrowserRouter>` : 컴포넌트가 react-router를 사용할 수 있도록 처리

- `<Routes></Routes>` : 주소 변경을 감지하고, 일치하는 Route를 찾아서 표시해주는 역할

- `<Route>` : 컴포넌트와 주소를 연결 시켜놓기 위한 태그.

- `<Link></Link>` : react-router에서 페이지 링킹은 a태그가 아니라 Link 태그를 사용. + state를 전달할 수 있다.

- `<Route></Route>` : NestedRoute(버전 6부터 권장)

  - 공통적으로 렌더링하고 싶은 컴포넌트가 있을 때 효과적. + url의 계층적 구조를 알기 쉬운 장점도 있다.
  - 상위 컴포넌트를 통해 하위 컴포넌트를 렌더링하므로 상위 컴포넌트에 `<Outlet />`을 포함시켜줘야 하위 컴포넌트를 렌더링할 수 있다.

- `useParams()` : path parameter값을 받아올 수 있는 훅

- 경로 명시할 때 주의사항 : 절대경로와 상대경로... 상대경로로 작성하면, 현재 나의 위치에 명시한 path가 덧붙혀짐에 주의한다.

- `useOutletContext` : Outlet 태그를 통해 하위 컴포넌트를 마운트시킬 때, context라는 속성으로 하위 컴포넌트에게 데이터를 전달할 수 있으며, 이렇게 전달된 데이터는 하위 컴포넌트에서 useOutletContext 훅을 통해 받을 수 있다.

- `index Route`: NestedRoute 내부에서 기본 경로에 대해 렌더링할 컴포넌트를 지정할 때 사용된다.
  ```jsx
  <Route path="posts" element={<PostLayout />}>
    <Route index element={<Posts />} />
    <Route path=":postId" element={<PostDetail />} />
  </Route>
  ```

### React Router 활용

- `useSearchParams` : 쿼리파라미터를 다룰 수 있게 해주는 훅
- `useLocation`: 현재 location에 대한 값들을 담은 객체를 받아 사용할 수 있게 하는 훅
  - 여기서 보통 state를 다루게 되는데, 이 state는 Link 태그에 전달된 state props에 담겨있는 데이터이다. 즉, 페이지를 이동하면서 전달되는 data를 이용하고자 할 때 사용된다.
- `useNavigate`: 주소 이동을 위한 훅. Link 태그와 다르게, 함수 내부에서 주소 이동을 실행할 때 사용된다.
  - const navigate = useNavigate() 로 초기화한 후 , navigate()를 호출한다. 첫번째 인자로 이동할 경로, 두번째 인자로 옵션을 제공. replace, state
  - replace로 페이지 이력을 현재 페이지와 교체한다. state로 다음 페이지에 data를 전달하고, useLocation으로 데이터를 받는다.
  - 경로 인자에 숫자를 제공할 수 있다. 현재 히스토리 스택을 기준으로 페이지를 이동한다.

### React Router 부가기능

- `NavLink` : 기본적으로 가지고 있는 isActive props를 활용하여 현재 접속한 Nav가 어디인지 표시하는 과정을 돕는다.
- `CustomNavLink` : 링크를 타고 페이지를 이동했을 때에도 queryParams를 주소창에 유지하고 싶을 때 사용
