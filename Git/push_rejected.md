## Error

`git init`을 하고 `git push`할 때,

```
git push -u origin main
To https://github.com/keemdy/TIL.git
 ! [rejected]        main -> main (non-fast-forward)
error: 레퍼런스를 'https://github.com/keemdy/TIL.git'에 푸시하는데 실패했습니다
힌트: 현재 브랜치의 끝이 리모트 브랜치보다 뒤에 있으므로 업데이트가
힌트: 거부되었습니다. 푸시하기 전에 ('git pull ...' 등 명령으로) 리모트
힌트: 변경 사항을 포함하십시오.
힌트: 자세한 정보는 'git push --help'의 "Note about fast-forwards' 부분을
힌트: 참고하십시오.
```

위와 같은 에러 발생

## 원인

`git pull origin main`을 하지 않아서  
`.gitignore`이나 `README.md`를 가져오지 못해 발생한 문제  
뒤늦게 실행해도 해결되지 않는다.

## 해결

```
git push origin +master
```

or

```
git pull origin --allow-unrealated-histories
```

한 후에 push
