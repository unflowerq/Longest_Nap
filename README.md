# Longest_Nap

낮잠 오래 자기(Longest Nap)

교수가 낮잠 자려고 하는데, 10:00 ~ 18:00 에 스케쥴이 없을 때, 제일 긴 낮잠을 자고 싶어한다. 프로그래머인 당신에게 요구 하고 있다. 

input
- 임의 개수의 테스트 케이스가 입력되며 각 테스트 케이스가 하루를 나타냄
- 각 테스트 케이스의 첫번째 줄에는 100 이하의 양의 정수 s가 들어있으며 이 수는 그 날 미리 잡혀있는 약속의 개수를 나타냄
- 그 다음 줄부터 s개의 줄에는 time1 time2 약속 형식으로 잡혀있는 약속이 입력되며 time1은 시작 시각, time2는 끝나는 시각을 나타. 모든 시각은 hh:mm 형식으로 주어짐. 끝나는 시각은 반드시 시작 시간보다 뒤며 시작 시간과 스페이스 한 개로 구분
- 모든 시각은 10:00 이후, 18:00 이전으로 주어. 따라서 결과도 반드시 이 시간 내에 있어야 함. 즉 10:00 전에 낮잠을 잘 수 없고 18::00 넘어서까지 낮잠을 잘 수도 없다.
- 약속은 임의의 문자를 열거한 형태로 주어지는데 반드시 한 줄에 입력되어야 한다. 각 줄의 길이는 255글자를 넘지 않으며 10<=hh<=18, 0<=mm<60 이라고 가정할 수 있다. 하지만 약속이 어떤 정해진 순서대로 입려된다고 가정할 수 없고 파일 종료 문자가 나올 때까지 입력을 모두 읽어야 한다.

output
- Day #d: the longest nap starts at hh:mm and will last for [H hours and] M minutes.
- d는 테스트 케이스 번호(1부터 시작)
- hh:mm은 낮잠을 자기 시작하는 시각, 총 시간이 60분 미만이면 분만 출력
- 낮잠을 잘 수 있는 시간은 시작 시간과 끝나는 시각의 차로 계산
- 가장 길게 낮잠을 잘 수 있는 시간이 여러 개 있으며 그 중 가장 빨리 시작하는 것을 출력
- 교수가 하루 종일 바쁜 경우는 없다고 가정

input example
- 4
- 10:00 12:00 Lectures
- 12:00 13:00 Lunch, like always.
- 13:00 15:00 Boring Lectures...
- 15:30 17:45 Reading
- 4
- 10:00 12:00 Lectures
- 12:00 13:00 Lunch, just lunch.
- 13:00 15:00 Lectures, lectures... oh, no!
- 16:45 17:45 Reading (to be or not to be?)
- 4
- 10:00 12:00 Lectures, as everday.
- 12:00 13:00 Lunch, again!!!
- 13:00 15:00 Lectures, more lectures!
- 15:30 17:15 Reading (I love reading, but should I schedule it?)
- 1
- 12:00 13:00 I love lunch! Have you ever noticed it? :)

output example
- Day #1: the longest nap starts at 15:00 and will last for 30 minutes.
- Day #2: the longest nap starts at 15:00 and will last for 1 hours and 45 minutes.
- Day #3: the longest nap starts at 17:15 and will last for 45 minutes.
- Day #4: the longest nap starts at 13:00 and will last for 5 hours and 0 minutes.
