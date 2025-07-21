# {{ sdk_name }} {{ version }} LLM 최적화 완전 참조 문서 작성 요청 v2

## 🎯 목표
{{ sdk_name }} {{ version }}의 **LLM 최적화된 완전한 SDK 참조 문서**를 작성해주세요. 
이 문서는 LLM이 {{ sdk_name }} 코드를 생성하고 디버깅하는데 필요한 모든 정보를 포함해야 합니다.

## 📋 기술 스택 정보
- **주요 기술**: {{ sdk_name }}
- **버전**: {{ version }}
- **언어**: {{ language }}
- **SDK 유형**: {{ sdk_type }}
{% if github_url %}
- **GitHub URL**: {{ github_url }}
{% endif %}
{% if docs_url %}
- **문서 URL**: {{ docs_url }}
{% endif %}
- **생성 날짜**: {{ current_date }}
- **모델**: {{ model_variant }}
- **문서 형식**: LLM 최적화 참조 문서 (llms.txt 표준 호환)
- **타겟 사용자**: AI/ML 엔지니어, 개발자, LLM 프롬프트 설계자

## 📖 문서 구조 요구사항

{% if sdk_type == 'web-framework' %}
### 웹 프레임워크용 구조
```markdown
# {{ sdk_name }} {{ version }} 완전 SDK 참조

## 1. 빠른 참조 가이드
### 1.1 핵심 API 요약표
### 1.2 자주 사용하는 패턴 모음
### 1.3 설정 옵션 참조표

## 2. 기본 개념과 아키텍처
### 2.1 핵심 개념 (컴포넌트, 라우팅, 상태 관리)
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
{% elif sdk_type == 'database' or sdk_type == 'orm' %}
### 데이터베이스/ORM용 구조
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
{% else %}
### API/라이브러리용 구조
```markdown
# {{ sdk_name }} {{ version }} API 참조

## 1. 시작하기
### 1.1 설치 및 설정
### 1.2 기본 사용법
### 1.3 핵심 개념
### 1.4 아키텍처 개요

## 2. 핵심 API 참조
### 2.1 주요 네임스페이스/모듈
### 2.2 핵심 클래스 및 함수
### 2.3 유틸리티 함수들

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
{% endif %}

## ✅ 품질 요구사항

### 코드 품질
- **완전한 실행 가능한 코드 예제** (import문부터 에러 처리까지)
- **LLM이 즉시 활용 가능한 형태**
- **프로덕션 수준의 에러 처리 패턴**
- **실무 적용 가능한 베스트 프랙티스**

### 문서 품질
- **마크다운 형식**으로 작성
- **명확한 헤딩 구조** (H1-H4 적절히 사용)
- **코드 블록에 적절한 언어 태그** 사용
- **테이블과 리스트**를 활용한 시각적 구조화

### LLM 최적화
- **토큰 효율성**: 중요한 정보를 먼저 배치
- **검색 최적화**: 키워드와 태그 적절히 사용
- **컨텍스트 유지**: 관련 정보를 섹션별로 그룹화

{% if include_security_section %}

### 🔒 보안 고려사항
- **인증/인가 패턴** 상세 설명
- **보안 베스트 프랙티스** 포함
- **취약점 방지 방법** 제시
{% endif %}

{% if include_performance_tips %}

### ⚡ 성능 최적화
- **성능 모니터링** 방법
- **병목점 해결** 전략
- **확장성 고려사항** 포함
{% endif %}

## 🎨 출력 형식 지침

### 각 API 항목 필수 포함 내용
1. **간단한 설명** (1-2문장)
2. **함수/메서드 시그니처** (완전한 타입 정보 포함)
3. **매개변수 설명** (이름, 타입, 목적, 기본값, 제약사항)
4. **반환값 설명**
5. **완전한 사용 예제** (아래 템플릿 참조)
6. **일반적인 사용 패턴**
7. **주의사항과 팁**
8. **관련 API 참조**
9. **에러 처리 방법**

