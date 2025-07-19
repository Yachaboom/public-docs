# LLM 최적화 기술 문서 작성 템플릿

## 📋 템플릿 사용 방법

### 1. 기본 정보 입력
아래 섹션의 변수들이 자동으로 치환됩니다:

```markdown
## 기술 스택 정보
- **주요 기술**: {{ sdk_name }} (예: FastAPI, React, SQLAlchemy)
- **버전**: {{ version }} (예: 3.0.0, 2024.1)
- **언어**: {{ language }} (예: Python, JavaScript, Rust)
- **SDK 유형**: {{ sdk_type }} (예: web-framework, database, api-library)
- **주요 용도**: {{ sdk_type }} 기반 개발
- **GitHub URL**: {{ github_url }}
- **문서 URL**: {{ docs_url }}
```

### 2. 문서 구조 선택
아래 3가지 옵션 중 기술에 맞는 구조를 선택하세요:

---

## 🎯 프롬프트 템플릿

```markdown
# {{ sdk_name }} {{ version }} LLM 최적화 완전 참조 문서 작성 요청

## 목표
{{ sdk_name }} {{ version }}의 **LLM 최적화된 완전한 SDK 참조 문서**를 작성해주세요. 
이 문서는 LLM이 {{ sdk_name }} 코드를 생성하고 디버깅하는데 필요한 모든 정보를 포함해야 합니다.

## 기술 스택 정보
- **주요 기술**: {{ sdk_name }}
- **버전**: {{ version }}
- **언어**: {{ language }}
- **SDK 유형**: {{ sdk_type }}
- **GitHub URL**: {{ github_url }}
- **문서 URL**: {{ docs_url }}

## 문서 구조 요구사항

### 옵션 A: 웹 프레임워크용 구조
```markdown
# {{ sdk_name }} {{ version }} 완전 SDK 참조

## 1. 빠른 참조 가이드
### 1.1 핵심 API 요약표
### 1.2 자주 사용하는 패턴 모음
### 1.3 설정 옵션 참조표

## 2. 기본 개념과 아키텍처
### 2.1 핵심 개념 (예: 컴포넌트, 라우팅, 상태 관리)
### 2.2 아키텍처 패턴
### 2.3 라이프사이클

## 3. 상세 API 참조
### 3.1 핵심 모듈
### 3.2 라우팅 시스템
### 3.3 미들웨어/인터셉터
### 3.4 상태 관리
### 3.5 폼 처리
### 3.6 HTTP 클라이언트

## 4. 통합 패턴과 실전 예제
### 4.1 인증/권한 처리
### 4.2 데이터베이스 연동
### 4.3 파일 업로드/다운로드
### 4.4 에러 처리 패턴
### 4.5 테스팅 전략

## 5. 프로덕션 가이드
### 5.1 빌드 및 배포
### 5.2 성능 최적화
### 5.3 보안 설정
### 5.4 모니터링 및 로깅
### 5.5 문제 해결
```

### 옵션 B: 데이터베이스/ORM용 구조
```markdown
# {{ sdk_name }} {{ version }} 완전 참조

## 1. 연결 및 설정
### 1.1 데이터베이스 연결
### 1.2 연결 풀 관리
### 1.3 설정 옵션 완전 가이드

## 2. 스키마 정의와 모델링
### 2.1 모델 정의
### 2.2 관계 설정
### 2.3 인덱스 및 제약조건
### 2.4 타입 매핑

## 3. 마이그레이션 시스템
### 3.1 마이그레이션 생성
### 3.2 마이그레이션 실행
### 3.3 롤백 전략
### 3.4 프로덕션 마이그레이션

## 4. 쿼리 패턴
### 4.1 기본 CRUD 작업
### 4.2 복잡한 쿼리 빌딩
### 4.3 조인 및 관계 쿼리
### 4.4 집계 함수
### 4.5 Raw SQL 사용

## 5. 고급 기능
### 5.1 트랜잭션 관리
### 5.2 이벤트 및 후크
### 5.3 캐싱 전략
### 5.4 배치 처리

## 6. 성능 최적화
### 6.1 쿼리 최적화
### 6.2 인덱싱 전략
### 6.3 연결 풀 튜닝
### 6.4 프로파일링 및 모니터링
```

### 옵션 C: API/라이브러리용 구조
```markdown
# {{ sdk_name }} {{ version }} API 참조

## 1. 시작하기
### 1.1 설치 및 설정
### 1.2 기본 사용법
### 1.3 핵심 개념
### 1.4 아키텍처 개요

## 2. 핵심 API 참조
### 2.1 [주요 네임스페이스/모듈 1]
### 2.2 [주요 네임스페이스/모듈 2]
### 2.3 [주요 네임스페이스/모듈 3]
### 2.4 유틸리티 함수들

## 3. 고급 기능
### 3.1 비동기 처리
### 3.2 이벤트 시스템
### 3.3 플러그인/확장 시스템
### 3.4 커스터마이징

## 4. 통합 및 패턴
### 4.1 일반적인 사용 사례
### 4.2 다른 라이브러리와의 통합
### 4.3 디자인 패턴
### 4.4 베스트 프랙티스

