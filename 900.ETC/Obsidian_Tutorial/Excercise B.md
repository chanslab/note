# Mermaid

**Mermaid**는 텍스트 기반으로 다이어그램과 차트를 그릴 수 있게 해주는 오픈소스 JavaScript 도구입니다. 복잡한 그래픽 툴 없이 **Markdown**과 유사한 단순한 텍스트 문법만으로 순서도, 시퀀스 다이어그램, 간트 차트 등을 쉽고 빠르게 생성할 수 있다는 것이 큰 장점입니다. ^mermaid-concept

---

## 1. 기본 구조 및 방향 설정

모든 Mermaid 코드는 상단에 어떤 종류의 다이어그램인지를 선언하며 시작합니다.

### 차트 방향 (Flowchart 기준)

- **TB / TD**: 위에서 아래로 (Top to Bottom / Top Down)
    
- **BT**: 아래에서 위로 (Bottom to Top)
    
- **LR**: 왼쪽에서 오른쪽으로 (Left to Right)
    
- **RL**: 오른쪽에서 왼쪽으로 (Right to Left)
    

---

## 2. 주요 다이어그램 문법

### 1) 순서도 (Flowchart)

가장 많이 쓰이는 형태입니다. 노드(박스)의 모양은 괄호의 종류에 따라 결정됩니다.

코드 스니펫

```
graph TD
    A[사각형 노드] --> B(라운드 노드)
    B --> C{조건문/다이아몬드}
    C -- Yes --> D((원형 노드))
    C -- No --> E[/평행사변형/]
```

- `[ ]`: 직사각형 (기본)
    
- `( )`: 모서리가 둥근 사각형
    
- `{ }`: 마름모 (결정/조건)
    
- `(( ))`: 원형
    
- `-->`: 화살표 실선
    
- `-.->`: 화살표 점선
    
- `==>`: 굵은 화살표 실선
    

---

### 2) 시퀀스 다이어그램 (Sequence Diagram)

객체 간의 상호작용과 시간 순서를 표현할 때 유용합니다.

코드 스니펫

```
sequenceDiagram
    참여자A->>참여자B: 요청 메시지
    참여자B-->>참여자A: 응답 메시지
    Note over 참여자A, 참여자B: 중간 설명 메모
```

- `->>` : 실선 화살표
    
- `-->>` : 점선 화살표
    
- `activate` / `deactivate` : 활성화 상태 표시
    

---

### 3) 간트 차트 (Gantt Chart)

프로젝트 일정 관리 시 사용합니다.

코드 스니펫

```
gantt
    title 프로젝트 일정표
    dateFormat  YYYY-MM-DD
    section 설계 단계
    기획하기 :a1, 2026-04-18, 5d
    설계하기 :after a1, 7d
    section 개발 단계
    코딩하기 :2026-04-30, 10d
```

---

### 4) 개체-관계 다이어그램 (ER Diagram)

데이터베이스 구조를 표현할 때 사용합니다.

코드 스니펫

```
erDiagram
    USER ||--o{ ORDER : places
    USER {
        string username
        string email
    }
    ORDER {
        int orderNumber
        string price
    }
```

---

## 3. 스타일 커스터마이징

특정 노드에 색상을 입히거나 선 스타일을 바꿀 수 있습니다.

- **방법**: `style [노드ID] fill:[색상],stroke:[색상],stroke-width:[두께]px`
    
- **예시**: `style A fill:#f9f,stroke:#333,stroke-width:4px`
    

---

## 4. Mermaid 사용 팁

- **Live Editor**: 설치 없이 웹 브라우저에서 바로 작성해보고 싶다면 [Mermaid Live Editor](https://mermaid.live/)를 추천합니다.
    
- **Markdown 적용**: Markdown 문서 내에서 사용할 때는 코드 블록 시작 부분에 언어 이름으로 `mermaid`를 적어주면 됩니다.
    

> **작성 예시**
> 
> ```mermaid
> 
> graph LR
> 
> Start --> Stop
> 
> ```

---

# 주석

인라인 주석 %%주석 내용%% 입니다

블록 주석

%%
이 부분은 블록 주석 입니다. 
%%

> [!note] 주석
읽기 모드에서는 보이지 않습니다.

---
