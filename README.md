<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>혜화 속 미술은행 : Memory in Flow</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+KR:wght@400;600;700&family=Pretendard:wght@400;500;600&display=swap" rel="stylesheet">
    <script>
        tailwind.config={theme:{extend:{colors:{brand:{gold:'#E5A63B',coral:'#E87A5D',teal:'#56ACAC',yellowBg:'#F8B62D'}},fontFamily:{serif:['"Noto Serif KR"','serif'],sans:['"Pretendard"','sans-serif']}}}}
    </script>
    <style>
        body{font-family:'Pretendard',sans-serif;background:#121212;color:#2C2A29}
        .mc{max-width:480px;margin:0 auto;background:#FAF8F5;min-height:100vh;position:relative}
        .glass{background:rgba(255,255,255,0.88);backdrop-filter:blur(12px);border:1px solid rgba(255,255,255,0.5)}
        .glass-d{background:rgba(44,42,41,0.9);backdrop-filter:blur(10px);color:#FAF8F5}
        html{scroll-behavior:smooth}
    </style>
</head>
<body class="antialiased">
    <div class="mc pb-20 shadow-2xl">
        <header class="sticky top-0 z-50 glass px-5 py-3 flex justify-between items-center border-b border-stone-200">
            <div class="flex items-center gap-2">
                <span class="w-2.5 h-2.5 rounded-full bg-brand-coral animate-pulse"></span>
                <span class="font-serif font-bold text-xs text-stone-800">혜화 속 미술은행</span>
            </div>
            <div class="flex items-center gap-3 text-stone-600 text-sm">
                <button onclick="shareExhibition()" class="hover:text-brand-gold p-1" title="공유"><i class="fa-solid fa-share-nodes text-xs"></i></button>
                <a href="#mapSection" class="hover:text-brand-gold p-1" title="위치"><i class="fa-solid fa-location-dot text-xs"></i></a>
            </div>
        </header>

        <section class="px-6 pt-7 pb-10 flex flex-col justify-between min-h-[75vh]" style="background:linear-gradient(135deg, #F9ECE1 0%, #F5F1DA 40%, #E6F3EE 100%)">
            <div class="space-y-1">
                <span class="inline-block px-3 py-1 rounded-full bg-white/80 border border-stone-200 text-[11px] font-medium text-stone-700">2026 국립현대미술관 미술은행 청년인력양성 사업</span>
                <p class="text-[10px] font-serif text-stone-500 uppercase tracking-widest">National Museum of Modern and Contemporary Art, Korea</p>
            </div>
            <div class="my-5 space-y-2">
                <h1 class="font-serif font-black text-4xl text-stone-900 leading-tight">혜화 속<br>미술은행</h1>
                <p class="font-serif italic text-sm text-stone-700">: Memory in flow</p>
                <div class="pt-1 flex flex-wrap gap-1.5 text-xs font-serif text-stone-700">
                    <span class="px-2.5 py-0.5 rounded bg-white/80 border border-amber-200">스미다</span>
                    <span class="px-2.5 py-0.5 rounded bg-white/80 border border-amber-200">번지다</span>
                    <span class="px-2.5 py-0.5 rounded bg-white/80 border border-amber-200">흐르다</span>
                    <span class="px-2.5 py-0.5 rounded bg-white/80 border border-amber-200">고이다</span>
                </div>
            </div>
            <div class="glass p-4 rounded-2xl shadow-lg space-y-2.5">
                <div class="flex justify-between items-center border-b border-stone-200 pb-2">
                    <div>
                        <span class="text-[9px] text-stone-400 font-semibold block uppercase">EXHIBITION DATES</span>
                        <span class="text-xs font-bold text-stone-800">2026. 08. 16 (일) ~ 08. 30 (일)</span>
                    </div>
                    <span id="dDayBadge" class="px-2 py-0.5 rounded-full bg-brand-coral text-white text-[10px] font-bold">D-DAY</span>
                </div>
                <div class="grid grid-cols-2 gap-1 text-[11px] text-stone-700">
                    <div><span class="text-stone-400 block text-[9px]">관람 시간</span><span class="font-medium">10:00 - 18:00 (월 휴관)</span></div>
                    <div><span class="text-stone-400 block text-[9px]">전시 장소</span><span class="font-medium">상명아트센터 갤러리 1F</span></div>
                </div>
                <div class="pt-1 flex gap-2">
                    <a href="#rsvpModal" onclick="openRsvpModal()" class="flex-1 py-2 bg-stone-900 text-white text-center rounded-xl text-xs font-medium flex items-center justify-center gap-1"><i class="fa-regular fa-bell text-xs"></i> 일정 신청</a>
                    <a href="#diarySection" class="flex-1 py-2 bg-brand-gold text-white text-center rounded-xl text-xs font-medium flex items-center justify-center gap-1"><i class="fa-solid fa-pen-nib text-xs"></i> 마음일기장</a>
                </div>
            </div>
        </section>

        <!-- CURATOR NOTE -->
        <section class="px-6 py-8 bg-white space-y-4 border-t border-stone-100">
            <div class="space-y-1">
                <span class="text-xs font-serif text-brand-coral uppercase tracking-widest font-semibold block">Curator's Note</span>
                <h2 class="text-lg font-serif font-bold text-stone-900">예술은 특별한 공간에만 머무르지 않는다</h2>
            </div>
            <div class="p-4 rounded-2xl bg-[#F88B54] text-white space-y-2 font-serif text-xs">
                <p class="font-light">"일상의 길목에서 우연히 마주한 한 작품은 잠시 발걸음을 멈추게 하고, 익숙했던 풍경을 새롭게 바라보게 합니다."</p>
                <p class="opacity-90 text-[11px]">그 짧은 만남은 오래된 기억을 떠올리게 하고, 미처 의식하지 못했던 감정을 발견하게 합니다.</p>
            </div>
            <div class="text-stone-700 text-xs leading-relaxed font-serif space-y-2">
                <p>이번 《혜화 속 미술은행: Memory in Flow》는 대학로 혜화라는 역사적 감수성의 거리에서 관람객과 예술이 스치는 순간을 담아내고자 했습니다.</p>
                <p>국립현대미술관 미술은행의 소장품들이 여러분의 지나온 기억과 교차할 때 비로소 생명력을 얻습니다.</p>
            </div>
        </section>

        <!-- SECTIONS -->
        <section class="px-6 py-8 bg-stone-900 text-white space-y-4">
            <div class="text-center space-y-1">
                <span class="text-xs font-serif text-brand-gold tracking-widest uppercase block">Exhibition Sections</span>
                <h2 class="text-lg font-serif font-bold">4가지 감각의 흐름</h2>
            </div>
            <div class="rounded-xl bg-brand-yellowBg p-4 space-y-2 text-stone-900">
                <div class="flex justify-between items-start">
                    <div><span class="text-[9px] font-bold uppercase text-stone-700">SECTION 01</span><h3 class="text-base font-serif font-bold">스미다 (Permeate)</h3></div>
                    <span class="w-6 h-6 rounded-full bg-white/40 flex items-center justify-center font-bold text-xs">01</span>
                </div>
                <p class="text-xs font-serif leading-relaxed">모든 기억은 첫 만남에서 시작된다. 빛과 색, 형태가 만들어 내는 울림은 마음속에 스며든다.</p>
                <div class="pt-1.5 border-t border-stone-900/10 flex flex-wrap gap-1 font-serif text-[11px] font-bold">
                    <span class="px-2 py-0.5 rounded bg-white/50">권기수</span><span class="px-2 py-0.5 rounded bg-white/50">권용래</span><span class="px-2 py-0.5 rounded bg-white/50">노은주</span><span class="px-2 py-0.5 rounded bg-white/50">노 준</span><span class="px-2 py-0.5 rounded bg-white/50">신수진</span>
                </div>
            </div>
            <div class="rounded-xl bg-brand-yellowBg p-4 space-y-2 text-stone-900">
                <div class="flex justify-between items-start">
                    <div><span class="text-[9px] font-bold uppercase text-stone-700">SECTION 02</span><h3 class="text-base font-serif font-bold">번지다 (Spread)</h3></div>
                    <span class="w-6 h-6 rounded-full bg-white/40 flex items-center justify-center font-bold text-xs">02</span>
                </div>
                <p class="text-xs font-serif leading-relaxed">스며든 감각은 작품과 공간을 따라 번져 나간다. 서로 다른 시선은 새로운 연결을 만든다.</p>
                <div class="pt-1.5 border-t border-stone-900/10 flex flex-wrap gap-1 font-serif text-[11px] font-bold">
                    <span class="px-2 py-0.5 rounded bg-white/50">김동원</span><span class="px-2 py-0.5 rounded bg-white/50">김병주</span><span class="px-2 py-0.5 rounded bg-white/50">김현숙</span><span class="px-2 py-0.5 rounded bg-white/50">이세현</span><span class="px-2 py-0.5 rounded bg-white/50">홍세진</span>
                </div>
            </div>
            <div class="rounded-xl bg-brand-yellowBg p-4 space-y-2 text-stone-900">
                <div class="flex justify-between items-start">
                    <div><span class="text-[9px] font-bold uppercase text-stone-700">SECTION 03</span><h3 class="text-base font-serif font-bold">흐르다 (Flow)</h3></div>
                    <span class="w-6 h-6 rounded-full bg-white/40 flex items-center justify-center font-bold text-xs">03</span>
                </div>
                <p class="text-xs font-serif leading-relaxed">시간은 멈추지 않고 흐른다. 사람과 관계, 기억은 작품 속에서 교차하며 이야기를 이어간다.</p>
                <div class="pt-1.5 border-t border-stone-900/10 flex flex-wrap gap-1 font-serif text-[11px] font-bold">
                    <span class="px-2 py-0.5 rounded bg-white/50">김나리</span><span class="px-2 py-0.5 rounded bg-white/50">박영근</span><span class="px-2 py-0.5 rounded bg-white/50">방인희</span><span class="px-2 py-0.5 rounded bg-white/50">안규철</span><span class="px-2 py-0.5 rounded bg-white/50">차혜림</span>
                </div>
            </div>
            <div class="rounded-xl bg-brand-yellowBg p-4 space-y-2 text-stone-900">
                <div class="flex justify-between items-start">
                    <div><span class="text-[9px] font-bold uppercase text-stone-700">SECTION 04</span><h3 class="text-base font-serif font-bold">고이다 (Accumulate)</h3></div>
                    <span class="w-6 h-6 rounded-full bg-white/40 flex items-center justify-center font-bold text-xs">04</span>
                </div>
                <p class="text-xs font-serif leading-relaxed">흘러온 시간과 감정은 마음 한편에 쌓인다. 작품과 함께한 순간은 새로운 흐름으로 이어진다.</p>
                <div class="pt-1.5 border-t border-stone-900/10 flex flex-wrap gap-1 font-serif text-[11px] font-bold">
                    <span class="px-2 py-0.5 rounded bg-white/50">고혜정</span><span class="px-2 py-0.5 rounded bg-white/50">김병주</span><span class="px-2 py-0.5 rounded bg-white/50">박형진</span><span class="px-2 py-0.5 rounded bg-white/50">변상환</span><span class="px-2 py-0.5 rounded bg-white/50">서기환</span><span class="px-2 py-0.5 rounded bg-white/50">최재혁</span>
                </div>
            </div>
        </section>

        <!-- SPECIAL EVENTS -->
        <section class="px-6 py-8 bg-white space-y-4">
            <div class="space-y-1 text-center">
                <span class="text-xs font-serif text-brand-coral uppercase tracking-widest font-semibold block">Special Events</span>
                <h2 class="text-lg font-serif font-bold text-stone-900">전시 특별 프로그램</h2>
            </div>
            <div class="p-4 rounded-xl bg-amber-100 border border-amber-200 space-y-2">
                <div class="flex items-center justify-between border-b border-amber-200 pb-1.5">
                    <div><span class="text-[9px] font-bold text-amber-800 uppercase block">OPENING CEREMONY</span><h3 class="font-serif font-bold text-sm text-stone-900">개막행사 안내</h3></div>
                    <span class="text-[10px] font-bold text-stone-800 bg-white/80 px-2 py-0.5 rounded">8월 16일(일) 15:00</span>
                </div>
                <div class="space-y-1 text-xs text-stone-700 font-serif">
                    <div class="flex gap-2"><span class="font-bold text-amber-800 min-w-[32px]">15:00</span><span>참석자 등록 및 전시 관람</span></div>
                    <div class="flex gap-2"><span class="font-bold text-amber-800 min-w-[32px]">15:08</span><span>총장님 인사말 & 축사</span></div>
                    <div class="flex gap-2"><span class="font-bold text-amber-800 min-w-[32px]">15:18</span><div><span class="font-bold block">🎻 개막 축하 연주</span><span class="text-[10px] text-stone-600">• F. Kreisler - Schön Rosmarin / G. Fauré - Sicilienne</span></div></div>
                    <div class="flex gap-2"><span class="font-bold text-amber-800 min-w-[32px]">15:35</span><span>학예사와 함께하는 전시 투어</span></div>
                </div>
            </div>
            <div class="p-4 rounded-xl bg-teal-50 border border-teal-200 space-y-2">
                <div class="flex items-center justify-between border-b border-teal-200 pb-1.5">
                    <div><span class="text-[9px] font-bold text-teal-700 uppercase block">ARTIST TALK</span><h3 class="font-serif font-bold text-sm text-stone-900">박형진 작가와의 대화</h3></div>
                    <span class="text-[10px] font-bold text-white bg-brand-teal px-2 py-0.5 rounded">8월 22일(토) 15:00</span>
                </div>
                <p class="text-xs text-stone-700 font-serif leading-relaxed">새와 자연, 둥지의 포근한 감각을 담아내는 박형진 작가와 함께 작품 속 시간의 자국과 일상 속 예술을 다룹니다.</p>
                <button onclick="openRsvpModal()" class="w-full py-2 bg-brand-teal text-white text-xs font-bold rounded-lg shadow hover:bg-teal-700"><i class="fa-solid fa-calendar-check mr-1"></i>참가 사전 예약</button>
            </div>
        </section>

        <!-- DIARY SECTION -->
        <section id="diarySection" class="px-6 py-8 bg-gradient-to-b from-amber-50 to-orange-50 border-t border-amber-100 space-y-4">
            <div class="text-center space-y-1">
                <span class="text-xs font-serif text-brand-coral uppercase tracking-widest font-semibold block">Visitor Journal</span>
                <h2 class="text-lg font-serif font-bold text-stone-900">혜화에서 적어내리는 마음일기장</h2>
                <p class="text-xs text-stone-600 font-serif">전시를 관람하며 마음속에 남은 생각을 적어주세요.</p>
            </div>

            <div class="glass p-4 rounded-xl border border-amber-200 shadow-sm space-y-3">
                <div>
                    <label class="block text-xs font-bold text-stone-700 mb-1 font-serif">1. 마음 단어 선택</label>
                    <div class="grid grid-cols-4 gap-1 text-xs font-serif">
                        <button type="button" onclick="selectKeyword('스미다','✨')" class="kw-btn py-1.5 rounded-lg border border-amber-500 bg-amber-500 text-white font-semibold flex flex-col items-center" data-word="스미다"><span>✨</span><span>스미다</span></button>
                        <button type="button" onclick="selectKeyword('번지다','🌊')" class="kw-btn py-1.5 rounded-lg border border-stone-300 bg-white text-stone-700 font-semibold flex flex-col items-center" data-word="번지다"><span>🌊</span><span>번지다</span></button>
                        <button type="button" onclick="selectKeyword('흐르다','🍃')" class="kw-btn py-1.5 rounded-lg border border-stone-300 bg-white text-stone-700 font-semibold flex flex-col items-center" data-word="흐르다"><span>🍃</span><span>흐르다</span></button>
                        <button type="button" onclick="selectKeyword('고이다','💧')" class="kw-btn py-1.5 rounded-lg border border-stone-300 bg-white text-stone-700 font-semibold flex flex-col items-center" data-word="고이다"><span>💧</span><span>고이다</span></button>
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-bold text-stone-700 mb-1 font-serif">2. 마음 이모티콘 선택</label>
                    <div class="flex gap-1.5 text-base" id="emojiPicker">
                        <button type="button" onclick="selectEmoji('💛')" class="em-btn w-8 h-8 rounded-lg border border-amber-400 bg-amber-50 flex items-center justify-center" data-emoji="💛">💛</button>
                        <button type="button" onclick="selectEmoji('🌿')" class="em-btn w-8 h-8 rounded-lg border border-stone-200 bg-white flex items-center justify-center" data-emoji="🌿">🌿</button>
                        <button type="button" onclick="selectEmoji('🎨')" class="em-btn w-8 h-8 rounded-lg border border-stone-200 bg-white flex items-center justify-center" data-emoji="🎨">🎨</button>
                        <button type="button" onclick="selectEmoji('🌸')" class="em-btn w-8 h-8 rounded-lg border border-stone-200 bg-white flex items-center justify-center" data-emoji="🌸">🌸</button>
                        <button type="button" onclick="selectEmoji('💭')" class="em-btn w-8 h-8 rounded-lg border border-stone-200 bg-white flex items-center justify-center" data-emoji="💭">💭</button>
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-bold text-stone-700 mb-1 font-serif">3. 이름 / 닉네임</label>
                    <input type="text" id="authorInput" placeholder="예: 대학로를 거니는 이" class="w-full px-3 py-1.5 text-xs rounded-lg border border-stone-300 focus:outline-none bg-white">
                </div>

                <div>
                    <label class="block text-xs font-bold text-stone-700 mb-1 font-serif">4. 마음일기 내용</label>
                    <textarea id="contentInput" rows="2" placeholder="작품 앞에서 느꼈던 감정이나 기억을 적어주세요..." class="w-full px-3 py-1.5 text-xs rounded-lg border border-stone-300 focus:outline-none bg-white font-serif resize-none"></textarea>
                </div>

                <button onclick="saveDiaryEntry()" class="w-full py-2 bg-brand-coral text-white rounded-lg text-xs font-bold shadow hover:bg-orange-600 flex items-center justify-center gap-1"><i class="fa-solid fa-paper-plane"></i> 마음일기장 게시하기</button>
            </div>

            <div id="diaryList" class="space-y-2 pt-1">
                <div class="p-3 rounded-lg bg-white border border-stone-200 shadow-sm space-y-1">
                    <div class="flex justify-between items-center text-xs">
                        <div class="flex items-center gap-1"><span class="px-2 py-0.5 rounded bg-amber-100 text-amber-800 font-bold font-serif">✨ 스미다</span><span>💛</span></div>
                        <span class="text-stone-400 text-[10px]">혜화동 관람객</span>
                    </div>
                    <p class="text-xs font-serif text-stone-700">"오랜만에 대학로 골목을 지나 미술관에 들어서니, 바쁜 일상 속에 잊고 지냈던 평온함이 마음속 깊이 스며듭니다."</p>
                    <div class="flex justify-end">
                        <button onclick="toggleLike(this)" class="px-2 py-0.5 rounded-full border border-stone-200 text-[10px] text-stone-500 flex items-center gap-1"><span>❤️</span><span class="like-count font-bold">12</span></button>
                    </div>
                </div>
            </div>
        </section>

        <!-- LOCATION -->
        <section id="mapSection" class="px-6 py-8 bg-white space-y-4 border-t border-stone-200">
            <div class="space-y-1 text-center">
                <span class="text-xs font-serif text-brand-teal uppercase tracking-widest font-semibold block">Location Info</span>
                <h2 class="text-lg font-serif font-bold text-stone-900">오시는 길 및 관람 안내</h2>
            </div>
            <div class="bg-sky-50 border border-sky-200 p-4 rounded-xl space-y-1.5 font-serif">
                <span class="text-[9px] font-bold text-sky-800 uppercase block">VENUE ADDRESS</span>
                <h3 class="text-xs font-bold text-stone-900">상명아트센터 갤러리 1F</h3>
                <p class="text-xs text-stone-600">서울 종로구 동숭길 133 상명대학교예술디자인센터 1층</p>
                <p class="text-xs text-stone-700 pt-1 border-t border-sky-200 flex items-center gap-1"><i class="fa-solid fa-train-subway text-sky-600"></i> 지하철 4호선 혜화역 1번 출구 (도보 1분)</p>
            </div>
            <div class="grid grid-cols-2 gap-2">
                <button onclick="addToCalendar()" class="py-2 bg-stone-800 text-white rounded-lg text-xs font-bold"><i class="fa-regular fa-calendar-plus mr-1"></i>일정에 추가</button>
                <button onclick="shareExhibition()" class="py-2 bg-brand-gold text-white rounded-lg text-xs font-bold"><i class="fa-solid fa-share-nodes mr-1"></i>초대장 공유</button>
            </div>
        </section>

        <footer class="px-6 py-6 bg-stone-900 text-stone-400 text-center text-[10px] font-serif space-y-1">
            <p class="font-semibold text-stone-200 text-xs">혜화 속 미술은행 : Memory in Flow</p>
            <p class="text-stone-500">2026 국립현대미술관 미술은행 &lt;청년인력양성 사업&gt;</p>
            <p class="text-stone-600">주최: 상명대학교 | 후원: 국립현대미술관 미술은행</p>
        </footer>
    </div>

    <!-- MODAL -->
    <div id="rsvpModal" class="fixed inset-0 bg-black/70 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-xs w-full p-5 space-y-3 relative font-serif shadow-2xl">
            <button onclick="closeRsvpModal()" class="absolute top-3 right-3 text-stone-400 text-base"><i class="fa-solid fa-xmark"></i></button>
            <div class="text-center space-y-1">
                <h3 class="text-base font-bold text-stone-900">프로그램 알림 신청</h3>
                <p class="text-[11px] text-stone-500">사전 알림 문자를 보내드립니다.</p>
            </div>
            <form onsubmit="submitRsvp(event)" class="space-y-2 pt-1">
                <div>
                    <label class="block text-[11px] font-bold text-stone-700 mb-0.5">참석 프로그램</label>
                    <select id="rsvpProgram" class="w-full px-2 py-1 text-xs rounded-lg border border-stone-300 bg-white">
                        <option value="개막행사 (08.16 15:00)">개막행사 (08.16 일 15:00)</option>
                        <option value="박형진 작가 토크 (08.22 15:00)">박형진 작가 토크 (08.22 토 15:00)</option>
                    </select>
                </div>
                <div><label class="block text-[11px] font-bold text-stone-700 mb-0.5">성함</label><input type="text" required placeholder="성함 입력" class="w-full px-2 py-1 text-xs rounded-lg border border-stone-300"></div>
                <div><label class="block text-[11px] font-bold text-stone-700 mb-0.5">연락처</label><input type="tel" required placeholder="010-0000-0000" class="w-full px-2 py-1 text-xs rounded-lg border border-stone-300"></div>
                <button type="submit" class="w-full py-2 bg-brand-coral text-white font-bold rounded-lg text-xs mt-1">신청하기</button>
            </form>
        </div>
    </div>

    <!-- TOAST -->
    <div id="toast" class="fixed bottom-6 left-1/2 -translate-x-1/2 glass-d px-4 py-2 rounded-full text-xs font-medium shadow-2xl transition-all duration-300 opacity-0 pointer-events-none z-50 flex items-center gap-2">
        <i class="fa-solid fa-circle-check text-brand-gold"></i><span id="toastMsg">알림 메시지</span>
    </div>

    <script>
        let selectedKeyword='스미다', selectedEmoji='💛';
        function updateDDay(){
            const diff=Math.ceil((new Date('2026-08-16T00:00:00')-new Date())/(1000*60*60*24));
            document.getElementById('dDayBadge').innerText=diff>0?`D-${diff}`:(diff===0?'D-DAY':'전시 중');
        }
        function selectKeyword(word,emoji){
            selectedKeyword=word;if(emoji)selectEmoji(emoji);
            document.querySelectorAll('.kw-btn').forEach(btn=>{
                const m=btn.getAttribute('data-word')===word;
                btn.className=`kw-btn py-1.5 rounded-lg border ${m?'border-amber-500 bg-amber-500 text-white':'border-stone-300 bg-white text-stone-700'} font-semibold flex flex-col items-center`;
            });
        }
        function selectEmoji(emoji){
            selectedEmoji=emoji;
            document.querySelectorAll('.em-btn').forEach(btn=>{
                const m=btn.getAttribute('data-emoji')===emoji;
                btn.className=`em-btn w-8 h-8 rounded-lg border ${m?'border-amber-400 bg-amber-50':'border-stone-200 bg-white'} flex items-center justify-center`;
            });
        }
        function saveDiaryEntry(){
            const author=document.getElementById('authorInput').value.trim()||'혜화 관람객';
            const content=document.getElementById('contentInput').value.trim();
            if(!content)return showToast('마음일기 내용을 입력해 주세요.');
            const card=document.createElement('div');
            card.className='p-3 rounded-lg bg-white border border-stone-200 shadow-sm space-y-1';
            card.innerHTML=`<div class="flex justify-between items-center text-xs"><div class="flex items-center gap-1"><span class="px-2 py-0.5 rounded bg-amber-100 text-amber-800 font-bold font-serif">${selectedKeyword}</span><span>${selectedEmoji}</span></div><span class="text-stone-400 text-[10px]">${escapeHtml(author)}</span></div><p class="text-xs font-serif text-stone-700">"${escapeHtml(content)}"</p><div class="flex justify-end"><button onclick="toggleLike(this)" class="px-2 py-0.5 rounded-full border border-stone-200 text-[10px] text-stone-500 flex items-center gap-1"><span>❤️</span><span class="like-count font-bold">1</span></button></div>`;
            document.getElementById('diaryList').prepend(card);
            document.getElementById('contentInput').value='';
            showToast('마음일기가 등록되었습니다.');
        }
        function toggleLike(btn){
            let countSpan=btn.querySelector('.like-count'),current=parseInt(countSpan.innerText);
            if(btn.classList.contains('liked')){btn.classList.remove('liked','text-red-500','bg-red-50');countSpan.innerText=current-1;}
            else{btn.classList.add('liked','text-red-500','bg-red-50');countSpan.innerText=current+1;}
        }
        function escapeHtml(t){return t.replace(/[&<>"']/g,m=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#039;'}[m]));}
        function openRsvpModal(){document.getElementById('rsvpModal').classList.remove('hidden');}
        function closeRsvpModal(){document.getElementById('rsvpModal').classList.add('hidden');}
        function submitRsvp(e){e.preventDefault();closeRsvpModal();showToast('사전 신청이 완료되었습니다.');}
        function addToCalendar(){window.open(`https://calendar.google.com/calendar/render?action=TEMPLATE&text=${encodeURIComponent('혜화 속 미술은행 전시회')}&dates=20260816T100000Z/20260830T180000Z&details=${encodeURIComponent('상명아트센터 갤러리 1F')}`,'_blank');}
        function shareExhibition(){document.execCommand('copy');showToast('초대장 링크가 복사되었습니다.');}
        function showToast(msg){
            const toast=document.getElementById('toast');
            document.getElementById('toastMsg').innerText=msg;
            toast.classList.remove('opacity-0','pointer-events-none');
            setTimeout(()=>toast.classList.add('opacity-0','pointer-events-none'),2300);
        }
        window.onload=function(){updateDDay();selectKeyword('스미다','✨');};
    </script>
</body>
</html>
