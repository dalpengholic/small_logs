---
layout: post
title: Golang test
subtitle: 
categories: Golang
tags: [Golang, test]
---
고랭 테스트 코드 만들기
1. 테스트 코드는 테스트 대상이 있는 폴더에 같이 있어야 하고 파일명이 `.._test.go` 이어야 함
```zsh
 ➜ ls
fruitpkg.go      fruitpkg_test.go
```

2. 패키지 이름은 테스트 대상과 달라야 함

3. Import를  "testing"(테스터) 과 "gomarket/fruit"(테스트 대상) 둘다 해줘야 함
```Golang
import "testing"
import "gomarket/fruit"
```

4. 테스트 함수는 `func Test.... (t *testing.T)` 형태여아 함
```Golang
func TestNewFruitItem(t *testing.T){
	result1 := fruit.NewFruitItem("apple", 0.7)
	if result1.Name != "apple" {
		t.Errorf("결과1 값은 apple 이어야 합니다.")
	}
	if result1.Weight != 0.7 {
		t.Errorf("결과1 무게는 0.7 이어야 합니다.")
	}


	result2 := fruit.NewFruitItem("banana", 0.7)
	if result2.Name != "banana" {
		t.Errorf("결과1 값은 banana 이어야 합니다.")
	}
	if result2.Weight != 0.7 {
		t.Errorf("결과2 값은 0.7 이어야 합니다")
	}
}
```