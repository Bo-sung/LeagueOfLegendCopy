# LeagueOfLegendCopy
롤 모작. 칼바람 모작
맵 : 칼바람 나락
구성 
 일직선상의 맵.
 필요 구조물 : 각 진영마다 포탑 4개(1차, 2차, 쌍둥이), 억제기, 넥서스, 우물(우물 내 상점 포함)
 필요 몹 : (웨이브당 3마리)근거리 미니언, (웨이브당 3마리)원거리 미니언, (3웨이브당 한마리)대포 미니언, (억제기 파괴시 웨이브당 한마리)슈퍼 미니언
 구현할 챔피언 목록 : 카서스, 가랜, 애쉬, 리산드라.

세부사항


    시스템
     미니언 어그로 : 아군 챔피언이 적 챔피언에게 공격을 당할경우 아군 미니언이 상대 챔피언을 공격.
     포탑 어그로 : 적 챔피언이 아군 챔피언을 포탑 사거리 내에서 공격시 포탑의 타겟 적 챔피언으로 변경됨
     미니언 생성 순서
      1. 근거리 근거리 근거리 원거리 원거리 원거리
      2. 근거리 근거리 근거리 원거리 원거리 원거리
      3. 근거리 근거리 근거리 대포 원거리 원거리 원거리
     억제기 파괴시. 슈퍼미니언 근거리 근거리 근거리 (대포) 원거리 원거리 원거리
     대포 미니언 생성 조건 : 3번쨰 웨이브마다 생성.
     아이탬 구입 조건 : 게임 시작 또는 사망후 부활시 우물 내에서 구입가능. 단 우물밖으로 벗어날시 구매 불가
     
    챔피언
    
     카서스
					
     	스텟
      	구분  기본 능력(+레벨 당 상승) 최종 수치
		체력		550(+87)	2029
		체력 재생	6.5(+0.56)	16
		마나		467(+30.5)	985.5
		마나 재생	8.0(+0.8)	21.6
		공격력		45.66(+3.25)	100.86
		공격 속도	0.625(+2.11%)	0.849
		방어력		20.88(+3.5)	80.38
		마법 저항력	30(+0.5)	38.5
		사거리		450(+0)		450
		이동 속도	335(+0)		335
	
      패시브 : 사망시 7초간 부활하여 스킬을 마나소모없이 사용 가능. 단 궁극기는 유지시간 4초 초과시 시전 불가능.
      Q 스킬 : 적을 공격시 q 범위내 적이 하나일경우 2배의 피해를 가함.
      마나 소모량 : 20 / 26 / 23 / 36 / 44
      범위 : 675
      재사용대기시간 : 1s
      데미지 : 50 / 70 / 90 / 110 / 130(+0.35AP)
     
      W 스킬 : 지정한 지역에 통과 가능한 벽을 생성. 벽을 지나친 적은 슬로우 및 마법저항력 감소 디버프가 가해짐.      
      마나 소모량 :70
      범위 : 1000
      재사용대기시간 : 15s
      둔화율 : 40 / 50 / 60 / 70 / 80%
      마법저항력 감소 : 15%
      벽 너비 : 800 / 900 / 1000 / 1100 / 1200
      벽 시아 : 1300/ 1325 / 1350 / 1375 / 1400
      
      E 스킬 : 패시브는 적을 스킬로 처치시 마나을 일정량 회복함. 토글형 장판스킬
      마나 소모량 : 303 / 43 / 54 / 66 / 76
      범위 : 550
      재사용대기시간 : 0.5
      데미지 : 30 / 50 / 70 / 90 / 110(+0.2AP)
      
      R 스킬 : 모든 적 챔피언에게 피해를 가함. 사거리 제한 없음.
      마나 소모량 : 20 / 26 / 23 / 36 / 44
      범위 : 675
      재사용대기시간 : 1초
      데미지 : 50 / 70 / 90 / 110 / 130(+0.35AP)
      
     가랜
					
     	스텟
      	구분  기본 능력(+레벨 당 상승) 최종 수치
		체력		620(+840)	2048
		체력 재생	8.0(+0.5)	16.5
		공격력		66(+4.5)	142.5
		공격 속도	0.625(+3.65%)	1.013
		방어력		36(+3)		87
		마법 저항력	32.1(+0.75)	44.85
		사거리		175(-)		175
		이동 속도	340(-)		340
     
      패시브 : 8초간 적에게 피해 또는 스킬 적중이 없을경우 5초당 최대체력의 일정비만큼 회복.
              계산식 : 5초당 최대체력의 1.5 ~ 10.8&
      Q 스킬 : 가렌에게 적용된 모든 둔화 효과가 풀리며 다음 기본 공격시 침묵 상태이상 부여, 기본공격시 50의 거리를 순간적으로 이동함
      W 스킬 : (패시브) 유닛 처치시 영구적으로 0.25 방어력과 마법저항력 증가. 최대 30까지 중첩가능. 최대 중첩시 가랜의 방어력과 마법저항력이 10% 증가,
               (액티브) 일정시간동안 받는피해 30퍼 감소, 처음 0.75초간 보호막 및 60퍼센트 강인함 효과 부여
      E 스킬 : 검을 들고 회전. 가장 가까운 적에게 피해량 25%증가. 공격 횟수는 공격속도 비례, 6회 히트된 적 챔피언은 6초간 방어력 25% 감소됨.(6회 이수 추가공격은 적중시마다 효과지속시간 초기화함.), 치명타 적용시 33% 추가피해 가할수 있음. 몬스터에게 150% 피해 가함, 스킬 시전중 중단시 남은 스킬 지속시간만큼 재사용 대기시간 감소. 시전시강동안 유닛 충돌 무시함. cc기를 맞아도 캔슬되지 않음.
              공격속도 비례 계산식 7 + 아이템 및 레벨업으로 얻는 공격속도 25%마다 +1
      R 스킬 : 적 챔피언의 잃은 체력 비례한 피해을 추가로 입힘. 고정피해
                잃은체력 비례 피해 계산식 : 최대채력 - 현제채력 * (15% + 5 * 스킬 레벨)
                
     애쉬
     	
     	스텟
      	구분  기본 능력(+레벨 당 상승) 최종 수치
		체력       	 570(+87)          2049
		체력 재생	3.5(+0.55)	 12.85
		마나		 280(+32)	824
		마나 재생    7.0(+0.4)	13.8
		공격력  	     61(+2.96)	111.32
		공격 속도	0.658(3.33%)	1.030
		방어력		26(+3.4)	83.8
		마법 저항력  30(+0.5)	38.5
		사거리  	      600(-)	600
		이동 속도     325(-)	325
     
      패시브 스킬 및 기본공격시 2초간 대상의 속도 둔화 및 표식부여. 표식이 붙은 적을 공격시 추가피해를 가함. 치명타 대신 둔화 비율 증가.
      q스킬 : (패시브)기본공격시 스택 증가. 4회까지 중첩가능. 기본공격을 하지 않으면 1초당 1스택 감소.
              (액티브)4초간 공격속도 증가. 기본공격이 다발 공격으로 변경됨. 사용중 중첩 증가하지 않음.
      W 스킬 : 원뿔 형태로 화살을 발사함. 관통불가. 투사체 9개.
      E 스킬 : 지정한 위치를 향해 투사체 발사. 투사체가 지나가며 그 일대를 밝혀줌. 밣혀진 시아는 5초간 유지됨. 2회까지 저장가능.
      R 스킬 : 사거리 제한 없는 투사체를 발사함. 피격된 적은 투사체가 날아간 거리에 비례하여 기절.
      
     리산드라
					
     	스텟
      	구분  기본 능력(+레벨 당 상승) 최종 수치
		체력		550(+90)	2080
		체력 재생	7.0(+0.55)	16.5
		마나		475(+30)	985
		마나 재생	8.0(+0.8)	21.6
		공격력		53(+2.7)	98.9
		공격 속도	0.801(+1.36%)	0.801
		방어력		22(+3.7)	84.9
		마법 저항력	30(+0.5)	38.5
		사거리		550(-)	550
		이동 속도	325(-)	325
						
      패시브 : 주변에서 적 챔피언이 처치될시 적이 얼음 노예로 변환. 얼음노예는 4초간 적을 향해 이동하며 주변의 적을 둔화시킴. 그후 자폭하여 피해를 가함. 단 사망후 효과를 가진 챔피언은 그 효과가 끝난후 얼음노예화 됨.
      Q 스킬 : 투사체가 첫번쨰적에게 닿으면 뒤로 퍼져 광역피해로 전환됨. 첫번쨰 로 닿는 적에게는 둔화가 걸림.
      W 스킬 : 주변 적에게 마법피해를 입히고 일정시간동안 속박을 걸고 마법피해 가함.
      E 스킬 : 투사체를 던져 관통되는 적들에게 마법피해를 입함. 재사용시 투사체의 현제위치로 순간이동함.
      R 스킬 : 적에게 시전 : 1.5초 적을 기절, 자신에게 시전 : 2.5초 무적상태, 주변 적들에게 둔화 및 마법피해 가함.
