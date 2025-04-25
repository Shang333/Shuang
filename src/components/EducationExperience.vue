<template>
    <section id="education-experience" class="edu-exp-section">
      <h2>學歷</h2>
      <ul class="edu-list">
        <li v-for="(edu, i) in educations" :key="i">
          <h3>{{ edu.school }} <span>{{ edu.date }}</span></h3>
          <p>{{ edu.degree }}</p>
          <p class="desc">{{ edu.description }}</p>
        </li>
      </ul>

      <h2>專業訓練</h2>
      <ul class="edu-list">
        <li v-for="(edu, i) in train" :key="i">
          <h3>{{ edu.school }} <span>{{ edu.date }}</span></h3>
          <p>{{ edu.degree }}</p>
          <p class="desc">{{ edu.description }}</p>
        </li>
      </ul>
  
    <h2>工作經驗</h2>
      <ul class="exp-list">
        <li v-for="(exp, i) in experiences" :key="i">
            <h3>{{ exp.company }} <span>{{ exp.date }}</span></h3>
            <p>{{ exp.title }}</p>
            <div class="desc">
            <div v-for="(project, j) in exp.projects" :key="j" class="project">
                <div class="project-title">{{ j + 1 }}. {{ project.title }} {{ project.date ? '(' + project.date + ')' : '' }}</div>
                <ul v-if="project.details && project.details.length > 0" class="project-details">
                <li v-for="(detail, k) in project.details" :key="k">{{ detail }}</li>
                </ul>
            </div>
            </div>
        </li>
      </ul>
    </section>
  </template>
  
  <script setup>
  const educations = [
    {
      school: '國立臺灣師範大學 - 環境教育所',
      degree: '碩士畢業',
      date: '2016/9 ~ 2019/5',
      description: "",
    },
    {
      school: '國立臺灣科技大學 - 營建工程系',
      degree: '學士畢業',
      date: '2011/5 ~ 2015/6',
      description: "",
    },
  ];
  
  const train =[
    {
      school: '資策會',
      degree: '全端工程師就業養成班結業',
      date: '2020/6 ~ 2020/9',
      description: '學習前端（ HTML / CSS、boostrap、 javascript、jQuery）、資料庫（SQL Server & Transact SQL語言）、後端（C#程式設計、LINQ資料存取技術、ASP.NET MVC網站開發）及版本控制（GitHub、Git）等技術',
    }  
  ];

  const experiences = [
  {
    company: '繽紛科技',
    title: '後端工程師',
    date: '2024/5 - 至今',
    projects: [
      {
        title: '台北市橋涵管理系統',
        date: '2024/5 ~ 至今',
        details: [
          '橋涵包含橋梁、地下道、隧道、人行天橋四種，總共約800多座橋涵',
          '既有系統使用框架為.net framework 4.8、資料庫為MS SQL，已有十年以上的歷史，包含10個大模組',
          '使用web site專案重建在windows 10環境運行',
          '修復1500多項資安漏洞',
          '開發新模組(.net core 6 Mvc web api):',
          'GIS模組: GIS查詢橋涵、hover查詢、單一橋涵查詢、下拉選單、EXCEL匯出等功能',
          '監測模組: 自行設計API格式，開發接收監測廠商資料的API、監測設備平台查詢',
          'AI裂縫辨識模組: 自行設計資料表和API格式，和Python工程師合作，相互傳送檔案、顯示相關分析資訊在平台上'
        ]
      },
      {
        title: '公司產品API開發',
        date: '2024/5~至今',
        details: ['人車、門禁、環安衛']
      },
      {
        title: 'AR智慧工地驗收輔助系統後台API開發',
        date: '2024/10~2024/11',
        details: ['和安卓、IOS APP工程師合作，開發APP使用的API，以及查詢後台']
      },
      {
        title: 'MVC網站圖片效能優化',
        date: '2025約一週',
        details: []
      },
      {
        title: '與主管共同研究/重構設計公司產品軟體架構',
        date: '2025/2~2025/4',
        details: []
      }
    ]
  },
  {
    company: '干城數碼(派駐在Acer總部)',
    title: '後端工程師',
    date: '2023/02 - 2023/09 (約半年)',
    projects: [
      {
        title: 'Acer全球官網維護',
        date: '',
        details: ['使用CMS系統、.net core、node.js等技術進行QA、開發及維護']
      },
      {
        title: 'Earth Mission App(已上架)',
        date: '',
        details: ['擔任Flutter QA']
      },
      {
        title: '自學AI繪圖工具於公司分享',
        date: '',
        details: ['Adobe Firefly、Midjourney、Stable Diffsion本機版']
      }
    ]
  },
  {
    company: '明門實業公司資訊部Web Team',
    title: '全端工程師',
    date: '2020/10 - 2022/06 (約2年)',
    projects: [
      {
        title: 'BPM系統開發',
        date: '',
        details: ['開發過2個專案，流程為撰寫需求文件、需求訪談、程式開發、測試、維運']
      },
      {
        title: '維護既有網頁系統',
        date: '',
        details: ['包含不同環境，經手過約7個']
      },
      {
        title: '處理使用者需求、使用問題回覆',
        date: '',
        details: []
      },
      {
        title: '自學各種技術於公司內部分享交流',
        date: '',
        details: [
          'Flutter入門與基礎實作',
          'Microsoft Power Apps開發訂餐App',
          'Bravo Studio X Figma復刻路跑網站'
        ]
      }
    ]
  },
  {
    company: '均一平台教育基金會',
    title: '內容合作開發組自然科內容實習生',
    date: '2019/06 - 2020/05 (約1年)',
    projects: [
      {
        title: '國中理化教材與外部合作課程開發',
        date: '',
        details: [
          '設計國中理化教材（撰寫14部腳本)，並編寫其他科外部合作課程之教材或習題（媒體教育教案及影片架構，台灣吧：歷史、公民，台北酷課雲：國中理財）',
          '與外部夥伴（台北酷課雲、動畫公司）共同開發108課綱素養導向60部國中理化動畫影片，並於三個月內完成修正及審查（影片內容、字幕、旁白）'
        ]
      }
    ]
  },
  {
    company: '致勝先師教育股份有限公司',
    title: '兼職數理科線上家教',
    date: '2018/06 - 2019/06 (1年)',
    projects: [
      {
        title: '線上教授國中小數理科課程',
        date: '',
        details: [
          '線上教授約300~400堂課(1小時/堂)',
          '依學生的需求打造客製化課程，以Skype線上授課，科目涵蓋國中小數理'
        ]
      }
    ]
  },
  {
    company: '國立臺灣師範大學',
    title: '＜建構本校大學部永續發展素養計畫＞兼任學習型助理',
    date: '2018/05 - 2018/12 (約1.5年)',
    projects: [
      {
        title: '環境教育研究計畫',
        date: '',
        details: ['規劃及執行環境教育研究計畫']
      }
    ]
  },
  {
    company: '臺北市私立鎮麟文理短期補習班(臺北車站本部)',
    title: '助理導師、國中數理輔導老師',
    date: '2015/04 - 2016/10 (約1.5年)',
    projects: []
  }
];
  </script>
  
  <style scoped lang="scss">
  .edu-exp-section {
    padding: 3rem 2rem;
    max-width: 800px;
    margin: auto;
  
    h2 {
      font-size: 1.5rem;
      margin-top: 2rem;
      margin-bottom: 1rem;
      border-bottom: 2px solid #ccc;
      padding-bottom: 0.5rem;
    }
  
    ul {
      list-style: none;
      padding: 0;
      margin: 0 0 2rem 0;
  
      li {
        margin-bottom: 1.5rem;
  
        h3 {
          margin: 0;
          font-size: 1.1rem;
          font-weight: bold;
  
          span {
            float: right;
            font-size: 0.9rem;
            color: #888;
          }
        }
  
        p {
          margin: 0.3rem 0;
          font-size: 0.95rem;
          color: #444;
        }
  
        .desc {
          font-size: 0.9rem;
          color: #666;
        }
      }
    }
    .desc {
        margin-top: 10px;
        }

        .project {
        margin-bottom: 15px;
        }

        .project-title {
        font-weight: bold;
        margin-bottom: 5px;
        }

        .project-details {
        margin-left: 20px;
        list-style-type: disc;
        }

        .project-details li {
        margin-bottom: 5px;
        }
  }
  </style>
  