### {{ language }} 코드 예제 템플릿
{% if language == 'Python' %}
```python
# 필요한 imports 모두 포함
from {{ sdk_name | lower }} import (
    필요한_클래스,
    필요한_함수,
    필요한_예외
)
from typing import Dict, List, Optional, Union, Any
import asyncio
import logging
from dataclasses import dataclass
from pathlib import Path

# 로깅 설정
logger = logging.getLogger(__name__)

# 타입 정의 (Python 3.11+ 타입 힌트 활용)
@dataclass
class ConfigModel:
    """설정 모델 클래스
    
    Attributes:
        name: 설정 이름
        value: 설정 값
        is_active: 활성화 여부
    """
    name: str
    value: Union[str, int, bool]
    is_active: bool = True

# 실제 구현
async def process_data(
    data: Dict[str, Any], 
    config: Optional[ConfigModel] = None,
    timeout: float = 30.0
) -> Dict[str, Any]:
    """데이터를 처리하는 비동기 함수
    
    Args:
        data: 처리할 데이터 딕셔너리
        config: 선택적 설정 객체
        timeout: 처리 시간 제한 (초)
    
    Returns:
        처리된 결과 데이터 딕셔너리
    
    Raises:
        ValueError: 입력 데이터가 유효하지 않을 때
        TimeoutError: 처리 시간이 초과되었을 때
        ConnectionError: 네트워크 연결 오류 발생 시
    
    Example:
        >>> config = ConfigModel(name="test", value="example")
        >>> result = await process_data({"key": "value"}, config)
        >>> print(result)
        {'processed': True, 'data': {'key': 'value'}}
    """
    try:
        # 1. 입력 검증 (Python의 강력한 타입 검사 활용)
        if not isinstance(data, dict) or not data:
            raise ValueError("입력 데이터는 비어있지 않은 딕셔너리여야 합니다")
        
        if config and not isinstance(config, ConfigModel):
            raise TypeError("config는 ConfigModel 인스턴스여야 합니다")
        
        # 2. 비동기 처리 (asyncio 패턴 활용)
        start_time = asyncio.get_event_loop().time()
        
        # 실제 처리 로직
        processed_data = {}
        for key, value in data.items():
            # Python의 match-case 구문 활용 (3.10+)
            match value:
                case str() if value.strip():
                    processed_data[key] = value.upper()
                case int() | float():
                    processed_data[key] = value * 2
                case list() | tuple():
                    processed_data[key] = len(value)
                case _:
                    processed_data[key] = str(value)
        
        # 3. 시간 제한 검사
        elapsed = asyncio.get_event_loop().time() - start_time
        if elapsed > timeout:
            raise TimeoutError(f"처리 시간 초과: {elapsed:.2f}초 > {timeout}초")
        
        # 4. 결과 검증 및 반환
        result = {
            "processed": True,
            "data": processed_data,
            "processing_time": elapsed,
            "config_used": config.name if config else None
        }
        
        logger.info(f"데이터 처리 완료: {len(data)}개 항목, {elapsed:.3f}초 소요")
        return result
        
    except ValueError as e:
        logger.error(f"입력 검증 실패: {e}")
        raise
    except TimeoutError as e:
        logger.error(f"시간 초과 오류: {e}")
        raise
    except Exception as e:
        logger.error(f"예상치 못한 오류 발생: {type(e).__name__}: {e}")
        raise ConnectionError(f"데이터 처리 중 오류: {e}") from e

# 컨텍스트 매니저 패턴 (with 문 활용)
class DataProcessor:
    """데이터 처리기 클래스 - Python의 컨텍스트 매니저 패턴 활용"""
    
    def __init__(self, config: ConfigModel):
        self.config = config
        self.is_connected = False
    
    async def __aenter__(self):
        """비동기 컨텍스트 매니저 진입"""
        await self.connect()
        return self
    
    async def __aexit__(self, exc_type, exc_val, exc_tb):
        """비동기 컨텍스트 매니저 종료"""
        await self.disconnect()
        if exc_type:
            logger.error(f"처리 중 오류: {exc_type.__name__}: {exc_val}")
        return False
    
    async def connect(self):
        """연결 설정"""
        self.is_connected = True
        logger.info("데이터 처리기 연결됨")
    
    async def disconnect(self):
        """연결 해제"""
        self.is_connected = False
        logger.info("데이터 처리기 연결 해제됨")

# 사용 예제 (Python의 다양한 패턴 시연)
async def main():
    """메인 실행 함수 - Python 비동기 프로그래밍 패턴"""
    try:
        # 설정 객체 생성
        config = ConfigModel(
            name="production_config",
            value="high_performance",
            is_active=True
        )
        
        # 기본 사용법
        sample_data = {
            "username": "john_doe",
            "age": 30,
            "tags": ["developer", "python", "ai"],
            "score": 85.5
        }
        
        result = await process_data(sample_data, config, timeout=10.0)
        print(f"처리 결과: {result}")
        
        # 컨텍스트 매니저 사용법
        async with DataProcessor(config) as processor:
            # 추가 처리 로직
            print(f"프로세서 상태: {processor.is_connected}")
        
        # 리스트 컴프리헨션과 비동기 처리 조합
        tasks = [
            process_data({"item": i}, config)
            for i in range(5)
        ]
        results = await asyncio.gather(*tasks, return_exceptions=True)
        
        for i, result in enumerate(results):
            if isinstance(result, Exception):
                print(f"작업 {i} 실패: {result}")
            else:
                print(f"작업 {i} 성공: {result['processed']}")
                
    except Exception as e:
        print(f"메인 실행 오류: {e}")
        logger.exception("상세 오류 정보")

# Python 스크립트 실행 패턴
if __name__ == "__main__":
    # Python의 asyncio 이벤트 루프 실행
    try:
        asyncio.run(main())
    except KeyboardInterrupt:
        print("\n프로그램이 사용자에 의해 중단되었습니다.")
    except Exception as e:
        print(f"프로그램 실행 중 오류: {e}")
        exit(1)
```
{% elif language == 'JavaScript' %}
```javascript
// ES6+ 모듈 시스템과 구조 분해 할당 활용
const { 
  processData, 
  DataProcessor, 
  ValidationError 
} = require('{{ sdk_name | lower }}');
const fs = require('fs').promises;
const path = require('path');
const { promisify } = require('util');
const EventEmitter = require('events');

// 최신 JavaScript 클래스 문법 활용
class ConfigManager extends EventEmitter {
  /**
   * 설정 관리 클래스
   * @param {Object} options - 설정 옵션
   * @param {string} options.name - 설정 이름
   * @param {string|number|boolean} options.value - 설정 값
   * @param {boolean} [options.isActive=true] - 활성화 여부
   */
  constructor({ name, value, isActive = true }) {
    super();
    this.name = name;
    this.value = value;
    this.isActive = isActive;
    this.createdAt = new Date();
  }

  // Getter/Setter 패턴
  get displayName() {
    return `${this.name} (${this.isActive ? 'active' : 'inactive'})`;
  }

  set value(newValue) {
    const oldValue = this._value;
    this._value = newValue;
    this.emit('valueChanged', { oldValue, newValue });
  }

  get value() {
    return this._value;
  }
}

/**
 * 데이터를 비동기로 처리하는 함수 (ES2020+ 기능 활용)
 * @param {Object} data - 처리할 데이터 객체
 * @param {ConfigManager} [config=null] - 선택적 설정 객체
 * @param {number} [timeout=30000] - 처리 시간 제한 (밀리초)
 * @returns {Promise<Object>} 처리된 결과 객체
 * @throws {ValidationError} 입력 데이터가 유효하지 않을 때
 * @throws {Error} 처리 시간이 초과되었을 때
 * 
 * @example
 * const config = new ConfigManager({ name: "test", value: "example" });
 * const result = await processUserData({ name: "John" }, config);
 * console.log(result);
 * // { processed: true, data: { name: "JOHN" }, processingTime: 45 }
 */
async function processUserData(data, config = null, timeout = 30000) {
  const startTime = performance.now();
  
  try {
    // 1. 입력 검증 (JavaScript의 다양한 타입 체킹 방법)
    if (!data || typeof data !== 'object' || Object.keys(data).length === 0) {
      throw new ValidationError('입력 데이터는 비어있지 않은 객체여야 합니다');
    }

    if (config && !(config instanceof ConfigManager)) {
      throw new TypeError('config는 ConfigManager 인스턴스여야 합니다');
    }

    // 2. Promise.race로 타임아웃 구현
    const processingPromise = processDataInternal(data, config);
    const timeoutPromise = new Promise((_, reject) => {
      setTimeout(() => reject(new Error(`처리 시간 초과: ${timeout}ms`)), timeout);
    });

    // 3. 비동기 데이터 처리 (다양한 ES6+ 패턴 활용)
    const processedData = await Promise.race([processingPromise, timeoutPromise]);
    
    // 4. 결과 객체 생성 (구조 분해 할당과 단축 속성명)
    const processingTime = performance.now() - startTime;
    const result = {
      processed: true,
      data: processedData,
      processingTime: Math.round(processingTime * 100) / 100,
      configUsed: config?.name ?? null,
      timestamp: new Date().toISOString()
    };

    console.log(`✅ 데이터 처리 완료: ${Object.keys(data).length}개 항목, ${result.processingTime}ms 소요`);
    return result;

  } catch (error) {
    const processingTime = performance.now() - startTime;
    console.error(`❌ 처리 실패 (${processingTime.toFixed(2)}ms):`, error.message);
    
    // 에러 타입별 처리
    if (error instanceof ValidationError) {
      throw error; // 재throw
    } else if (error.message.includes('시간 초과')) {
      throw new Error(`타임아웃 오류: ${error.message}`);
    } else {
      throw new Error(`데이터 처리 중 예상치 못한 오류: ${error.message}`);
    }
  }
}

// 내부 처리 함수 (Promise 체이닝과 async/await 혼합 패턴)
async function processDataInternal(data, config) {
  const processedData = {};
  
  // Object.entries()와 for...of 루프 활용
  for (const [key, value] of Object.entries(data)) {
    // 타입별 처리 (JavaScript의 동적 타이핑 활용)
    switch (typeof value) {
      case 'string':
        processedData[key] = value.trim() ? value.toUpperCase() : '';
        break;
      case 'number':
        processedData[key] = value * 2;
        break;
      case 'boolean':
        processedData[key] = !value;
        break;
      case 'object':
        if (Array.isArray(value)) {
          processedData[key] = value.length;
        } else if (value !== null) {
          // 재귀적 객체 처리
          processedData[key] = await processDataInternal(value, config);
        } else {
          processedData[key] = null;
        }
        break;
      default:
        processedData[key] = String(value);
    }
  }

  return processedData;
}

// 클래스 기반 데이터 처리기 (ES6 클래스와 Symbol 활용)
class DataProcessor extends EventEmitter {
  // Private 필드 (ES2022)
  #isConnected = false;
  #config = null;
  
  // Static 메서드
  static createWithDefaults(name) {
    const config = new ConfigManager({
      name,
      value: 'default',
      isActive: true
    });
    return new DataProcessor(config);
  }

  constructor(config) {
    super();
    this.#config = config;
    this.connectionId = Symbol('connection');
  }

  // Async iterator 패턴 (ES2018)
  async* processStream(dataStream) {
    for await (const chunk of dataStream) {
      try {
        const result = await processUserData(chunk, this.#config);
        yield result;
      } catch (error) {
        this.emit('error', error);
        yield { error: error.message, chunk };
      }
    }
  }

  // getter로 private 필드 접근
  get isConnected() {
    return this.#isConnected;
  }

  get config() {
    return { ...this.#config }; // 얕은 복사로 불변성 보장
  }

  async connect() {
    if (this.#isConnected) {
      throw new Error('이미 연결되어 있습니다');
    }
    
    this.#isConnected = true;
    this.emit('connected', { connectionId: this.connectionId });
    console.log('🔗 데이터 처리기 연결됨');
  }

  async disconnect() {
    if (!this.#isConnected) {
      console.warn('⚠️ 이미 연결이 해제되어 있습니다');
      return;
    }
    
    this.#isConnected = false;
    this.emit('disconnected', { connectionId: this.connectionId });
    console.log('🔌 데이터 처리기 연결 해제됨');
  }
}

// 실사용 예제 (모던 JavaScript 패턴 종합)
async function demonstrateUsage() {
  console.log('🚀 JavaScript 데이터 처리 데모 시작');
  
  try {
    // 1. 기본 사용법 (구조 분해 할당과 기본값)
    const config = new ConfigManager({
      name: 'production_config',
      value: 'high_performance',
      isActive: true
    });

    const sampleData = {
      username: '  john_doe  ',
      age: 30,
      tags: ['developer', 'javascript', 'node'],
      profile: {
        bio: 'Full-stack developer',
        active: true
      },
      score: 85.5
    };

    // 2. 비동기 처리와 에러 핸들링
    const result = await processUserData(sampleData, config, 10000);
    console.log('📊 처리 결과:', JSON.stringify(result, null, 2));

    // 3. 클래스 인스턴스 사용 (Factory 패턴)
    const processor = DataProcessor.createWithDefaults('demo_processor');
    
    // 4. 이벤트 리스너 등록
    processor.on('connected', ({ connectionId }) => {
      console.log(`🎉 연결 완료: ${connectionId.toString()}`);
    });

    processor.on('error', (error) => {
      console.error('💥 처리기 오류:', error.message);
    });

    await processor.connect();

    // 5. Promise.all을 활용한 병렬 처리
    const batchData = Array.from({ length: 5 }, (_, i) => ({
      item: `item_${i}`,
      value: Math.random() * 100
    }));

    const batchResults = await Promise.allSettled(
      batchData.map(item => processUserData(item, config))
    );

    // 6. 결과 분석 (map, filter, reduce 활용)
    const { fulfilled, rejected } = batchResults.reduce(
      (acc, result) => {
        if (result.status === 'fulfilled') {
          acc.fulfilled.push(result.value);
        } else {
          acc.rejected.push(result.reason);
        }
        return acc;
      },
      { fulfilled: [], rejected: [] }
    );

    console.log(`✅ 성공: ${fulfilled.length}개, ❌ 실패: ${rejected.length}개`);

    // 7. 정리 작업
    await processor.disconnect();

  } catch (error) {
    console.error('💣 메인 실행 오류:', error.message);
    console.error('스택 트레이스:', error.stack);
  } finally {
    console.log('🏁 데모 완료');
  }
}

// Node.js 환경 감지 및 실행
if (typeof require !== 'undefined' && require.main === module) {
  // IIFE (즉시 실행 함수) 패턴
  (async () => {
    try {
      await demonstrateUsage();
    } catch (error) {
      console.error('프로그램 실행 실패:', error);
      process.exit(1);
    }
  })();
}

// CommonJS와 ES Module 모두 지원하는 내보내기
module.exports = {
  processUserData,
  DataProcessor,
  ConfigManager,
  demonstrateUsage
};

// ES Module 지원
if (typeof module !== 'undefined' && module.exports) {
  module.exports.default = { processUserData, DataProcessor, ConfigManager };
}
```
{% elif language == 'TypeScript' %}
```typescript
// TypeScript 5.0+ ES2022 모듈 시스템과 고급 타입 활용
import { 
  processData, 
  DataProcessor as BaseDataProcessor, 
  ValidationError 
} from '{{ sdk_name | lower }}';
import { promises as fs } from 'fs';
import { join, resolve } from 'path';
import { EventEmitter } from 'events';
import { performance } from 'perf_hooks';

// 고급 TypeScript 타입 정의
type ConfigValue = string | number | boolean | null;
type ProcessingMode = 'sync' | 'async' | 'stream';
type LogLevel = 'debug' | 'info' | 'warn' | 'error';

// 유니온 타입과 리터럴 타입
interface ProcessingOptions {
  mode?: ProcessingMode;
  timeout?: number;
  retries?: number;
  logLevel?: LogLevel;
}

// 제네릭 인터페이스와 조건부 타입
interface ConfigManagerOptions<T = ConfigValue> {
  readonly name: string;
  value: T;
  isActive?: boolean;
  metadata?: Record<string, unknown>;
}

// 맵드 타입과 키 of 연산자
type PartialConfig<T> = {
  [K in keyof T]?: T[K];
};

// 템플릿 리터럴 타입 (TypeScript 4.1+)
type EventName = `config:${string}` | `processor:${string}` | 'error';

// 커스텀 에러 클래스 (타입 안전한 에러 처리)
class ProcessingError extends Error {
  constructor(
    message: string,
    public readonly code: string,
    public readonly context?: Record<string, unknown>
  ) {
    super(message);
    this.name = 'ProcessingError';
  }
}

class ValidationError extends Error {
  constructor(
    message: string,
    public readonly field: string,
    public readonly value: unknown
  ) {
    super(message);
    this.name = 'ValidationError';
  }
}

// 추상 클래스와 제네릭 클래스
abstract class BaseConfig<T = ConfigValue> {
  protected readonly _createdAt: Date = new Date();
  
  constructor(
    public readonly name: string,
    protected _value: T,
    public readonly isActive: boolean = true
  ) {}

  // 추상 메서드
  abstract validate(value: T): boolean;
  
  // 타입 가드
  protected isValidValue(value: unknown): value is T {
    return this.validate(value as T);
  }

  get value(): T {
    return this._value;
  }

  get createdAt(): Date {
    return new Date(this._createdAt);
  }
}

// 구체 클래스 구현
class ConfigManager<T = ConfigValue> extends BaseConfig<T> {
  private readonly _eventEmitter = new EventEmitter();
  private _metadata: Map<string, unknown> = new Map();

  constructor(options: ConfigManagerOptions<T>) {
    super(options.name, options.value, options.isActive ?? true);
    
    if (options.metadata) {
      Object.entries(options.metadata).forEach(([key, value]) => {
        this._metadata.set(key, value);
      });
    }
  }

  // 메서드 오버로딩
  validate(value: T): boolean;
  validate(value: T, strict: true): asserts value is NonNullable<T>;
  validate(value: T, strict?: boolean): boolean | asserts value is NonNullable<T> {
    const isValid = value !== null && value !== undefined;
    
    if (strict && !isValid) {
      throw new ValidationError(
        `Invalid value for ${this.name}`,
        this.name,
        value
      );
    }
    
    return isValid;
  }

  // 제네릭 메서드
  updateValue<U extends T>(newValue: U): Promise<void> {
    return new Promise((resolve, reject) => {
      try {
        this.validate(newValue, true);
        const oldValue = this._value;
        this._value = newValue;
        
        this._eventEmitter.emit('config:valueChanged', {
          oldValue,
          newValue,
          timestamp: new Date()
        });
        
        resolve();
      } catch (error) {
        reject(error);
      }
    });
  }

  // 타입 안전한 메타데이터 접근
  getMetadata<U = unknown>(key: string): U | undefined {
    return this._metadata.get(key) as U | undefined;
  }

  setMetadata(key: string, value: unknown): void {
    this._metadata.set(key, value);
    this._eventEmitter.emit('config:metadataChanged', { key, value });
  }

  // 이벤트 리스너 (타입 안전)
  on(event: EventName, listener: (...args: any[]) => void): this {
    this._eventEmitter.on(event, listener);
    return this;
  }

  // 불변성을 보장하는 상태 복사
  clone(): ConfigManager<T> {
    const metadata = Array.from(this._metadata.entries()).reduce(
      (acc, [key, value]) => ({ ...acc, [key]: value }),
      {}
    );
    
    return new ConfigManager({
      name: this.name,
      value: this._value,
      isActive: this.isActive,
      metadata
    });
  }
}

// 고급 함수 시그니처 (오버로드와 조건부 타입)
interface ProcessDataResult<T = Record<string, unknown>> {
  readonly processed: true;
  readonly data: T;
  readonly processingTime: number;
  readonly configUsed: string | null;
  readonly timestamp: string;
  readonly metadata?: Record<string, unknown>;
}

// 함수 오버로딩으로 타입 안전성 강화
async function processUserData<T extends Record<string, unknown>>(
  data: T,
  config?: ConfigManager,
  options?: ProcessingOptions
): Promise<ProcessDataResult<T>>;

async function processUserData<T extends Record<string, unknown>>(
  data: T[],
  config?: ConfigManager,
  options?: ProcessingOptions
): Promise<ProcessDataResult<T>[]>;

/**
 * 데이터를 타입 안전하게 비동기 처리하는 제네릭 함수
 * @template T - 입력 데이터의 타입
 * @param data - 처리할 데이터 (객체 또는 객체 배열)
 * @param config - 선택적 설정 매니저 인스턴스
 * @param options - 처리 옵션
 * @returns 처리된 결과의 Promise
 * @throws {ValidationError} 입력 데이터가 유효하지 않을 때
 * @throws {ProcessingError} 처리 중 오류가 발생했을 때
 * 
 * @example
 * interface UserData {
 *   name: string;
 *   age: number;
 * }
 * 
 * const config = new ConfigManager({ name: "user-processor", value: "v1.0" });
 * const userData: UserData = { name: "John", age: 30 };
 * const result = await processUserData(userData, config);
 * console.log(result.data.name); // TypeScript가 타입을 알고 있음
 */
async function processUserData<T extends Record<string, unknown>>(
  data: T | T[],
  config?: ConfigManager,
  options: ProcessingOptions = {}
): Promise<ProcessDataResult<T> | ProcessDataResult<T>[]> {
  const startTime = performance.now();
  const { mode = 'async', timeout = 30000, retries = 3, logLevel = 'info' } = options;

  // 타입 가드 함수
  const isDataArray = (input: T | T[]): input is T[] => Array.isArray(input);
  const isValidObject = (input: unknown): input is Record<string, unknown> => 
    typeof input === 'object' && input !== null && !Array.isArray(input);

  try {
    // 1. 런타임 타입 검증 (타입 가드 활용)
    if (isDataArray(data)) {
      if (data.length === 0) {
        throw new ValidationError('입력 배열이 비어있습니다', 'data', data);
      }
      
      // 배열의 모든 요소 검증
      data.forEach((item, index) => {
        if (!isValidObject(item)) {
          throw new ValidationError(
            `배열 인덱스 ${index}의 요소가 유효한 객체가 아닙니다`,
            `data[${index}]`,
            item
          );
        }
      });
    } else {
      if (!isValidObject(data)) {
        throw new ValidationError('입력 데이터가 유효한 객체가 아닙니다', 'data', data);
      }
    }

    if (config && !(config instanceof ConfigManager)) {
      throw new ValidationError(
        'config는 ConfigManager 인스턴스여야 합니다',
        'config',
        config
      );
    }

    // 2. 비동기 처리 with 타임아웃 (Promise 레이스 패턴)
    const processingPromise = isDataArray(data) 
      ? processDataArrayInternal(data, config, options)
      : processDataInternal(data, config, options);

    const timeoutPromise = new Promise<never>((_, reject) => {
      setTimeout(() => {
        reject(new ProcessingError(
          `처리 시간 초과: ${timeout}ms`,
          'TIMEOUT_ERROR',
          { timeout, mode }
        ));
      }, timeout);
    });

    const processedData = await Promise.race([processingPromise, timeoutPromise]);
    
    // 3. 결과 객체 생성 (타입 안전한 객체 구성)
    const processingTime = Math.round((performance.now() - startTime) * 100) / 100;
    
    if (isDataArray(data)) {
      return (processedData as T[]).map(item => ({
        processed: true as const,
        data: item,
        processingTime,
        configUsed: config?.name ?? null,
        timestamp: new Date().toISOString(),
        metadata: {
          mode,
          itemsProcessed: data.length,
          retries
        }
      }));
    } else {
      return {
        processed: true as const,
        data: processedData as T,
        processingTime,
        configUsed: config?.name ?? null,
        timestamp: new Date().toISOString(),
        metadata: {
          mode,
          retries
        }
      };
    }

  } catch (error) {
    const processingTime = performance.now() - startTime;
    
    // 타입 안전한 에러 처리
    if (error instanceof ValidationError || error instanceof ProcessingError) {
      if (logLevel !== 'debug') {
        console.error(`❌ ${error.constructor.name}: ${error.message}`);
      }
      throw error;
    }
    
    // 알 수 없는 에러를 ProcessingError로 감싸기
    const wrappedError = new ProcessingError(
      `예상치 못한 오류: ${error instanceof Error ? error.message : String(error)}`,
      'UNKNOWN_ERROR',
      { originalError: error, processingTime }
    );
    
    console.error('💥 처리 실패:', wrappedError.message);
    throw wrappedError;
  }
}

// 내부 처리 함수들 (타입 안전한 구현)
async function processDataInternal<T extends Record<string, unknown>>(
  data: T,
  config?: ConfigManager,
  options?: ProcessingOptions
): Promise<T> {
  const result = {} as T;
  
  // keyof 연산자와 타입 안전한 반복
  for (const key in data) {
    if (Object.prototype.hasOwnProperty.call(data, key)) {
      const value = data[key];
      
      // 타입 안전한 값 처리
      switch (typeof value) {
        case 'string':
          (result as any)[key] = value.trim() ? value.toUpperCase() : '';
          break;
        case 'number':
          (result as any)[key] = value * 2;
          break;
        case 'boolean':
          (result as any)[key] = !value;
          break;
        case 'object':
          if (Array.isArray(value)) {
            (result as any)[key] = value.length;
          } else if (value !== null) {
            // 재귀적 처리 (타입 안전성 유지)
            (result as any)[key] = await processDataInternal(
              value as Record<string, unknown>,
              config,
              options
            );
          } else {
            (result as any)[key] = null;
          }
          break;
        default:
          (result as any)[key] = String(value);
      }
    }
  }
  
  return result;
}

async function processDataArrayInternal<T extends Record<string, unknown>>(
  dataArray: T[],
  config?: ConfigManager,
  options?: ProcessingOptions
): Promise<T[]> {
  // Promise.allSettled로 병렬 처리 (부분 실패 허용)
  const results = await Promise.allSettled(
    dataArray.map(item => processDataInternal(item, config, options))
  );
  
  const processedItems: T[] = [];
  const errors: { index: number; error: Error }[] = [];
  
  results.forEach((result, index) => {
    if (result.status === 'fulfilled') {
      processedItems.push(result.value);
    } else {
      errors.push({ index, error: result.reason });
    }
  });
  
  // 에러가 있으면 상세 정보와 함께 예외 발생
  if (errors.length > 0) {
    throw new ProcessingError(
      `배열 처리 중 ${errors.length}개 항목에서 오류 발생`,
      'BATCH_PROCESSING_ERROR',
      { errors: errors.map(e => ({ index: e.index, message: e.error.message })) }
    );
  }
  
  return processedItems;
}

// 고급 클래스 (추상화, 인터페이스 구현, 제네릭)
interface IDataProcessor<T = unknown> {
  readonly isConnected: boolean;
  readonly config: Readonly<ConfigManager>;
  connect(): Promise<void>;
  disconnect(): Promise<void>;
  process(data: T): Promise<ProcessDataResult<T>>;
}

class DataProcessor<T extends Record<string, unknown> = Record<string, unknown>> 
  extends EventEmitter implements IDataProcessor<T> {
  
  // Private 필드 (TypeScript 4.3+)
  readonly #isConnected: boolean = false;
  readonly #config: ConfigManager;
  readonly #connectionId: symbol;
  
  // 정적 팩토리 메서드 (제네릭 지원)
  static createWithDefaults<U extends Record<string, unknown>>(
    name: string,
    defaultValue: ConfigValue = 'default'
  ): DataProcessor<U> {
    const config = new ConfigManager({
      name,
      value: defaultValue,
      isActive: true,
      metadata: { createdBy: 'factory', version: '1.0.0' }
    });
    return new DataProcessor<U>(config);
  }

  constructor(config: ConfigManager) {
    super();
    this.#config = config;
    this.#connectionId = Symbol('processor-connection');
    
    // 설정 변경 이벤트 리스닝
    this.#config.on('config:valueChanged', (event) => {
      this.emit('processor:configChanged', event);
    });
  }

  // ReadOnly 속성 (불변성 보장)
  get isConnected(): boolean {
    return this.#isConnected;
  }

  get config(): Readonly<ConfigManager> {
    return this.#config;
  }

  get connectionId(): symbol {
    return this.#connectionId;
  }

  // 비동기 제너레이터 (AsyncIterator 패턴)
  async* processStream(dataStream: AsyncIterable<T>): AsyncGenerator<ProcessDataResult<T>, void, unknown> {
    if (!this.#isConnected) {
      throw new ProcessingError(
        '스트림 처리를 위해서는 먼저 연결이 필요합니다',
        'NOT_CONNECTED',
        { connectionId: this.#connectionId.toString() }
      );
    }

    for await (const chunk of dataStream) {
      try {
        const result = await this.process(chunk);
        yield result;
      } catch (error) {
        this.emit('error', error);
        yield {
          processed: false,
          error: error instanceof Error ? error.message : String(error),
          chunk
        } as any; // 에러 케이스는 타입 단언 사용
      }
    }
  }

  async connect(): Promise<void> {
    if (this.#isConnected) {
      throw new ProcessingError(
        '이미 연결되어 있습니다',
        'ALREADY_CONNECTED',
        { connectionId: this.#connectionId.toString() }
      );
    }
    
    // 연결 로직 (비동기 시뮬레이션)
    await new Promise(resolve => setTimeout(resolve, 100));
    
    (this as any).#isConnected = true;
    this.emit('processor:connected', { 
      connectionId: this.#connectionId.toString(),
      timestamp: new Date()
    });
    
    console.log('🔗 TypeScript 데이터 처리기 연결됨');
  }

  async disconnect(): Promise<void> {
    if (!this.#isConnected) {
      console.warn('⚠️ 이미 연결이 해제되어 있습니다');
      return;
    }
    
    (this as any).#isConnected = false;
    this.emit('processor:disconnected', { 
      connectionId: this.#connectionId.toString(),
      timestamp: new Date()
    });
    
    console.log('🔌 TypeScript 데이터 처리기 연결 해제됨');
  }

  async process(data: T): Promise<ProcessDataResult<T>> {
    if (!this.#isConnected) {
      throw new ProcessingError(
        '처리를 위해서는 먼저 연결이 필요합니다',
        'NOT_CONNECTED'
      );
    }

    return processUserData(data, this.#config);
  }
}

// 실사용 예제 (TypeScript 고급 기능 종합 시연)
interface UserProfile {
  readonly id: number;
  name: string;
  email: string;
  age: number;
  tags: ReadonlyArray<string>;
  preferences: {
    theme: 'light' | 'dark';
    notifications: boolean;
  };
}

async function demonstrateTypeScriptUsage(): Promise<void> {
  console.log('🚀 TypeScript 고급 기능 데모 시작');
  
  try {
    // 1. 타입 안전한 설정 객체 생성
    const config = new ConfigManager<string>({
      name: 'user-profile-processor',
      value: 'production',
      isActive: true,
      metadata: {
        version: '2.0.0',
        environment: 'production',
        features: ['validation', 'caching', 'monitoring']
      }
    });

    // 2. 강타입 데이터 정의
    const userProfile: UserProfile = {
      id: 1,
      name: '  김개발  ',
      email: 'kim@example.com',
      age: 28,
      tags: ['developer', 'typescript', 'react'] as const,
      preferences: {
        theme: 'dark',
        notifications: true
      }
    };

    // 3. 타입 안전한 데이터 처리
    const result = await processUserData(userProfile, config, {
      mode: 'async',
      timeout: 5000,
      logLevel: 'info'
    });

    console.log('📊 처리 결과:', {
      ...result,
      data: {
        ...result.data,
        // TypeScript가 타입을 정확히 추론
        processedName: result.data.name,
        doubledAge: result.data.age
      }
    });

    // 4. 제네릭 클래스 사용
    const processor = DataProcessor.createWithDefaults<UserProfile>('demo-processor');
    
    // 5. 타입 안전한 이벤트 핸들링
    processor.on('processor:connected', (event) => {
      console.log(`🎉 연결 완료: ${event.connectionId} at ${event.timestamp}`);
    });

    processor.on('error', (error: Error) => {
      console.error('💥 처리기 오류:', error.message);
    });

    await processor.connect();

    // 6. 배치 처리 (타입 안전성 유지)
    const batchData: UserProfile[] = Array.from({ length: 3 }, (_, i) => ({
      id: i + 2,
      name: `사용자${i + 2}`,
      email: `user${i + 2}@example.com`,
      age: 25 + i,
      tags: ['user', 'test'],
      preferences: {
        theme: i % 2 === 0 ? 'light' : 'dark',
        notifications: true
      }
    }));

    const batchResults = await processUserData(batchData, config);
    console.log(`✅ 배치 처리 완료: ${batchResults.length}개 프로필 처리됨`);

    // 7. 에러 처리 데모
    try {
      await processUserData(null as any, config);
    } catch (error) {
      if (error instanceof ValidationError) {
        console.log(`🔍 검증 에러 감지: ${error.field} - ${error.message}`);
      }
    }

    await processor.disconnect();

  } catch (error) {
    if (error instanceof ProcessingError) {
      console.error(`💣 처리 에러: [${error.code}] ${error.message}`);
      if (error.context) {
        console.error('컨텍스트:', error.context);
      }
    } else {
      console.error('💥 예상치 못한 오류:', error);
    }
  } finally {
    console.log('🏁 TypeScript 데모 완료');
  }
}

// 타입 안전한 모듈 내보내기
export {
  ConfigManager,
  DataProcessor,
  processUserData,
  ProcessingError,
  ValidationError,
  demonstrateTypeScriptUsage
};

export type {
  ConfigValue,
  ProcessingMode,
  LogLevel,
  ProcessingOptions,
  ConfigManagerOptions,
  ProcessDataResult,
  IDataProcessor,
  UserProfile
};

// CommonJS 호환성
if (typeof module !== 'undefined' && module.exports) {
  module.exports = {
    ConfigManager,
    DataProcessor,
    processUserData,
    ProcessingError,
    ValidationError,
    demonstrateTypeScriptUsage
  };
}

// 실행 환경 감지 및 데모 실행
if (typeof require !== 'undefined' && require.main === module) {
  demonstrateTypeScriptUsage().catch(console.error);
}
```
{% else %}
```{{ language.lower() }}
{% if language == 'Java' %}
// Java 코드 예제 - Spring Boot 스타일
package com.example.{{ sdk_name | lower }};

import {{ sdk_name | lower }}.*;
import org.springframework.stereotype.Service;
import org.springframework.beans.factory.annotation.Autowired;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import java.util.*;
import java.util.concurrent.CompletableFuture;
import java.time.LocalDateTime;

@Service
public class DataProcessorService {
    private static final Logger logger = LoggerFactory.getLogger(DataProcessorService.class);
    
    @Autowired
    private ConfigManager configManager;
    
    /**
     * 데이터를 비동기로 처리하는 메서드
     * @param data 처리할 데이터 맵
     * @param config 설정 객체
     * @return 처리된 결과의 CompletableFuture
     * @throws ValidationException 입력 데이터가 유효하지 않을 때
     * @throws ProcessingException 처리 중 오류가 발생했을 때
     */
    public CompletableFuture<ProcessingResult> processDataAsync(
            Map<String, Object> data, 
            ProcessingConfig config) throws ValidationException {
        
        return CompletableFuture.supplyAsync(() -> {
            long startTime = System.currentTimeMillis();
            
            try {
                // 1. 입력 검증
                if (data == null || data.isEmpty()) {
                    throw new ValidationException("입력 데이터가 비어있습니다");
                }
                
                // 2. 데이터 처리
                Map<String, Object> processedData = new HashMap<>();
                for (Map.Entry<String, Object> entry : data.entrySet()) {
                    Object value = entry.getValue();
                    if (value instanceof String) {
                        processedData.put(entry.getKey(), ((String) value).toUpperCase());
                    } else if (value instanceof Number) {
                        processedData.put(entry.getKey(), ((Number) value).doubleValue() * 2);
                    } else {
                        processedData.put(entry.getKey(), value.toString());
                    }
                }
                
                // 3. 결과 생성
                long processingTime = System.currentTimeMillis() - startTime;
                ProcessingResult result = new ProcessingResult(
                    true,
                    processedData,
                    processingTime,
                    config.getName(),
                    LocalDateTime.now()
                );
                
                logger.info("데이터 처리 완료: {}ms", processingTime);
                return result;
                
            } catch (Exception e) {
                logger.error("데이터 처리 실패: {}", e.getMessage(), e);
                throw new ProcessingException("처리 중 오류 발생", e);
            }
        });
    }
    
    // 사용 예제
    public static void main(String[] args) {
        DataProcessorService service = new DataProcessorService();
        Map<String, Object> testData = Map.of(
            "name", "john_doe",
            "age", 30,
            "active", true
        );
        
        ProcessingConfig config = new ProcessingConfig("test-config");
        
        service.processDataAsync(testData, config)
            .thenAccept(result -> System.out.println("결과: " + result))
            .exceptionally(throwable -> {
                System.err.println("에러: " + throwable.getMessage());
                return null;
            });
    }
}

{% elif language == 'C#' %}
// C# 코드 예제 - .NET 6+ 스타일
using {{ sdk_name | replace('-', '') }};
using Microsoft.Extensions.Logging;
using System.Text.Json;

namespace {{ sdk_name | replace('-', '') }}.Processing;

public class DataProcessor
{
    private readonly ILogger<DataProcessor> _logger;
    private readonly ConfigManager _configManager;
    
    public DataProcessor(ILogger<DataProcessor> logger, ConfigManager configManager)
    {
        _logger = logger;
        _configManager = configManager;
    }
    
    /// <summary>
    /// 데이터를 비동기로 처리합니다
    /// </summary>
    /// <param name="data">처리할 데이터</param>
    /// <param name="config">처리 설정</param>
    /// <param name="cancellationToken">취소 토큰</param>
    /// <returns>처리 결과</returns>
    /// <exception cref="ArgumentException">잘못된 입력 데이터</exception>
    /// <exception cref="ProcessingException">처리 오류</exception>
    public async Task<ProcessingResult> ProcessDataAsync(
        Dictionary<string, object> data, 
        ProcessingConfig config,
        CancellationToken cancellationToken = default)
    {
        var startTime = DateTime.UtcNow;
        
        try
        {
            // 1. 입력 검증
            if (data?.Any() != true)
            {
                throw new ArgumentException("입력 데이터가 비어있습니다", nameof(data));
            }
            
            // 2. 비동기 데이터 처리
            var processedData = new Dictionary<string, object>();
            
            await foreach (var kvp in ProcessDataItemsAsync(data, cancellationToken))
            {
                processedData[kvp.Key] = kvp.Value;
            }
            
            // 3. 결과 생성
            var processingTime = DateTime.UtcNow - startTime;
            var result = new ProcessingResult
            {
                Processed = true,
                Data = processedData,
                ProcessingTimeMs = (long)processingTime.TotalMilliseconds,
                ConfigUsed = config.Name,
                Timestamp = DateTime.UtcNow
            };
            
            _logger.LogInformation("데이터 처리 완료: {ProcessingTime}ms", result.ProcessingTimeMs);
            return result;
        }
        catch (Exception ex) when (!(ex is ArgumentException))
        {
            _logger.LogError(ex, "데이터 처리 실패");
            throw new ProcessingException("처리 중 오류 발생", ex);
        }
    }
    
    private async IAsyncEnumerable<KeyValuePair<string, object>> ProcessDataItemsAsync(
        Dictionary<string, object> data,
        [EnumeratorCancellation] CancellationToken cancellationToken = default)
    {
        foreach (var kvp in data)
        {
            cancellationToken.ThrowIfCancellationRequested();
            
            await Task.Delay(1, cancellationToken); // 비동기 처리 시뮬레이션
            
            var processedValue = kvp.Value switch
            {
                string s when !string.IsNullOrWhiteSpace(s) => s.ToUpperInvariant(),
                int i => i * 2,
                double d => d * 2,
                bool b => !b,
                _ => kvp.Value?.ToString() ?? string.Empty
            };
            
            yield return new KeyValuePair<string, object>(kvp.Key, processedValue);
        }
    }
}

// 사용 예제
public class Program
{
    public static async Task Main(string[] args)
    {
        var logger = LoggerFactory.Create(builder => builder.AddConsole())
            .CreateLogger<DataProcessor>();
        var configManager = new ConfigManager();
        var processor = new DataProcessor(logger, configManager);
        
        var testData = new Dictionary<string, object>
        {
            ["name"] = "john_doe",
            ["age"] = 30,
            ["active"] = true
        };
        
        var config = new ProcessingConfig { Name = "test-config" };
        
        try
        {
            var result = await processor.ProcessDataAsync(testData, config);
            Console.WriteLine($"결과: {JsonSerializer.Serialize(result)}");
        }
        catch (Exception ex)
        {
            Console.WriteLine($"에러: {ex.Message}");
        }
    }
}

{% elif language == 'Go' %}
// Go 코드 예제
package main

import (
    "context"
    "encoding/json"
    "errors"
    "fmt"
    "log"
    "strings"
    "sync"
    "time"
    
    "{{ sdk_name | lower }}"
)

// ProcessingConfig 설정 구조체
type ProcessingConfig struct {
    Name      string            `json:"name"`
    Options   map[string]interface{} `json:"options"`
    CreatedAt time.Time         `json:"created_at"`
}

// ProcessingResult 처리 결과 구조체
type ProcessingResult struct {
    Processed      bool                   `json:"processed"`
    Data          map[string]interface{} `json:"data"`
    ProcessingTime int64                  `json:"processing_time_ms"`
    ConfigUsed    string                 `json:"config_used"`
    Timestamp     time.Time              `json:"timestamp"`
}

// DataProcessor 데이터 처리기
type DataProcessor struct {
    config *ProcessingConfig
    mu     sync.RWMutex
}

// NewDataProcessor 새로운 데이터 처리기 생성
func NewDataProcessor(config *ProcessingConfig) *DataProcessor {
    return &DataProcessor{
        config: config,
    }
}

// ProcessDataAsync 데이터를 비동기로 처리
func (dp *DataProcessor) ProcessDataAsync(
    ctx context.Context, 
    data map[string]interface{},
) (*ProcessingResult, error) {
    startTime := time.Now()
    
    // 1. 입력 검증
    if len(data) == 0 {
        return nil, errors.New("입력 데이터가 비어있습니다")
    }
    
    // 2. 컨텍스트 확인
    select {
    case <-ctx.Done():
        return nil, ctx.Err()
    default:
    }
    
    // 3. 고루틴을 사용한 동시 처리
    processedData := make(map[string]interface{})
    mu := sync.Mutex{}
    var wg sync.WaitGroup
    errorCh := make(chan error, len(data))
    
    for key, value := range data {
        wg.Add(1)
        go func(k string, v interface{}) {
            defer wg.Done()
            
            select {
            case <-ctx.Done():
                errorCh <- ctx.Err()
                return
            default:
            }
            
            // 타입별 처리
            var processed interface{}
            switch val := v.(type) {
            case string:
                if strings.TrimSpace(val) != "" {
                    processed = strings.ToUpper(val)
                } else {
                    processed = ""
                }
            case int:
                processed = val * 2
            case int64:
                processed = val * 2
            case float64:
                processed = val * 2
            case bool:
                processed = !val
            default:
                processed = fmt.Sprintf("%v", v)
            }
            
            mu.Lock()
            processedData[k] = processed
            mu.Unlock()
        }(key, value)
    }
    
    // 모든 고루틴 완료 대기
    wg.Wait()
    close(errorCh)
    
    // 에러 확인
    if len(errorCh) > 0 {
        return nil, <-errorCh
    }
    
    // 4. 결과 생성
    processingTime := time.Since(startTime).Milliseconds()
    result := &ProcessingResult{
        Processed:      true,
        Data:          processedData,
        ProcessingTime: processingTime,
        ConfigUsed:    dp.config.Name,
        Timestamp:     time.Now(),
    }
    
    log.Printf("데이터 처리 완료: %dms", processingTime)
    return result, nil
}

// 사용 예제
func main() {
    config := &ProcessingConfig{
        Name:      "test-config",
        Options:   make(map[string]interface{}),
        CreatedAt: time.Now(),
    }
    
    processor := NewDataProcessor(config)
    
    testData := map[string]interface{}{
        "name":   "john_doe",
        "age":    30,
        "active": true,
        "score":  85.5,
    }
    
    ctx, cancel := context.WithTimeout(context.Background(), 5*time.Second)
    defer cancel()
    
    result, err := processor.ProcessDataAsync(ctx, testData)
    if err != nil {
        log.Printf("에러: %v", err)
        return
    }
    
    resultJSON, _ := json.MarshalIndent(result, "", "  ")
    fmt.Printf("결과: %s\n", resultJSON)
}

{% elif language == 'Rust' %}
// Rust 코드 예제
use {{ sdk_name | replace('-', '_') }}::*;
use serde::{Deserialize, Serialize};
use std::collections::HashMap;
use std::sync::Arc;
use tokio::sync::RwLock;
use anyhow::{Context, Result};
use tracing::{info, error};
use chrono::{DateTime, Utc};

#[derive(Debug, Clone, Serialize, Deserialize)]
pub struct ProcessingConfig {
    pub name: String,
    pub options: HashMap<String, serde_json::Value>,
    pub created_at: DateTime<Utc>,
}

#[derive(Debug, Serialize, Deserialize)]
pub struct ProcessingResult {
    pub processed: bool,
    pub data: HashMap<String, serde_json::Value>,
    pub processing_time_ms: u64,
    pub config_used: String,
    pub timestamp: DateTime<Utc>,
}

#[derive(Debug)]
pub struct DataProcessor {
    config: Arc<RwLock<ProcessingConfig>>,
}

impl DataProcessor {
    /// 새로운 데이터 처리기 생성
    pub fn new(config: ProcessingConfig) -> Self {
        Self {
            config: Arc::new(RwLock::new(config)),
        }
    }
    
    /// 데이터를 비동기로 처리
    pub async fn process_data_async(
        &self,
        data: HashMap<String, serde_json::Value>,
    ) -> Result<ProcessingResult> {
        let start_time = std::time::Instant::now();
        
        // 1. 입력 검증
        if data.is_empty() {
            anyhow::bail!("입력 데이터가 비어있습니다");
        }
        
        // 2. 설정 읽기
        let config = self.config.read().await;
        let config_name = config.name.clone();
        drop(config); // 락 해제
        
        // 3. 병렬 데이터 처리
        let mut processed_data = HashMap::new();
        let mut tasks = Vec::new();
        
        for (key, value) in data.into_iter() {
            let task = tokio::spawn(async move {
                let processed_value = match value {
                    serde_json::Value::String(s) if !s.trim().is_empty() => {
                        serde_json::Value::String(s.to_uppercase())
                    }
                    serde_json::Value::Number(n) => {
                        if let Some(i) = n.as_i64() {
                            serde_json::Value::Number((i * 2).into())
                        } else if let Some(f) = n.as_f64() {
                            serde_json::Value::Number(
                                serde_json::Number::from_f64(f * 2.0)
                                    .unwrap_or_else(|| 0.into())
                            )
                        } else {
                            value
                        }
                    }
                    serde_json::Value::Bool(b) => serde_json::Value::Bool(!b),
                    other => other,
                };
                
                Ok::<(String, serde_json::Value), anyhow::Error>((key, processed_value))
            });
            tasks.push(task);
        }
        
        // 4. 모든 태스크 완료 대기
        for task in tasks {
            match task.await.context("태스크 실행 실패")? {
                Ok((key, value)) => {
                    processed_data.insert(key, value);
                }
                Err(e) => {
                    error!("데이터 처리 실패: {}", e);
                    return Err(e);
                }
            }
        }
        
        // 5. 결과 생성
        let processing_time = start_time.elapsed().as_millis() as u64;
        let result = ProcessingResult {
            processed: true,
            data: processed_data,
            processing_time_ms: processing_time,
            config_used: config_name,
            timestamp: Utc::now(),
        };
        
        info!("데이터 처리 완료: {}ms", processing_time);
        Ok(result)
    }
}

// 사용 예제
#[tokio::main]
async fn main() -> Result<()> {
    tracing_subscriber::init();
    
    let config = ProcessingConfig {
        name: "test-config".to_string(),
        options: HashMap::new(),
        created_at: Utc::now(),
    };
    
    let processor = DataProcessor::new(config);
    
    let mut test_data = HashMap::new();
    test_data.insert("name".to_string(), serde_json::Value::String("john_doe".to_string()));
    test_data.insert("age".to_string(), serde_json::Value::Number(30.into()));
    test_data.insert("active".to_string(), serde_json::Value::Bool(true));
    test_data.insert("score".to_string(), serde_json::Value::Number(
        serde_json::Number::from_f64(85.5).unwrap()
    ));
    
    match processor.process_data_async(test_data).await {
        Ok(result) => {
            let result_json = serde_json::to_string_pretty(&result)?;
            println!("결과: {}", result_json);
        }
        Err(e) => {
            error!("에러: {:?}", e);
        }
    }
    
    Ok(())
}

{% else %}
// {{ language }} 코드 예제
// 완전한 실행 가능한 예제 ({{ language }} 최신 버전 기준)

// 1. 필요한 의존성 및 import
// {{ language }}의 표준 라이브러리와 주요 패키지들 import
{% if language == 'Swift' %}
import Foundation
import {{ sdk_name }}
{% elif language == 'Kotlin' %}
import {{ sdk_name }}.*
import kotlinx.coroutines.*
import kotlinx.serialization.*
{% elif language == 'Ruby' %}
require '{{ sdk_name | replace('-', '_') }}'
require 'json'
require 'logger'
{% elif language == 'PHP' %}
<?php
require_once '{{ sdk_name }}/autoload.php';
use {{ sdk_name | title }}\*;
{% endif %}

// 2. 설정 및 데이터 모델 정의
// {{ language }}의 타입 시스템 특성을 활용한 구조체/클래스 정의

// 3. 핵심 데이터 처리 함수
// {{ language }}의 관용구와 패턴을 활용한 실제 구현
function processData(data, config) {
    // 입력 검증
    if (!data || isEmpty(data)) {
        throw new Error("유효하지 않은 입력 데이터");
    }
    
    // {{ language }} 특화 처리 로직
    const startTime = getCurrentTime();
    
    try {
        // 비동기/동시성 처리 ({{ language }}의 동시성 모델 활용)
        const processedData = processInParallel(data);
        
        // 결과 생성
        const result = {
            processed: true,
            data: processedData,
            processingTime: getCurrentTime() - startTime,
            configUsed: config.name,
            timestamp: getCurrentTimestamp()
        };
        
        return result;
        
    } catch (error) {
        // {{ language }} 특화 에러 처리
        logError("데이터 처리 실패", error);
        throw new ProcessingError("처리 중 오류 발생", error);
    }
}

// 4. 유틸리티 및 헬퍼 함수들
// {{ language }}의 표준 라이브러리 활용

// 5. 실사용 예제
function main() {
    const config = createConfig("test-config");
    const testData = {
        name: "john_doe",
        age: 30,
        active: true
    };
    
    try {
        const result = processData(testData, config);
        console.log("처리 결과:", JSON.stringify(result, null, 2));
    } catch (error) {
        console.error("에러:", error.message);
    }
}

// 6. {{ language }} 특화 패턴
// - 메모리 관리 (필요한 경우)
// - 에러 처리
// - 로깅 및 디버깅
// - 성능 최적화

{% endif %}
```
{% endif %}

