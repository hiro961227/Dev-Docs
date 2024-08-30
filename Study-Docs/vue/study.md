## v-bind ( ```:```, ```.``` ```.prop``` )
> 하나 이상의 속성 또는 컴포넌트 prop을 표현식에 동적으로 바인딩됨, 인자가 있는 ```any``` 인자가 없는 ```Object``` 값이 요구됨

```vue
    <!-- 속성 바인딩 -->
    <img v-bind:src="imageSrc" />
    <!-- 동적인 속성명 -->
    <button v-bind:[key]="value"></button>
    <!-- 단축 문법 -->
    <img :src="imageSrc" />
    <!-- 인라인으로 문자열 결합 -->
    <img :src="'/path/to/images/' + fileName" />
    <!-- class 바인딩 -->
    <div :class="{ red: isRed }"></div>
    <div :class="[classA, classB]"></div>
    <div :class="[classA, { classB: isB, classC: isC }]"></div>

    <!-- style 바인딩 -->
    <div :style="{ fontSize: size + 'px' }"></div>
    <div :style="[styleObjectA, styleObjectB]"></div>

    <!-- 속성을 객체로 바인딩 -->
    <div v-bind="{ id: someProp, 'other-attr': otherProp }"></div>
```

***


## v-model
> 사용자 입력을 받는 폼(form) 엘리먼트 또는 컴포넌트에 양방향 바인딩을 만듦

1. 제한된 사용: ```input``` ```select``` ```textarea```


***


## v-slot
> ```이름이 있는 슬롯``` 또는 ```props를 받을 것으로 예상되는 범위형(Scoped) 슬롯```

1. 제한된 사용: ```template``` ```컴포넌트```(props를 수신할 기본 슬롯만 있는 경우)

```vue
<!-- 이름이 있는 슬롯 -->
<BaseLayout>
  <template v-slot:header>
    해더 컨텐츠
  </template>

  <template v-slot:default>
    기본 슬롯 컨텐츠
  </template>

  <template v-slot:footer>
    푸터 컨텐츠
  </template>
</BaseLayout>

<!-- props를 수신할 기본 슬롯 -->
<InfiniteScroll>
  <template v-slot:item="slotProps">
    <div class="item">
      {{ slotProps.item.text }}
    </div>
  </template>
</InfiniteScroll>

<!-- props를 수신할 기본 슬롯, 분해할당을 사용 -->
<Mouse v-slot="{ x, y }">
  마우스 위치: {{ x }}, {{ y }}
</Mouse>
```

***


## ref
> **상태 관리** | 단일 원시 값(primitive value) 또는 객체를 **반응형으로 만들 때** 사용, 원시 값(숫자, 문자열, boolean 등)에 이용됨

1. 단일 값에 적합 - **원시 값**이나 **단일 객체**를 반응형으로 만들 때 유용
2. ```.value``` 접근: ref로 생성된 반응형 변수는 .value를 통해 접근하고 수정 가능
3. 자동 언래핑: ref가 템플릿에서 사용될 때는 .value를 명시적으로 사용하지 않아도 됨, 객체 내부까지 추적하지 않음

```vue
<script setup>
import { ref } from 'vue';

const count = ref(0);

const increment = () => {
  count.value++;  // ref 사용 시 .value를 통해 값에 접근합니다.
};
</script>
```

***



## reactive 
> **상태 관리** | 객체를 **반응형으로 변환**하는 데 사용
> *객체 내부의 모든 속성을 추적하여 반응형으로 만들어 줌*

1. 객체에 적합 - **여러 속성**을 가진 객체를 반응형으로 만들 때 유용
2. **속성에 직접 접근** - .value 없이 접근 가능
3. 깊은 반응성: **객체 내부의 모든 속성과 중첩된 객체**까지도 자동으로 반응형으로 변환

```vue
<script setup>
import { reactive } from 'vue';

const state = reactive({
  count: 0,
  message: 'Hello, Vue!'
});

const increment = () => {
  state.count++;  // .value 없이 객체 속성에 직접 접근
};
</script>
```


***



## props (소품)
> 부모 -> 자식 데이터 전달 [하향식 단방향 바인딩] | 자식 component가 실수로 데이터를 변경해 부모 component의 상태를 변경하는 것을 방지 <br>
> 부모 컴포넌트가 업데이트될 때마다 자식 컴포넌트의 모든 props가 최신 값으로 업데이트 <br>
> ```prop```는 **상위 컴포넌트의 정보를 전달**하기위한 사용자 지정 특성

