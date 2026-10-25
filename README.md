# 천체 중력가속도 계산기

구대칭 천체 바깥에서 거리별 중력가속도 크기 계산

- Plan ID: E055
- App: https://nanalab.kr/eng-gravity-at-radius/
- Repository: https://github.com/NaNaCompany/eng-gravity-at-radius
- Formula: `g = GM/r²`
- Output: 중력가속도 크기 g

## Model

M,r>0. 천체 외부의 구대칭 뉴턴 중력만 계산한다. r은 중심거리다. 자전에 의한 원심 효과·다른 천체·내부 밀도분포는 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `9.82030229338564`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