### 언어별 특화 요구사항

{% if language == 'Python' %}
#### Python 언어 특성 활용
- **타입 힌트**: 모든 함수와 클래스에 완전한 타입 어노테이션 적용
- **데코레이터**: `@property`, `@classmethod`, `@staticmethod`, `@dataclass` 등 적절한 데코레이터 사용
- **컨텍스트 매니저**: `with` 문과 `__enter__`, `__exit__` 메서드 활용
- **비동기 프로그래밍**: `async`/`await`, `asyncio` 패턴 완전 활용
- **언패킹**: `*args`, `**kwargs`, 구조 분해 할당 등 Python 관용구 사용
- **리스트/딕셔너리 컴프리헨션**: Pythonic한 데이터 처리 패턴 시연
- **매치 케이스**: Python 3.10+ `match-case` 구문 적극 활용
- **패스릿**: `pathlib.Path` 사용으로 현대적 파일 경로 처리

#### Python 생태계 통합
- **가상환경**: venv, conda, poetry 등 환경 관리 방법 제시
- **패키지 관리**: pip, setuptools, requirements.txt 등 의존성 관리
- **테스팅**: pytest, unittest, doctest 등 테스트 프레임워크 활용
- **문서화**: docstring, type hints, sphinx 등 문서화 도구 연동
- **린팅**: black, flake8, mypy, pylint 등 코드 품질 도구 활용
- **성능 프로파일링**: cProfile, line_profiler 등 성능 분석 도구

