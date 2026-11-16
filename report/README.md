# Sling Scroll 중간 보고서

요청한 한글 Markdown 원고는 [slingscroll-half-report.ko.md](slingscroll-half-report.ko.md)입니다. 같은 본문을 Overleaf에서 조판할 수 있도록 [main.tex](main.tex)와 [references.bib](references.bib)를 함께 제공합니다. 저자와 소속은 요청에 따라 비워 두었습니다.

## Overleaf에서 사용

1. `main.tex`와 `references.bib`를 같은 Overleaf 프로젝트에 업로드합니다. 제공된 ZIP을 새 프로젝트로 업로드해도 됩니다.
2. 메인 문서를 `main.tex`, 컴파일러를 **XeLaTeX**로 설정합니다.
3. 필요할 때 `\author{}`에 저자를 입력하고 `\affiliation{...}`을 추가합니다.
4. PDF를 다시 컴파일하고 본문이 4쪽 이내인지 확인한 뒤 다운로드합니다. 저자 정보나 그림을 추가하면 분량이 바뀔 수 있습니다.

Markdown은 검토·수정용 원고이고, Overleaf의 컴파일 대상은 LaTeX 파일입니다. 두 파일을 함께 제공했으므로 본문을 수정할 때에는 해당 내용을 양쪽에 반영해야 합니다.

## 적용한 형식과 제출 조건

- ACM 단일 열: `\documentclass[manuscript,review,nonacm]{acmart}`. `review`는 행 번호를 표시하고, `nonacm`은 수업 보고서에 해당하지 않는 ACM 출판 문구를 생략합니다.
- 필수 내용: Abstract, Introduction, Related Work, Proposed System, Evaluation, Results, Discussion, Conclusion.
- 본문은 참고문헌을 제외하고 4쪽 이내로 작성합니다. 참고문헌은 본문 뒤에 이어 배치하며 별도의 표지는 없습니다.
- 제출 파일 형식: PDF.
- 제출 위치: Blackboard의 Half Report 과제.
- 마감: **2026년 11월 22일 오후 11시 59분(KST)**.

형식은 [CHI 2027 공식 안내](https://chi2027.acm.org/chi-publication-formats/)의 초기 제출용 단일 열 설정을 따릅니다. 한글은 [Overleaf의 한글 조판 안내](https://www.overleaf.com/learn/latex/Korean)에 따라 XeLaTeX와 Noto CJK 글꼴을 사용합니다. 학술대회 출판이 아닌 수업 중간 보고서이므로 DOI·ISBN·저작권 문구는 표시하지 않습니다.

## 내용 정리 기준

원문 초안과 현재 코드가 다른 부분은 구현을 기준으로 정리했습니다. 길게 누르기 대기 시간 없이 시작하고, 세로 10 px 이내에서 취소하며, 선형항과 3차항을 결합해 이동량을 계산합니다. 일반 Flick과 다중 선택은 현재 구현된 기능으로 서술하지 않았습니다.

Results는 계산 로직·콘텐츠·QR 자동 테스트와 구현 진척만 보고합니다. 사용자 실험은 미수행 상태이며 18명 비교 실험은 계획입니다. 기법 블록 후 측정하는 Physical Demand를 거리별 피로나 장기적 피로로 해석하지 않았고, 실험 자세와 맞지 않는 한 손 엄지 조작의 편의성 주장도 제외했습니다.

참고문헌은 SDAZ, AKS, Zoofing의 원 논문과 NASA-TLX 공식 자료를 확인했습니다. AKS의 저자명은 Jongwook Jeong, Neunghoe Kim, Hoh Peter In으로 정리했습니다. 초안의 검정력 수치는 해당 분석 계획에서 확정할 근거가 부족해 제외했습니다.

## 조판 검증

2026년 11월 16일 로컬 XeTeX 기반 조판으로 **참고문헌을 포함해 총 4쪽**임을 확인했습니다. 네 페이지를 이미지로 렌더링해 한글·수식·참고문헌과 페이지 경계를 검토했으며, 누락 글자·본문 넘침·미해결 인용은 없었습니다. 검토용 PDF는 프로젝트의 `output/pdf/slingscroll-half-report.ko.pdf`에 있습니다.

이 검증은 저자와 소속을 비워 둔 현재 원고 기준입니다. Overleaf의 TeX Live 버전이나 추후 내용 변경에 따라 줄바꿈이 달라질 수 있으므로 제출 전 최종 PDF의 분량을 다시 확인하세요.
