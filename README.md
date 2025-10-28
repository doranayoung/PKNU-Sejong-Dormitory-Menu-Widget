<div align="center" style="font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,'Noto Sans KR',Arial,sans-serif;">
  <h1 style="margin:0.4rem 0;">PKNU 세종기숙사 식단 위젯</h1>
  <p style="margin:0.2rem 0;font-size:0.95rem;color:#555;">
    iOS Scriptable 기반 자동 식단 파싱 위젯
  </p>
  <p style="margin:0.6rem 0;">
    <span style="display:inline-block;background:#111;color:#fff;border-radius:8px;padding:4px 10px;font-size:12px;">Scriptable</span>
    <span style="display:inline-block;background:#eef2ff;color:#3730a3;border-radius:8px;padding:4px 10px;font-size:12px;">세종 식당 전용 (BID=foodE)</span>
    <span style="display:inline-block;background:#f1f5f9;color:#0f172a;border-radius:8px;padding:4px 10px;font-size:12px;">dormitory.pknu.ac.kr 기반</span>
  </p>
  <hr style="border:none;height:1px;background:#e5e7eb;margin:14px 0;width:92%;">
</div>

<div style="max-width:860px;margin:0 auto;line-height:1.65;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,'Noto Sans KR',Arial,sans-serif;color:#0f172a;">

  <h2>📌 개요</h2>
  <p>
    PKNU(부경대학교) 세종캠퍼스 기숙사 식단을 <strong>Scriptable 위젯</strong>으로
    홈 화면에서 바로 확인할 수 있는 프로젝트입니다.
    주차별 AJAX 호출까지 자동 처리하여, 공지 페이지에 오늘 날짜가 없더라도
    백업 소스에서 식단을 복구해줍니다.
  </p>

  <h2>✨ 주요 기능</h2>
  <ul>
    <li><strong>오늘 날짜 자동 탐지</strong> (다양한 형식 대응: 10/27, 10.27, 10-27, 10월27일 ...)</li>
    <li><strong>현재 주차에 미표기 시 AJAX 재요청</strong> → 백업 파싱</li>
    <li>조식·중식·석식을 <strong>한 줄 메뉴</strong>로 깔끔 정리</li>
    <li>빈 셀/주말/미운영은 <code>제공 없음</code>으로 일괄 처리</li>
    <li>Scriptable 위젯 UI로 iOS 홈화면에서 즉시 확인 가능</li>
  </ul>

  <h2>🧠 동작 방식</h2>
  <ol>
    <li>공지 페이지 HTML을 읽어와 오늘 날짜가 포함된 열을 탐색</li>
    <li>tbody에서 조식·중식·석식 행만 추출 후 태그 제거 및 1줄 정제</li>
    <li>없거나 비어 있을 경우 AJAX 페이지에서 다른 주차를 순차 탐색</li>
    <li>최종적으로 위젯에 식단 렌더링</li>
  </ol>

  <h2>📱 사용 방법</h2>
  <ol>
    <li>iOS 앱스토어에서 <strong>Scriptable</strong> 설치</li>
    <li>이 레포지토리의 스크립트 코드 복사</li>
    <li>Scriptable에 새 스크립트 생성 → 붙여넣기</li>
    <li>홈 화면에 Scriptable 위젯 추가 후 스크립트 연결</li>
  </ol>

  <h2>⚙️ 대상 식당</h2>
  <table style="border-collapse:collapse;width:100%;font-size:0.95rem;">
    <thead>
      <tr>
        <th style="text-align:left;border-bottom:1px solid #e5e7eb;padding:6px 8px;">항목</th>
        <th style="text-align:left;border-bottom:1px solid #e5e7eb;padding:6px 8px;">값</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding:6px 8px;border-bottom:1px solid #f1f5f9;">캠퍼스</td>
        <td style="padding:6px 8px;border-bottom:1px solid #f1f5f9;">세종</td>
      </tr>
      <tr>
        <td style="padding:6px 8px;border-bottom:1px solid #f1f5f9;">bid</td>
        <td style="padding:6px 8px;border-bottom:1px solid #f1f5f9;"><code>foodE</code></td>
      </tr>
      <tr>
        <td style="padding:6px 8px;border-bottom:1px solid #f1f5f9;">출처</td>
        <td style="padding:6px 8px;border-bottom:1px solid #f1f5f9;">https://dormitory.pknu.ac.kr</td>
      </tr>
    </tbody>
  </table>

  <h2>⚠️ 참고</h2>
  <ul>
    <li>GitHub는 JavaScript 실행을 지원하지 않음 (위젯은 Scriptable에서만 동작)</li>
    <li>학교 홈페이지 마크업 변경 시 파싱 로직 업데이트 필요</li>
  </ul>

  <h2>🧾 제작</h2>
  <p>ChatGPT × Doranayoung × Gemini</p>
</div>
