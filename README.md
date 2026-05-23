# AIT Storage

GitHub Pages로 공개하는 이미지 저장소입니다. `index.html`은 저장소의 이미지 파일을 자동으로 읽어 카드형 갤러리로 보여주는 정적 이미지 뷰어입니다.

## 이미지 뷰어

- 페이지: https://comeback-zunny.github.io/AIT-Storage/
- 저장소의 `playing`, `history`, `app-icon` 폴더를 GitHub API로 읽어 이미지 목록을 구성합니다.
- 게임명, 폴더명, 파일명으로 검색할 수 있습니다.
- 첫 화면에서 `PLAYING`, `HISTORY`, `앱 아이콘` 중 볼 카테고리를 선택합니다.
- 카테고리 화면에서는 폴더별로 최대 5장만 보여주고, `전체 보기`로 해당 폴더의 모든 이미지를 확인할 수 있습니다.
- `playing/thumbnail.png`, `history/thumbnail.png`, `app-icon/thumbnail.png`는 첫 화면 버튼 배경으로 사용합니다.
- 썸네일을 클릭하면 원본 이미지를 모달로 확인하고 이전/다음 이미지로 이동할 수 있습니다.

## 폴더 구조

이미지는 아래 구조로 저장합니다.

```text
playing/
  thumbnail.png
  게임명/
    이미지파일.png

history/
  thumbnail.png
  게임명/
    이미지파일.png

app-icon/
  thumbnail.png
  아이콘파일.png
```

하위 폴더를 추가하면 뷰어에서 앨범처럼 함께 표시됩니다.

```text
playing/
  게임명/
    앨범명/
      이미지파일.png
```

## 지원 형식

다음 확장자의 이미지 파일을 표시합니다.

- `.jpg`
- `.jpeg`
- `.png`
- `.gif`
- `.webp`
- `.avif`

## 업데이트 방법

1. 알맞은 폴더에 이미지를 추가합니다.
2. 변경사항을 `main` 브랜치에 커밋하고 푸시합니다.
3. GitHub Pages가 배포되면 이미지 뷰어에서 새 파일을 확인합니다.

`index.html`은 별도 빌드 과정 없이 동작하는 단일 정적 파일입니다.
