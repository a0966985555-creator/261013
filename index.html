<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <!-- 設定行動裝置與各種螢幕的響應式視窗縮放比例 -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>高中英文選擇題測驗系統</title>
  
  <!-- 載入 Google Fonts 字型 (中文: LXGW WenKai TC, 英文: Fraunces) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,100..900;1,9..144,100..900&family=LXGW+WenKai+TC&display=swap" rel="stylesheet">
  
  <!-- 載入 p5.js 核心函式庫 -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.0/p5.min.js"></script>

  <style>
    /* 清除預設邊距並設定背景與字型樣式 */
    html, body {
      margin: 0;
      padding: 0;
      overflow: hidden;
      background-color: #f0f4f8;
      font-family: 'LXGW WenKai TC', 'Fraunces', serif;
    }
    canvas {
      display: block;
    }
  </style>
</head>
<body>

  <script>
    const rawQuestionBank = [
      {
        question: "Due to heavy traffic, we had to ______ our trip to the countryside.",
        options: ["A) postpone", "B) accelerate", "C) establish", "D) conquer"],
        answer: 0,
        explanation: "postpone 意為「延期」。句意：由於交通壅塞，我們不得不延後鄉村之旅。"
      },
      {
        question: "The doctor advised him to adopt a healthy diet and exercise ______.",
        options: ["A) rarely", "B) regularly", "C) severely", "D) desperately"],
        answer: 1,
        explanation: "regularly 意為「規律地」。句意：醫生建議他採取健康飲食並規律運動。"
      },
      {
        question: "She has a strong ______ for classical music and plays the violin well.",
        options: ["A) objection", "B) passion", "C) threat", "D) distance"],
        answer: 1,
        explanation: "passion 意為「熱情」。句意：她對古典音樂有強烈的熱情，且小提琴彈得很好。"
      },
      {
        question: "The weather was so cold that the water in the pond had ______.",
        options: ["A) melted", "B) frozen", "C) boiled", "D) floated"],
        answer: 1,
        explanation: "frozen 意為「結冰」。句意：天氣太冷了，以至於池塘裡的水都結冰了。"
      },
      {
        question: "It is essential to ______ water when living in a drought-prone area.",
        options: ["A) consume", "B) pollute", "C) conserve", "D) ignore"],
        answer: 2,
        explanation: "conserve 意為「節約/保護」。句意：住在易乾旱地區，節約用水非常重要。"
      },
      {
        question: "The company decided to ______ a new marketing strategy to boost sales.",
        options: ["A) abandon", "B) implement", "C) hesitate", "D) criticize"],
        answer: 1,
        explanation: "implement 意為「實施、執行」。句意：公司決定實施一項新的行銷策略來促進銷售。"
      },
      {
        question: "Reading books regularly can greatly ______ your vocabulary and knowledge.",
        options: ["A) expand", "B) shrink", "C) decrease", "D) ruin"],
        answer: 0,
        explanation: "expand 意為「擴大、增加」。句意：定期閱讀書籍可以大大擴充你的詞彙量和知識。"
      },
      {
        question: "He showed great ______ by saving the child from the burning building.",
        options: ["A) cowardice", "B) courage", "C) laziness", "D) sadness"],
        answer: 1,
        explanation: "courage 意為「勇氣」。句意：他從燃燒的建築物中救出小孩，展現了極大的勇氣。"
      },
      {
        question: "Scientists are trying to ______ the causes of this mysterious disease.",
        options: ["A) ignore", "B) investigate", "C) complicate", "D) confuse"],
        answer: 1,
        explanation: "investigate 意為「調查」。句意：科學家們正試圖調查這種神祕疾病的起因。"
      },
      {
        question: "Please make sure to ______ all your files before turning off the computer.",
        options: ["A) delete", "B) save", "C) lose", "D) scatter"],
        answer: 1,
        explanation: "save 意為「儲存」。句意：關閉電腦前，請務必儲存所有檔案。"
      }
    ];

    let quizData = [];         // 每次隨機抽出的 5 題測驗陣列
    let currentQuestion = 0;   // 目前作答進度 (0 到 4)
    let score = 0;             // 答對題數累積
    let selectedOption = -1;   // 使用者點選的選項索引
    let answered = false;      // 判斷當前題目是否已作答

    function setup() {
      // 建立鋪滿整個視窗畫布
      createCanvas(windowWidth, windowHeight);
      // 隨機抽選 5 題
      initQuiz();
    }

    // 洗牌並抽出 5 題的函數
    function initQuiz() {
      let shuffled = [...rawQuestionBank];
      
      // Fisher-Yates 隨機排序演算法
      for (let i = shuffled.length - 1; i > 0; i--) {
        let j = floor(random(i + 1));
        let temp = shuffled[i];
        shuffled[i] = shuffled[j];
        shuffled[j] = temp;
      }
      
      quizData = shuffled.slice(0, 5);
      currentQuestion = 0;
      score = 0;
      selectedOption = -1;
      answered = false;
    }

    function draw() {
      // 繪製溫和的背景色
      background(242, 246, 250);

      // 檢查是否仍在測驗中，否則進入結算畫面
      if (currentQuestion < quizData.length) {
        drawQuizScreen();
      } else {
        drawResultScreen();
      }
    }

    function drawQuizScreen() {
      let q = quizData[currentQuestion];

      // 計算響應式卡片寬高與置中座標
      let cardWidth = constrain(width * 0.9, 300, 720);
      let cardHeight = constrain(height * 0.88, 500, 660);
      let cardX = width / 2 - cardWidth / 2;
      let cardY = height / 2 - cardHeight / 2;

      // 繪製卡片柔和陰影
      noStroke();
      fill(205, 215, 230, 100);
      rect(cardX + 6, cardY + 6, cardWidth, cardHeight, 16);

      // 繪製白色卡片主體
      fill(255);
      stroke(218, 226, 236);
      strokeWeight(2);
      rect(cardX, cardY, cardWidth, cardHeight, 16);

      // 繪製進度條底框
      noStroke();
      fill(230, 238, 246);
      rect(cardX + 24, cardY + 24, cardWidth - 48, 10, 5);

      // 繪製進度條填滿部分
      fill(74, 144, 226);
      let progressWidth = map(currentQuestion + 1, 1, quizData.length, 0, cardWidth - 48);
      rect(cardX + 24, cardY + 24, progressWidth, 10, 5);

      // 繪製題號提示文字
      fill(120);
      textFont('LXGW WenKai TC, sans-serif');
      textSize(width < 500 ? 12 : 14);
      textAlign(LEFT, CENTER);
      text("QUESTION " + (currentQuestion + 1) + " OF " + quizData.length, cardX + 24, cardY + 56);

      // 繪製英文題目本文
      fill(30);
      textFont('Fraunces, LXGW WenKai TC, serif');
      textSize(width < 500 ? 16 : 19);
      textWrap(WORD);
      text(q.question, cardX + 24, cardY + 95, cardWidth - 48);

      // 選項按鈕排版參數
      let optionStartY = cardY + 165;
      let optionHeight = width < 500 ? 44 : 50;
      let optionSpacing = width < 500 ? 10 : 14;

      for (let i = 0; i < q.options.length; i++) {
        let optY = optionStartY + i * (optionHeight + optionSpacing);
        
        // 偵測滑鼠懸停
        let isHover = mouseX > cardX + 24 && mouseX < cardX + cardWidth - 24 &&
                      mouseY > optY && mouseY < optY + optionHeight;

        // 預設樣式
        fill(250, 252, 255);
        stroke(215, 225, 238);
        strokeWeight(1.5);

        // 作答後的顏色標示
        if (answered) {
          if (i === q.answer) {
            // 正確選項強制填入規定之 #dde5b6 背景顏色
            fill(221, 229, 182); // #dde5b6 對應之 RGB
            stroke(175, 190, 130);
            strokeWeight(2);
          } else if (i === selectedOption && selectedOption !== q.answer) {
            // 點錯的選項顯示淺紅色
            fill(255, 220, 220);
            stroke(230, 150, 150);
            strokeWeight(2);
          }
        } else if (isHover) {
          // 未作答時懸停高亮
          fill(235, 243, 255);
          stroke(100, 160, 235);
        }

        // 繪製選項卡片
        rect(cardX + 24, optY, cardWidth - 48, optionHeight, 10);

        // 繪製選項文字
        fill(40);
        textFont('Fraunces, LXGW WenKai TC, serif');
        textSize(width < 500 ? 14 : 16);
        textAlign(LEFT, CENTER);
        text(q.options[i], cardX + 42, optY + optionHeight / 2);
      }

      if (answered) {
        fill(80, 95, 110);
        textFont('LXGW WenKai TC, sans-serif');
        textSize(width < 500 ? 13 : 15);
        textAlign(LEFT, CENTER);
        
        let explanationY = optionStartY + 4 * (optionHeight + optionSpacing) + 10;
        text("解析：" + q.explanation, cardX + 24, explanationY, cardWidth - 48);

        // 「下一題」按鈕參數
        let btnW = 140;
        let btnH = 44;
        let btnX = cardX + cardWidth - 24 - btnW;
        let btnY = cardY + cardHeight - 64;

        let isBtnHover = mouseX > btnX && mouseX < btnX + btnW &&
                         mouseY > btnY && mouseY < btnY + btnH;

        fill(isBtnHover ? 60 : 74, isBtnHover ? 130 : 144, isBtnHover ? 210 : 226);
        noStroke();
        rect(btnX, btnY, btnW, btnH, 8);

        fill(255);
        textFont('LXGW WenKai TC, sans-serif');
        textSize(15);
        textAlign(CENTER, CENTER);
        let btnLabel = (currentQuestion === quizData.length - 1) ? "查看成績 ➔" : "下一題 ➔";
        text(btnLabel, btnX + btnW / 2, btnY + btnH / 2);
      }
    }

    function drawResultScreen() {
      let cardWidth = constrain(width * 0.85, 300, 600);
      let cardHeight = 400;
      let cardX = width / 2 - cardWidth / 2;
      let cardY = height / 2 - cardHeight / 2;

      // 陰影與主卡片
      noStroke();
      fill(205, 215, 230, 100);
      rect(cardX + 6, cardY + 6, cardWidth, cardHeight, 16);

      fill(255);
      stroke(218, 226, 236);
      strokeWeight(2);
      rect(cardX, cardY, cardWidth, cardHeight, 16);

      // 結算標題
      fill(40);
      textFont('LXGW WenKai TC, sans-serif');
      textSize(26);
      textAlign(CENTER, CENTER);
      text("🎉 測驗完成！", width / 2, cardY + 70);

      // 分數大數字顯示
      fill(74, 144, 226);
      textFont('Fraunces, serif');
      textSize(52);
      text(score + " / " + quizData.length, width / 2, cardY + 160);

      fill(100);
      textFont('LXGW WenKai TC, sans-serif');
      textSize(18);
      text("您一共答對了 " + score + " 道題目", width / 2, cardY + 230);

      // 「重新測驗」按鈕
      let btnW = 160;
      let btnH = 48;
      let btnX = width / 2 - btnW / 2;
      let btnY = cardY + 300;

      let isBtnHover = mouseX > btnX && mouseX < btnX + btnW &&
                       mouseY > btnY && mouseY < btnY + btnH;

      fill(isBtnHover ? 60 : 74, isBtnHover ? 130 : 144, isBtnHover ? 210 : 226);
      noStroke();
      rect(btnX, btnY, btnW, btnH, 8);

      fill(255);
      textFont('LXGW WenKai TC, sans-serif');
      textSize(16);
      textAlign(CENTER, CENTER);
      text("重新測驗", width / 2, btnY + btnH / 2);
    }

    function mousePressed() {
      if (currentQuestion < quizData.length) {
        let q = quizData[currentQuestion];
        let cardWidth = constrain(width * 0.9, 300, 720);
        let cardHeight = constrain(height * 0.88, 500, 660);
        let cardX = width / 2 - cardWidth / 2;
        let cardY = height / 2 - cardHeight / 2;
        let optionStartY = cardY + 165;
        let optionHeight = width < 500 ? 44 : 50;
        let optionSpacing = width < 500 ? 10 : 14;

        if (!answered) {
          // 偵測是否點擊選項
          for (let i = 0; i < q.options.length; i++) {
            let optY = optionStartY + i * (optionHeight + optionSpacing);
            
            if (mouseX > cardX + 24 && mouseX < cardX + cardWidth - 24 &&
                mouseY > optY && mouseY < optY + optionHeight) {
              
              selectedOption = i;
              answered = true;
              
              if (selectedOption === q.answer) {
                score++;
              }
              break;
            }
          }
        } else {
          // 偵測是否點擊「下一題」按鈕
          let btnW = 140;
          let btnH = 44;
          let btnX = cardX + cardWidth - 24 - btnW;
          let btnY = cardY + cardHeight - 64;

          if (mouseX > btnX && mouseX < btnX + btnW &&
              mouseY > btnY && mouseY < btnY + btnH) {
            
            currentQuestion++;
            selectedOption = -1;
            answered = false;
          }
        }
      } else {
        // 結算畫面「重新測驗」按鈕點擊
        let cardHeight = 400;
        let cardY = height / 2 - cardHeight / 2;
        let btnW = 160;
        let btnH = 48;
        let btnX = width / 2 - btnW / 2;
        let btnY = cardY + 300;

        if (mouseX > btnX && mouseX < btnX + btnW &&
            mouseY > btnY && mouseY < btnY + btnH) {
          initQuiz();
        }
      }
    }

    // 視窗大小改變或手機轉向時自動調整畫布尺寸
    function windowResized() {
      resizeCanvas(windowWidth, windowHeight);
    }
  </script>
</body>
</html>