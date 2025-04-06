<script lang="ts">
  // 사용자 정보
  const department = "컴퓨터과학과"; // 예: 컴퓨터과학과
  const name = "윤태연"; // 예: 홍길동
  
  // 선택한 센서 정보
  const sensors = [
    {
      name: "가속도 센서 & 자이로스코프 센서",
      shortName: "Accelerometer & Gyroscope",
      description: "움직임과 회전을 감지하는 센서로, MEMS 기술을 기반으로 제작됩니다.",
      applications: [
        "동작 인식 및 제스처 컨트롤",
        "이미지 및 동영상 안정화",
        "게임 컨트롤",
        "화면 자동 회전",
        "만보계 기능"
      ],
      industryContribution: "자율주행차량, 드론, 웨어러블 기기 등 4차 산업혁명의 핵심 기술 분야에 활용됩니다."
    },
    {
      name: "GPS",
      shortName: "Global Positioning System",
      description: "위성 신호를 수신하여 현재 위치의 위도, 경도, 고도 정보를 계산하는 센서입니다.",
      applications: [
        "내비게이션 및 위치 기반 서비스",
        "운동 트래킹",
        "증강현실(AR) 서비스",
        "소셜 네트워킹"
      ],
      industryContribution: "스마트시티 구현, 자율주행차량, 공유 경제 등 4차 산업혁명의 핵심 인프라로 활용됩니다."
    },
    {
      name: "지문 인식 센서",
      shortName: "Fingerprint Sensor",
      description: "지문의 융선과 골 패턴을 감지하여 개인 인증에 활용하는 생체인식 센서입니다.",
      applications: [
        "스마트폰 잠금 해제",
        "앱 보안",
        "모바일 결제 인증",
        "온라인 서비스 로그인"
      ],
      industryContribution: "보안과 개인정보 보호의 핵심 요소로, 4차 산업혁명 시대의 핀테크, 의료 서비스 등에 활용됩니다."
    }
  ];
</script>

<main class="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 p-4 md:p-8">
  <div class="max-w-4xl mx-auto">
    <div class="bg-white rounded-xl shadow-lg overflow-hidden mb-8">
      <div class="bg-[#0364FD] py-6 px-6">
        <h1 class="text-2xl md:text-3xl font-bold text-white">2025학년도 1학기 컴퓨터의이해 중간과제물</h1>
      </div>
      
      <div class="p-6">
        <div class="flex flex-col md:flex-row gap-4 mb-8">
          <div class="bg-indigo-50 rounded-lg p-4 flex-1">
            <h2 class="font-semibold text-[#0364FD]">학과</h2>
            <p class="text-lg text-gray-800">{department}</p>
          </div>
          <div class="bg-indigo-50 rounded-lg p-4 flex-1">
            <h2 class="font-semibold text-[#0364FD]">이름</h2>
            <p class="text-lg text-gray-800">{name}</p>
          </div>
        </div>
        
        <h2 class="text-xl font-bold text-gray-800 mb-6">선택한 센서 기술</h2>
        
        <div class="space-y-8">
          {#each sensors as sensor}
            <div class="border border-gray-200 rounded-lg overflow-hidden">
              <div class="bg-gray-50 p-4 border-b border-gray-200">
                <h3 class="text-lg font-semibold text-gray-800">{sensor.name}</h3>
                <p class="text-gray-500 text-sm">{sensor.shortName}</p>
              </div>
              <div class="p-4">
                <p class="text-gray-700 mb-4">{sensor.description}</p>
                
                <h4 class="font-semibold text-[#0364FD] mb-2">주요 활용 사례</h4>
                <ul class="list-disc pl-5 mb-4 space-y-1">
                  {#each sensor.applications as app}
                    <li class="text-gray-700">{app}</li>
                  {/each}
                </ul>
                
                <h4 class="font-semibold text-[#0364FD] mb-2">4차 산업혁명 기여</h4>
                <p class="text-gray-700">{sensor.industryContribution}</p>
              </div>
            </div>
          {/each}
        </div>
      </div>
    </div>
    
    <div class="text-center text-gray-600 text-sm p-4">
      <p>이 페이지는 과제 제출을 위해 작성되었습니다.</p>
      <p>© {new Date().getFullYear()} {name} - 모든 권리 보유</p>
    </div>
  </div>
</main>