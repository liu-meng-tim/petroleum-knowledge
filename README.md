<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>石化業技術問題彙整</title>
  <style>
    body {
      font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
      background-color: #f8f9fa;
      color: #212529;
      margin: 0;
      padding: 2rem;
    }
    header {
      background-color: #1c1f23;
      color: #ffffff;
      padding: 2rem;
      text-align: center;
    }
    h1 {
      margin: 0;
      font-size: 2.5rem;
      letter-spacing: 1px;
    }
    section {
      background-color: #ffffff;
      border-radius: 12px;
      box-shadow: 0 0 12px rgba(0, 0, 0, 0.1);
      padding: 2rem;
      margin-bottom: 2rem;
      transition: all 0.3s ease;
    }
    h2 {
      border-bottom: 2px solid #007bff;
      padding-bottom: 0.5rem;
      margin-bottom: 1rem;
      color: #007bff;
      cursor: pointer;
    }
    ul {
      line-height: 1.8;
      padding-left: 1.5rem;
    }
    code {
      background-color: #e9ecef;
      padding: 0.2rem 0.4rem;
      border-radius: 4px;
    }
    .logo {
      max-width: 160px;
      margin: 1rem auto;
      display: block;
    }
    .intro {
      text-align: center;
      margin-top: 1rem;
      font-size: 1.1rem;
    }
    .collapsible {
      overflow: hidden;
      max-height: 1000px;
      transition: max-height 0.3s ease, opacity 0.3s ease;
      opacity: 1;
    }
    .collapsed .collapsible {
      max-height: 0;
      padding: 0;
      opacity: 0;
    }
  </style>
</head>
<body>
  <header>
    <img src="https://upload.wikimedia.org/wikipedia/zh/f/f0/Hotai_Motor_logo.svg" alt="Hotai Logo" class="logo">
    <h1>石化業技術問題彙整</h1>
    <p class="intro">由和泰集團內部技術彙編支援整理</p>
    <p>主題分類：名詞解釋、管道、維修、腐蝕、警報、防爆、火災防護</p>
  </header>

  <section>
    <h2 onclick="toggleSection(this)">名詞解釋</h2>
    <div class="collapsible">
      <ul>
        <li><strong>PSV</strong>（Pressure Safety Valve）：壓力安全閥，保護設備不受過壓損害。</li>
        <li><strong>PT/PI</strong>：壓力變送器（PT）與壓力指示器（PI），用於監控系統壓力。</li>
        <li><strong>delta P</strong>：壓差，用來判斷設備或管線內是否有堵塞或洩漏。</li>
        <li><strong>MOC</strong>（Management of Change）：變更管理制度，確保工程改動受到評估與控管。</li>
        <li><strong>HQ / MEHQ</strong>：化學抑制劑，常見於防止自聚反應的儲槽系統中。</li>
      </ul>
    </div>
  </section>

  <section>
    <h2 onclick="toggleSection(this)">管道系統</h2>
    <div class="collapsible">
      <ul>
        <li>氣體或液體輸送過程會產生靜電，當電荷累積到一定程度會擊穿空氣產生火花，具潛在火災風險。</li>
        <li>鋼製管線常配有壓力與流量監測，若洩漏時會利用氮氣置換清空。</li>
        <li>考慮使用<code>delta P</code>（壓差）進行洩漏判斷，3%偏差即會觸發關閉。</li>
        <li>管線識別符號：<code>PI</code>（壓力指示）、<code>PT</code>（壓力變送器）、<code>PCY</code>（壓力控制迴路）等。</li>
      </ul>
      <p><strong>參考標準：</strong> ANSI/ISA 5.1、API 14C、ASME B31.3</p>
    </div>
  </section>

  <section>
    <h2 onclick="toggleSection(this)">維修與安全閥</h2>
    <div class="collapsible">
      <ul>
        <li>PSV（壓力安全閥）需定期校驗，校驗標準包括POP值偏差±3%、關閉壓差等。</li>
        <li>設置隔離閥時，應保持常開狀態，確保PSV未被誤關閉。</li>
        <li>異動作業如檢修，應遵循MOC（變更管理）制度，臨時性繞接亦需納入紀錄。</li>
      </ul>
      <p><strong>參考標準：</strong> ASME BPVC Sec VIII, API 576, API 570, OSHA PSM</p>
    </div>
  </section>

  <section>
    <h2 onclick="toggleSection(this)">腐蝕與材料防護</h2>
    <div class="collapsible">
      <ul>
        <li>Trunnion 支撐等構件建議設置排水孔，避免積水造成點蝕。</li>
        <li>儲槽防自聚措施包括在線溫度監測及使用抑制劑（如HQ, MEHQ）。</li>
        <li>儲槽內部或管線包覆建議使用具防火阻燃等級的保溫材料。</li>
      </ul>
      <p><strong>參考標準：</strong> NACE MR0175、API 653、API RP 939C</p>
    </div>
  </section>

  <section>
    <h2 onclick="toggleSection(this)">警報系統</h2>
    <div class="collapsible">
      <ul>
        <li>應定期測試聲光警報器功能，並記錄測試週期與結果。</li>
        <li>警報邏輯設計應避免誤報與漏報，例如需設下限與上限警報。</li>
        <li>關鍵警報建議導入至DCS或SIS系統，並設有確認機制。</li>
      </ul>
      <p><strong>參考標準：</strong> IEC 61511、API RP 554、ISA 18.2</p>
    </div>
  </section>

  <section>
    <h2 onclick="toggleSection(this)">防爆設計</h2>
    <div class="collapsible">
      <ul>
        <li>設備與電氣元件應符合防爆等級，如Ex d、Ex e、Ex i等。</li>
        <li>防爆區劃建議依據氣體類別與通風情況進行分級。</li>
        <li>操作區可加裝正壓系統或氣體監測器進行主動保護。</li>
      </ul>
      <p><strong>參考標準：</strong> IEC 60079 系列、NFPA 70、CNS 3376</p>
    </div>
  </section>

  <section>
    <h2 onclick="toggleSection(this)">火災防護</h2>
    <div class="collapsible">
      <ul>
        <li>應設置自動灑水系統與泡沫滅火系統，對於儲槽建議使用固定泡沫裝置。</li>
        <li>火災特徵分析可透過天花板V型損壞、煙垢形狀與玻璃破裂方式判斷起火源。</li>
        <li>逃生動線應明確標示，並考量疏散安全時間（SET）與NFPA建議值。</li>
      </ul>
      <p><strong>參考標準：</strong> NFPA 30、NFPA 11、NFPA 72、ISO 13702</p>
    </div>
  </section>

  <script>
    function toggleSection(header) {
      const section = header.parentElement;
      section.classList.toggle('collapsed');
    }
  </script>
</body>
</html>