1. 하위 컴포넌트의 템플릿에서 상위 데이터를 직접 참조X

```vue
<!-- script setup -->
defineProps({
    btnType: {
        type: String,
        required: true
    }
});
<!-- script -->
export default {
  props: {
        btnType: {
            type: String,
            required: true
        }
    }
}

<!-- 변수 값을 동적으로 할당도 가능 -->
export default {
  data() {
    return {
      post: {
        id: 1,
        title: 'Vue와 함께하는 나의 여정'
      }
    }
  }
}
<BlogPost v-bind="post" /> === <BlogPost :id="post.id" :title="post.title" />
```
2. 실행 간 타입 체크
    ```type```: String, Number, Boolean, Array, Object, Date, Function, Symbol
3. ```v-bind``` ( ```:``` )를 사용하여 동적으로 할당할 수 있음
    ```vue
    <!-- prop 바인딩. "prop"은 자식 컴포넌트에서 선언되어 있어야 함 -->
    <MyComponent :prop="someThing" />
    <!-- 자식 컴포넌트와 공유될 부모 props를 전달 -->
    <MyComponent v-bind="$props" />
    ```

***



## emit (방출)
> 자식 -> 부모 데이터 전달 | 부모component가 업데이트될 때마다 자식componennt의 props는 최신 값으로 새로고침 <br>
> 컴포넌트에서 내보낼 커스텀 이벤트를 선언(```문자열 배열```의 간단한 형태 | ```key:prop name```, ```value: null``` or ```value: function``` 형식의 객체 형태)

1. 종류
    ```vue
    interface ComponentOptions {
        emits?: ArrayEmitsOptions | ObjectEmitsOptions
     }

     type ArrayEmitsOptions = string[]

     type ObjectEmitsOptions = { [key: string]: EmitValidator | null }

     type EmitValidator = (...args: unknown[]) => boolean
    ```
2. **유효성 검사 함수**: 컴포넌트의 $emit 호출에 전달된 인자를 수신 (인자의 유효성을 불리언값으로 반환해야 함)
    ex. this.$emit('foo', 1)이 호출되면, foo에 해당하는 유효성 검사기는 인자 1을 받음
3. 기본 DOM 이벤트 리스너가 아닌 컴포넌트 이벤트 리스너로 간주되는 이벤트 리스너에 영향, 컴포넌트의 $attrs 객체에서 제거되므로, 컴포넌트의 루트 엘리먼트로 전달되지 않음
 ```vue 
<!-- script setup -->
const emit = defineEmits(['trigger-modal']);
const handleClick = () => {
    emit('trigger-modal', layerType);
};

<!-- script -->
<!-- 배열 문법 -->
export default {
  emits: ['check'],
  created() {
    this.$emit('check')
  }
}
<!-- 객체 문법 -->
export default {
  emits: {
    // 유효성 검사 없음
    click: null,

    // 유효성 검사 사용
    submit: (payload) => {
      if (payload.email && payload.password) {
        return true
      } else {
        console.warn(`잘못된 정보 제출 이벤트!`)
        return false
      }
    }
  }
}
 ```
 4. vue API인 ```defineEmits```는 **컴포넌트 초기화 시점에 호출하여 emit 함수를 정의**하는 용도로, *이벤트를 정의하는 것이지 이벤트를 발생시키는 함수가 아님*


***


## setup
> 반응형 데이터를 만들고, 라이프 사이클을 제어
1. 빌드 과정 없이 컴포지션 API 사용 / 옵션 API 컴포넌트에서 컴포지션 API 기반 코드와 통합 시 컴포넌트에서 컴포지션 API 사용을 위한 진입점 역할
2. 객체를 반환하여 템플릿에 노출할 수 있습니다. 반환된 객체의 속성은 컴포넌트 인스턴스에서 사용할 수 있습니다
3. setup에서 반환된 refs는 템플릿에서 접근할 때, 자동으로 얕은 언래핑되므로, 접근할 때 .value를 사용할 필요가 없습니다
4. 객체를 동기적으로 반환
5. **setup 함수의 첫 번째 인자는 props , 두 번째 인자는 Setup Context 객체**
6. **setup 함수 내부의 props는 반응형**이며, **새 props가 전달되면 업데이트**됨
7. *props 객체를 분해할 경우, 분해 된 변수는 반응성을 잃게 됩니다*. 따라서 항상 ```props.xxx```처럼 접근
    ```vue
    export default {
        props: {
            title: String
        },
        setup(props) {
            console.log(props.title)
        }
     }
    ```