## 5. 실전 예제
### 5.1 기본 프로젝트 구조
### 5.2 완전한 애플리케이션 예제
### 5.3 테스팅 예제
### 5.4 배포 가이드
```

## API 문서 작성 표준

### 각 API 항목 필수 포함 내용:

1. **간단한 설명** (1-2문장)
2. **함수/메서드 시그니처** (완전한 타입 정보 포함)
3. **매개변수 설명**
   - 이름: 타입
   - 목적 및 설명
   - 기본값 (있는 경우)
   - 제약사항 및 유효한 값
4. **반환값 설명**
5. **완전한 사용 예제** (아래 템플릿 참조)
6. **일반적인 사용 패턴**
7. **주의사항과 팁**
8. **관련 API 참조**
9. **에러 처리 방법**

## 코드 예제 템플릿

### JavaScript/TypeScript 예제:
```typescript
// 필요한 모든 imports
import { [필요한_것들] } from '[패키지명]';

// 타입 정의 (TypeScript의 경우)
interface [타입명] {
  [속성]: [타입];
  // ...
}

// 실제 구현
async function [함수명]([매개변수]: [타입]): Promise<[반환타입]> {
  try {
    // 1. 입력 검증
    if (![매개변수]) {
      throw new Error('[에러 메시지]');
    }
    
    // 2. 핵심 로직
    const result = await [작업]();
    
    // 3. 결과 검증
    if (!result) {
      throw new Error('[에러 메시지]');
    }
    
    return result;
  } catch (error) {
    // 4. 에러 처리
    console.error('[컨텍스트]:', error);
    throw error;
  }
}

// 사용 예제
async function example() {
  try {
    const data = await [함수명]([인자]);
    console.log('Success:', data);
  } catch (error) {
    console.error('Error:', error.message);
  }
}
```

### Python 예제:
```python
# 필요한 imports
from [모듈] import [클래스/함수]
from typing import [타입_힌트]
import logging

# 로깅 설정
logger = logging.getLogger(__name__)

# 타입 정의
@dataclass
class [클래스명]:
    [필드]: [타입]
    # ...

# 실제 구현
async def [함수명]([매개변수]: [타입]) -> [반환타입]:
    """
    [함수의 목적과 기능 설명]
    
    Args:
        [매개변수]: [상세 설명]
    
    Returns:
        [반환값 설명]
    
    Raises:
        [예외타입]: [발생 조건]
    
    Example:
        >>> result = await [함수명]([예제_인자])
        >>> print(result)
    """
    try:
        # 1. 입력 검증
        if not [매개변수]:
            raise ValueError("[에러 메시지]")
        
        # 2. 핵심 로직
        result = await [작업]()
        
        # 3. 결과 검증
        if not result:
            raise ValueError("[에러 메시지]")
        
        logger.info(f"[함수명] 성공: {result}")
        return result
        
    except Exception as e:
        logger.error(f"[함수명] 실패: {e}")
        raise

# 사용 예제
async def main():
    try:
        data = await [함수명]([인자])
        print(f"결과: {data}")
    except Exception as e:
        print(f"에러: {e}")

if __name__ == "__main__":
    import asyncio
    asyncio.run(main())
```

### Rust 예제:
```rust
// 필요한 모든 imports
use [크레이트]::{[필요한_것들]};
use std::error::Error;
use tokio; // 비동기 처리용

// 커스텀 에러 타입
#[derive(Debug)]
pub enum [에러타입] {
    [에러종류1](String),
    [에러종류2](String),
}

impl std::fmt::Display for [에러타입] {
    fn fmt(&self, f: &mut std::fmt::Formatter<'_>) -> std::fmt::Result {
        match self {
            [에러타입]::[에러종류1](msg) => write!(f, "[에러종류1]: {}", msg),
            [에러타입]::[에러종류2](msg) => write!(f, "[에러종류2]: {}", msg),
        }
    }
}

impl Error for [에러타입] {}

// 타입 정의
#[derive(Debug, Clone, Serialize, Deserialize)]
pub struct [구조체명] {
    pub [필드]: [타입],
    // ...
}

// 구현
impl [구조체명] {
    /// [함수의 목적과 기능 설명]
    /// 
    /// # Arguments
    /// * `[인자]` - [상세 설명]
    /// 
    /// # Returns
    /// [반환값 설명]
    /// 
    /// # Errors
    /// [에러 발생 조건]
    /// 
    /// # Example
    /// ```
    /// let result = [구조체명]::[함수명]([예제_인자]).await?;
    /// println!("{:?}", result);
    /// ```
    pub async fn [함수명]([인자]: [타입]) -> Result<[반환타입], [에러타입]> {
        // 1. 입력 검증
        if [검증조건] {
            return Err([에러타입]::[에러종류1]("[에러 메시지]".to_string()));
        }
        
        // 2. 핵심 로직
        let result = [작업].await
            .map_err(|e| [에러타입]::[에러종류2](e.to_string()))?;
        
        // 3. 결과 검증
        if ![결과검증] {
            return Err([에러타입]::[에러종류1]("[에러 메시지]".to_string()));
        }
        
        Ok(result)
    }
}

