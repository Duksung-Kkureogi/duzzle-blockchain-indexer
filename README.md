# Duzzle 블록체인 인덱서 - 블록체인 트랜잭션 모니터링 및 NFT 상태 관리 서비스

## 주요 기능
1. 블록체인 이벤트/트랜잭션 모니터링
   - 5초 간격으로 새로운 트랜잭션 확인
   - RPC `eth_getLogs` 요청 처리

2. 필요한 데이터 필터링 (Duzzle 관련 컨트랙트의 이벤트만)
   - NFT 컨트랙트 (Puzzle Piece, Blueprint Item, Material Item)
   - Transfer 이벤트 처리

3. DB에 저장 
   - 트랜잭션 로그 저장
   - 중복 처리 방지
   - 배치 처리

4. NFT 보유 현황 같은 상태 업데이트
   - NFT 소유자 정보 갱신
   - `puzzle_piece`, `blueprint_item`, `material_item` 테이블 관리

## 기술 스택
- Node.js
- PostgreSQL
- TypeScript
- AWS Lambda
- Serverless Framework