8. *Props를 분해해야 하거나, 반응성을 유지하면서 외부 함수에 props를 전달해야 하는 경우*
    ```vue
    import { toRefs, toRef } from 'vue'

    export default {
        setup(props) {
            // refs 객체로 `props`를 변환한 후, 분해 할당
            const { title } = toRefs(props)
            // `title`은 `props.title`을 추적하는 ref 입니다.
            console.log(title.value)

            // 또는, 하나의 `props` 속성만 ref로 변환할 수 있습니다.
            const title = toRef(props, 'title')
        }
    }
    ```
9. *컨텍스트 객체는 setup 내부에서 유용할 수 있는 다른 값을 노출*
    ```vue
    export default {
        setup(props, context) {
            // 속성 (비-반응형 객체, $attrs에 해당함)
            console.log(context.attrs)

            // 슬롯 (비-반응형 객체, $slots에 해당함)
            console.log(context.slots)

            // 이벤트 발송 (함수, $emit에 해당함)
            console.log(context.emit)

            // 로컬 속성 노출 (함수)
            console.log(context.expose)
        }
    }
    ```
10. **컨텍스트 객체는 반응형이 아니며**, 안전하게 분해 할당
    ```vue
    export default {
        setup(props, { attrs, slots, emit, expose }) {
            ...
        }
    }
    ```
    * ```attrs``` ```slots``` 컴포넌트가 업데이트 될 때 항상 업데이트되는 스테이트폴(stateful)객체, 구조 분해하지 않고 ```attrs.x```, ```slots.x```처럼 속성 참고해야 됨
    * **반응형X**, attrs 또는 slots의 변경 사항을 기반으로 하는 사이드 이펙트는 onBeforeUpdate 생명 주기 훅 내에서 구현해야함
    * ```expose``` 함수는 부모 컴포넌트가 템플릿 참조를 통해 자식 컴포넌트 인스턴스에 접근할 때, *노출되는 속성을 명시적으로 제한*하기 위해 사용
        ```vue
        export default {
           setup(props, { expose }) {
            // 인스턴스를 "닫힘" 상태로 설정
            // 예: 부모 컴포넌트에 아무것도 노출하지 않으려는 경우
            expose()

            const publicCount = ref(0)
            const privateCount = ref(0)
            // 선택적으로 로컬 상태를 노출
            expose({ count: publicCount })
          }
        }
        ```
11. 범위 내 선언된 반응형 상태에 직접 접근할 수 있는 ```렌더 함수```를 반환 가능
    > 랜더함수: *JavaScript의 전체 프로그래밍 능력이 필요한 상황에 사용되는 함수*, JavaScript의 모든 함수를 사용하여 vnode로 작업할 수 있기 때문에 매우 동적인 로직을 다룰 때 템플릿보다 더 유연
    ```vue
    import { h, ref } from 'vue'

    export default {
        setup(props, { expose }) {
            const count = ref(0)
            const increment = () => ++count.value

            expose({
                increment
            })

            return () => h('div', count.value)
        }
    }
    ```
    * 렌더 함수를 반환하면, 다른 것을 반환할 수 없음 / 템플릿 참조를 통해 이 컴포넌트의 메서드를 부모 컴포넌트에 노출할 경우 문제가 되기에 위처럼 작성하는 것이 좋다
    *``` h()```는 ```하이퍼스크립트``` 의 약자로 , **HTML(하이퍼텍스트 마크업 언어)을 생성하는 자바스크립트**를 뜻함


***


## methods
> 컴포넌트 인스턴스에서 사용할 메서드를 선언
```vue
interface ComponentOptions {
  methods?: {
    [key: string]: (this: ComponentPublicInstance, ...args: any[]) => any
  }
}

<!-- script 예제 -->
export default {
  data() {
    return { a: 1 }
  },
  methods: {
    plus() {
      this.a++
    }
  },
  created() {
    this.plus()
    console.log(this.a) // => 2
  }
}
```

