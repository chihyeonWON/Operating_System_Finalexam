# Operating_System_Finalexam
운영체제 기말고사 정리입니다.
```
7번. 외부 단편화의 크기를 구하는 문제 (External Fragmentation)
50 + 120 = 170 (분할 크기 < 요청 작업 크기)

9번. 페이지 기억장치 할당기법에서, 한 페이지의 크기가 512바이트이고 페이지 번호는 0부터 시작한다면,
논리적인 주소 1224번지는 어디로 변환되는가?

0~512 0페이지
512~1024 1페이지
1024~1536 2페이지 
offset = 1224-1024 = 200

2페이지, offset = 200
```
## External Fragmentation
![image](https://github.com/chihyeonWON/Operating_System_Finalexam/assets/58906858/393e6a9f-29f6-4f6e-b4bc-864ba50b7315)
![image](https://github.com/chihyeonWON/Operating_System_Finalexam/assets/58906858/03ac06a0-593e-4209-89f1-613f283bcbfd)

## Segementation Logical Address to Physical Address
![image](https://github.com/chihyeonWON/Operating_System_Finalexam/assets/58906858/28d27f7f-00b0-4914-b686-26bd7e396042)
![image](https://github.com/chihyeonWON/Operating_System_Finalexam/assets/58906858/68503b24-6511-407a-ad3e-9582fdcc5d0e)

## FIFO Algorithm
![image](https://github.com/chihyeonWON/Operating_System_Finalexam/assets/58906858/486abdc4-d641-463f-b7ce-0bcf9533cd4a)

## LRU Algorithm
![image](https://github.com/chihyeonWON/Operating_System_Finalexam/assets/58906858/c54e34aa-b3c7-41bf-88f0-43dc31a23079)

## Working Set
![image](https://github.com/chihyeonWON/Operating_System_Finalexam/assets/58906858/a0abd111-f0c9-4561-b7cc-33c0bba5b4d5)

```
선입 선처리 FCFS 스케줄링은 입출력 요청들을 도착한 순서대로 처리하는 가장 간단한 방법으로 헤드의 이동 거리가 길다.

최소 탐색 시간 우선 SSTF 스케줄링은 헤드의 현재 위치를 기준으로, 원하는 트랙(실린더)이 가장 가까운 입출력 요청을 먼저
처리함으로써 헤드의 이동을 최소화 시킨다. 이 방법에서는 멀리 떨어진 요청들은 처리가 지연되는 기아 상태가 나타날 수 있다.

스캔(SCAN) 스케줄링은 최소 탐색 시간 우선 스케줄링의 기아 상태를 예방하여 공평성을 향상시키기 위해
헤드를 양 쪽 끝까지 지그재그 방식으로 번갈아 이동시키며 중간에 위치하는 요청들을 처리한다.
그러나 양쪽 끝 부분과 가운데 부분의 트랙들에 대한 처리 주기가 달라 공평성의 한계가 있다.

순환 스캔(S-SCAN) 스케줄링은 스캔 스케줄링의 트랙 위치에 따른 처리 주기의 편차를 제거하기 위해
헤드가 한 쪽 끝에 도달하면 다시 원래 처음으로 되돌아가 동일한 방향의 스캔을 계속하도록 한다.

미리보기 스캔 (LOOK) 스케줄링은 스캔 스케줄링과 동일하나 진행 방향의 전방에 더 이상의 요청이 존재하지 않으면
즉시 방향을 바꾸어 헤드 이동 거리를 좀 더 줄이지만 공평성 문제는 여전히 존재한다.

미리보기 순환 스캔(S-LOOK) 스케줄링은 순환 스캔 스케줄링과 동일하나 진행 방향의 전방에 더 이상의 요청이
존재하지 않으면 즉시 헤드를 원래의 첫 부분으로 되돌아가도록 한다.
```
