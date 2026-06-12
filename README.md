# TAKAHASHI LAB. — Photographer Portfolio

Portfolio website for Hayato Takahashi / TAKAHASHI LAB.

## Pages

| File | Description |
|------|-------------|
| `index.html` | Main portfolio — ART viewer, WORKS grid, ABOUT, CONTACT |
| `category.html` | Per-category photo gallery (`?cat=TITLE`) |
| `project.html` | YOUR PROJECT — shoot inquiry page |

## Local development

```bash
python3 -m http.server 8765
# → http://localhost:8765/
```

No build tools, no dependencies. Pure HTML/CSS/JS.

## Asset structure

```
assets/
  web/
    ART/           # 29 art images (max 3840px, JPEG q95)
      thumbs/      # 29 thumbnail strips (160px)
    works/         # Per-category portfolio images (max 3000px, JPEG q95)
      ビジュアル撮影/
      宣材写真/
      アパレル人物撮影/
      アパレルスタジオ撮影/
      アパレル物撮り/
      Leport 写真/
      アーティスト写真/
      ウェディングフォト/
      成人式前撮り/
      マタニティフォト/
      モデル撮影/
      ライブ撮影/
      スポーツ撮影/
      中判フィルムカメラ/
      キャンドル/
      シーシャ　撮影/
      お酒物撮り/
      物件撮影/
      工事　プロモーション/
    movie/
      running-movie-1080p-crf18.mp4   # 1080p H.264, BT.709, ~123MB
    1.jpg          # Profile photo (max 2400px, JPEG q95)
```

Original source files (ART/, TAKAHASHI LAB インスタ投稿用/, RUNNING MOVIE.mov) are stored locally and excluded from git via `.gitignore` — they exceed GitHub's 100 MB file limit.

## Deploy

Hosted on [Netlify](https://www.netlify.com/) — see `netlify.toml` for cache and header settings.

- HTML files: `Cache-Control: no-cache` (always fresh)
- Images / video: `Cache-Control: immutable, 1 year` (fingerprinted by path)

## Contact

**Email:** takahashilab.create@gmail.com  
**Instagram:** [@hayato.jpg](https://www.instagram.com/hayato.jpg/)