// 사용 예제
#[tokio::main]
async fn main() -> Result<(), Box<dyn Error>> {
    match [구조체명]::[함수명]([인자]).await {
        Ok(data) => println!("성공: {:?}", data),
        Err(e) => eprintln!("에러: {}", e),
    }
    
    Ok(())
}
```

## 참조표 템플릿

### 1. 설정 옵션 참조표
| 옵션명 | 타입 | 기본값 | 설명 | 예제 |
|--------|------|--------|------|------|
| [옵션1] | [타입] | [기본값] | [설명] | `[사용예]` |
| [옵션2] | [타입] | [기본값] | [설명] | `[사용예]` |

### 2. 에러 코드 참조표
| 에러 코드/타입 | 원인 | 해결 방법 | 예제 |
|----------------|------|-----------|------|
| [에러코드] | [원인] | [해결법] | `[코드예제]` |

### 3. API 호환성 매트릭스
| 기능 | v1.0 | v2.0 | v3.0 | 비고 |
|------|------|------|------|------|
| [기능1] | ✅ | ✅ | ✅ | 안정적 |
| [기능2] | ❌ | ✅ | ✅ | v2.0부터 지원 |
| [기능3] | ✅ | ⚠️ | ❌ | v3.0에서 제거 |

### 4. 성능 특성 참조표
| 작업 | 시간복잡도 | 공간복잡도 | 참고사항 |
|------|------------|------------|----------|
| [작업1] | O(n) | O(1) | [성능 팁] |
| [작업2] | O(log n) | O(n) | [주의사항] |

## LLMs.txt 표준 파일 생성

최종 결과물로 다음 3개 파일을 생성해주세요:

### 1. main-documentation.md
전체 구조화된 문서 (위 템플릿 기반)

### 2. llms.txt (인덱스 파일)
```
# {{ sdk_name }} {{ version }} Documentation Index

## Quick Reference
- Getting Started: #getting-started
- Installation: #installation
- Core Concepts: #core-concepts
- Configuration: #configuration

## API Reference
- [핵심모듈1]: #module-1
- [핵심모듈2]: #module-2
- [핵심모듈3]: #module-3
- Utilities: #utilities

## Common Patterns
- Authentication: #authentication
- Error Handling: #error-handling
- Async Operations: #async-operations
- Testing: #testing

## Examples
- Basic Usage: #basic-usage
- Advanced Examples: #advanced-examples
- Integration Examples: #integration-examples
- Production Setup: #production-setup

## Troubleshooting
- Common Errors: #common-errors
- Performance Issues: #performance-issues
- FAQ: #frequently-asked-questions

## Reference Tables
- Configuration Options: #configuration-options
- Error Codes: #error-codes
- API Compatibility: #api-compatibility
```

### 3. llms-full.txt (전체 내용 통합 파일)
```markdown
# {{ sdk_name }} {{ version }} Complete Reference for LLMs

[목차를 포함한 전체 문서 내용을 하나의 파일로 통합]

---
문서 메타데이터:
- 생성일: {{ current_date }}
- 기술: {{ sdk_name }}
- 버전: {{ version }}
- 형식: llms.txt standard v1.0
- 토큰 최적화: 적용됨
---

[전체 문서 내용]
```

## 품질 보증 체크리스트

작성된 문서가 다음 조건을 만족하는지 확인:

### 기능성
- [ ] LLM이 코드 생성에 즉시 활용 가능
- [ ] 모든 예제가 복사-붙여넣기로 실행 가능
- [ ] 에러 처리 패턴이 모든 예제에 포함
- [ ] 실제 프로덕션 환경에서 사용 가능한 수준

### 접근성
- [ ] 초보자도 이해할 수 있는 명확한 설명
- [ ] 단계별 가이드 제공
- [ ] 용어 정의 및 설명 포함
- [ ] 시각적 구조화 (표, 코드 블록 등)

### 정확성
- [ ] 최신 버전([버전]) 기준 정보
- [ ] 모든 API 정보 검증됨
- [ ] 실제 테스트된 예제 코드
- [ ] 공식 문서와 일치하는 내용

### 완성도
- [ ] 보안 고려사항 명시
- [ ] 성능 최적화 팁 포함
- [ ] 실전 문제 해결책 포함
- [ ] 테스팅 전략 제시

### 표준 준수
- [ ] llms.txt 표준 완전 준수
- [ ] 마크다운 문법 정확성
- [ ] 앵커 링크 일관성
- [ ] 메타데이터 포함

## 참고 자료 우선순위

1. **공식 문서** (가장 높은 우선순위)
2. **GitHub 저장소** (README, examples, docs 폴더)
3. **API 레퍼런스** 
4. **커뮤니티 리소스** (Stack Overflow, Discord, Forums)
5. **실제 프로젝트 사례**

---

이 템플릿을 사용하여 {{ sdk_name }} {{ version }}의 완전하고 실용적인 LLM 최적화 문서를 작성해주세요.
```