#### Python 디자인 패턴
- **싱글톤**: `__new__` 메서드나 모듈 레벨 변수 활용
- **팩토리**: 클래스 메서드나 함수를 통한 객체 생성 패턴
- **빌더**: 복잡한 객체 구성을 위한 빌더 패턴 구현
- **옵저버**: 이벤트 기반 프로그래밍 패턴
- **데코레이터 패턴**: 함수와 클래스 데코레이터 활용

#### 에러 처리 특화
- **예외 계층**: 커스텀 예외 클래스 정의 및 상속 구조
- **예외 체이닝**: `raise ... from ...` 구문으로 원인 추적
- **컨텍스트 매니저**: 자원 관리와 에러 처리 통합
- **로깅 통합**: logging 모듈과 예외 처리 연동

{% elif language == 'JavaScript' %}
#### JavaScript 현대 언어 특성 활용
- **ES6+ 문법**: 구조 분해 할당, 템플릿 리터럴, 화살표 함수, 스프레드 연산자 적극 활용
- **비동기 프로그래밍**: `async`/`await`, Promise.all/race/allSettled 패턴 완전 활용
- **모듈 시스템**: ES modules와 CommonJS 호환성 유지, 동적 import() 활용
- **클래스 문법**: ES2022 private fields (#), static methods, getter/setter 활용
- **함수형 프로그래밍**: map, filter, reduce, 고차 함수 패턴 적극 사용
- **이벤트 시스템**: EventEmitter, 커스텀 이벤트, 리스너 패턴 활용
- **심볼과 이터레이터**: Symbol() 활용, 커스텀 이터레이터/제너레이터 구현
- **프록시와 리플렉션**: 메타프로그래밍 패턴 활용

#### JavaScript 생태계 통합
- **패키지 관리**: npm, yarn, pnpm 등 의존성 관리 방법 제시
- **빌드 도구**: Webpack, Vite, Rollup, Parcel 등 번들러 통합 가이드
- **테스팅**: Jest, Mocha, Vitest, Cypress 등 테스트 프레임워크 활용
- **린팅**: ESLint, Prettier, JSHint 등 코드 품질 도구
- **런타임 환경**: Node.js, Deno, Bun 등 다양한 환경 고려
- **타입 체킹**: JSDoc, Flow, 또는 TypeScript 전환 고려사항

#### JavaScript 디자인 패턴
- **모듈 패턴**: IIFE, 네임스페이스, 모듈 시스템 활용
- **팩토리/빌더**: 객체 생성 패턴, 체이닝 메서드
- **옵저버/퍼블리셔**: 이벤트 기반 아키텍처 구현
- **프로미스 패턴**: 체이닝, 에러 핸들링, 병렬 처리
- **미들웨어 패턴**: Express.js 스타일 미들웨어 체인

#### 에러 처리 특화
- **에러 경계**: try-catch-finally, Promise catch, async/await 에러 처리
- **커스텀 에러**: Error 클래스 상속, 구조화된 에러 정보
- **에러 전파**: Promise rejection, 이벤트 기반 에러 처리
- **디버깅**: console 활용, 스택 트레이스, 소스맵 고려

{% elif language == 'TypeScript' %}
#### TypeScript 고급 타입 시스템 활용
- **제네릭**: 제약 조건, 조건부 타입, 맵드 타입, 템플릿 리터럴 타입 완전 활용
- **타입 안전성**: 타입 가드, 타입 단언, 유니온/인터섹션 타입 적절한 사용
- **고급 타입**: Utility Types (Partial, Pick, Omit, Record 등) 적극 활용
- **모듈 시스템**: namespace, module, 선언 병합 패턴 활용
- **데코레이터**: 실험적 데코레이터, 메타데이터 reflection 활용
- **추상화**: 추상 클래스, 인터페이스, 구현/상속 패턴
- **타입 추론**: 자동 타입 추론 활용과 명시적 타입 지정의 균형
- **엄격한 검사**: strict mode, noImplicitAny, noImplicitReturns 등 활용

#### TypeScript 도구 생태계
- **컴파일러**: tsc 설정, tsconfig.json 최적화, 빌드 파이프라인 통합
- **린팅**: ESLint + @typescript-eslint, TSLint 마이그레이션
- **테스팅**: Jest + ts-jest, Vitest, 타입 테스팅 전략
- **번들링**: Webpack, Vite, esbuild와 TypeScript 통합
- **문서화**: TSDoc, TypeScript 타입 정보 기반 문서 생성
- **개발 도구**: VS Code 통합, 인텔리센스, 리팩토링 도구

#### TypeScript 디자인 패턴
- **타입 안전한 팩토리**: 제네릭 팩토리, 빌더 패턴
- **의존성 주입**: 인터페이스 기반 DI, 타입 안전한 컨테이너
- **상태 관리**: 불변성, 타입 안전한 상태 업데이트
- **함수형 프로그래밍**: 타입 안전한 함수 조합, 모나드 패턴
- **옵저버 패턴**: 타입 안전한 이벤트 시스템

#### 타입 안전성 특화
- **런타임 검증**: Zod, io-ts 등 런타임 타입 검증 라이브러리 연동
- **타입 가드**: 사용자 정의 타입 가드, 타입 체킹 함수
- **에러 타입**: 타입 안전한 에러 처리, Result/Either 패턴
- **API 타입**: OpenAPI/GraphQL 스키마와 TypeScript 타입 동기화

{% else %}
#### {{ language }} 언어 특성 활용
- **언어별 관용구**: {{ language }}의 일반적인 코딩 패턴과 베스트 프랙티스 활용
- **표준 라이브러리**: {{ language }} 표준 라이브러리의 핵심 기능들 적극 활용
- **메모리 관리**: {{ language }}의 메모리 관리 방식에 맞는 효율적 코딩
- **동시성 모델**: {{ language }}의 스레딩/비동기 처리 모델 활용
- **에러 처리**: {{ language }} 특유의 예외 처리 메커니즘 완전 활용

#### {{ language }} 생태계 통합
- **패키지 관리**: {{ language }}의 주요 패키지 매니저와 의존성 관리
- **빌드 시스템**: {{ language }}의 표준 빌드 도구와 워크플로우
- **테스팅**: {{ language }}의 주요 테스트 프레임워크 활용
- **문서화**: {{ language }}의 문서화 도구와 표준 형식
- **개발 도구**: IDE 통합, 린터, 포매터 등 개발 환경 최적화

#### {{ language }} 디자인 패턴
- **언어별 패턴**: {{ language }}에서 널리 사용되는 디자인 패턴들
- **아키텍처 패턴**: {{ language }} 생태계의 일반적인 아키텍처 접근법
- **성능 패턴**: {{ language }}의 성능 특성을 고려한 최적화 패턴

{% endif %}

### 참조표 템플릿

#### 설정 옵션 참조표
| 옵션명 | 타입 | 기본값 | 설명 | 예제 |
|--------|------|--------|------|------|
| timeout | int | 30 | API 호출 시간 제한 (초) | `timeout=60` |
| max_retries | int | 3 | 최대 재시도 횟수 | `max_retries=5` |
| log_level | str | "INFO" | 로깅 수준 설정 | `log_level="DEBUG"` |

#### 에러 코드 참조표
| 에러 코드/타입 | 원인 | 해결 방법 | 예제 |
|----------------|------|-----------|------|
| ValueError | 유효하지 않은 입력값 | 입력 데이터 검증 및 수정 | `if not data: raise ValueError("빈 데이터")` |
| TimeoutError | 시간 초과 | timeout 값 증가 또는 재시도 | `timeout=60` |
| ConnectionError | 네트워크 오류 | 연결 상태 확인 및 재시도 로직 | `except ConnectionError: retry()` |

#### API 호환성 매트릭스
| 기능 | 이전 버전 | 현재 버전 | 비고 |
|------|-----------|-----------|------|
| 기본 API | ✅ | ✅ | 안정적 |
| 비동기 지원 | ❌ | ✅ | 새로 추가 |
| 타입 힌트 | ⚠️ | ✅ | 개선됨 |

## 📚 LLMs.txt 표준 파일 생성

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
- Core Modules: #core-modules
- Main Classes: #main-classes
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

Generated with void-breaker v1.0 on {{ current_date }}
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
- 언어: {{ language }}
- SDK 유형: {{ sdk_type }}
- 형식: llms.txt standard v1.0
- 토큰 최적화: 적용됨
- 생성 도구: void-breaker
---

[전체 문서 내용]
```

## ✅ 품질 보증 체크리스트

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
- [ ] 최신 버전({{ version }}) 기준 정보
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

### 언어별 특화 품질
{% if language == 'Python' %}
- [ ] 타입 힌트 완전 적용
- [ ] 비동기 프로그래밍 패턴 포함
- [ ] Python 관용구 적절히 사용
- [ ] 최신 Python 기능 활용 (3.11+)
- [ ] 패키지 생태계 연동 설명
{% elif language == 'JavaScript' %}
- [ ] ES6+ 모던 문법 활용 (구조 분해, 화살표 함수, 템플릿 리터럴)
- [ ] 비동기 패턴 완전 적용 (async/await, Promise.all/race)
- [ ] 함수형 프로그래밍 패턴 포함 (map, filter, reduce)
- [ ] 이벤트 기반 아키텍처 시연
- [ ] 모듈 시스템 호환성 (CommonJS + ES modules)
- [ ] 에러 처리 체계 완비 (try-catch, Promise rejection)
- [ ] Node.js 생태계 도구 연동 (npm, Jest, ESLint)
{% elif language == 'TypeScript' %}
- [ ] 고급 타입 시스템 완전 활용 (제네릭, 유니온, 매핑)
- [ ] 타입 안전성 보장 (타입 가드, strict mode)
- [ ] 인터페이스와 추상 클래스 적절한 사용
- [ ] 컴파일 타임 타입 검증 포함
- [ ] 런타임 타입 검증 패턴 시연
- [ ] TypeScript 도구 체인 통합 (tsc, ESLint, Jest)
- [ ] 최신 TypeScript 기능 활용 (4.9+)
{% else %}
- [ ] {{ language }} 언어 특성 완전 반영
- [ ] {{ language }} 생태계 도구 연동
- [ ] {{ language }} 관용구 및 베스트 프랙티스 적용
- [ ] {{ language }} 최신 버전 기능 활용
- [ ] {{ language }} 표준 라이브러리 적절한 사용
{% endif %}

## 📚 참고 자료 우선순위

1. **공식 문서** (가장 높은 우선순위)
2. **GitHub 저장소** (README, examples, docs 폴더)
3. **API 레퍼런스** 
4. **커뮤니티 리소스** (Stack Overflow, Discord, Forums)
5. **실제 프로젝트 사례**

## 🎯 성공 지표

### 문서 품질 목표
- **완성도**: 95% 이상 (모든 핵심 기능 커버)
- **정확성**: 100% (검증된 정보만 포함)
- **실행 가능성**: 100% (모든 코드 예제 실행 가능)
- **LLM 최적화**: 90% 이상 (토큰 효율성, 검색성)

### 사용자 만족도 목표
- **이해 용이성**: 초보자도 90% 이상 이해 가능
- **실무 적용성**: 프로덕션 환경에서 즉시 활용 가능
- **문제 해결력**: 일반적인 문제 80% 이상 해결 가능

---

이 요구사항에 따라 {{ sdk_name }} {{ version }}의 완전하고 실용적인 LLM 최적화 문서를 작성해주세요.
```