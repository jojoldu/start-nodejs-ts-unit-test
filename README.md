# Unit Test 

```bash
# 새 폴더 생성 및 초기화
mkdir my-ts-jest-project
cd my-ts-jest-project

# package.json 생성
npm init -y

# TypeScript 설치
npm install --save-dev typescript
```


```bash
npx tsc --init
```

```bash
npm install --save-dev jest @swc/jest @types/jest
```

```bash
// jest.config.js
module.exports = {
  // 테스트 환경 설정 (node, jsdom 등)
  testEnvironment: 'node',

  // Jest가 소스 코드를 어떻게 변환할지 설정
  transform: {
    '^.+\\.(t|j)sx?$': ['@swc/jest'],
  },

  testMatch: [
    '**/__tests__/**/*.(test|spec).(ts|tsx|js)',
    '**/?(*.)+(test|spec).(ts|tsx|js)',
  ],

  // 커버리지 옵션 등 추가 설정 가능
  collectCoverage: true,
  coverageDirectory: 'coverage',
};
```
