# Locale 적용 과정

## [Locale 설정 플로우](./locale-flow.md)에 따라 쿠키를 설정
* 자세한 내용은 기획이 필요(로그인 방식에 대한 기획 등)
## 번역 방식에 따른 언어 팩의 다운로드 및 변환
- 이 부분은 번역을 하는 방식에 따라 다를 예정이기 때문에 추후 개발 예정

언어 Json의 형식
``` json
{
  "HomePage": {
    "title": "Hello world!"
  }
}
```
## 설정된 Locale 쿠키를 기반으로 하는 웹페이지의 언어 설정

``` tsx
import { cookies } from "next/headers";
import { getRequestConfig } from "next-intl/server";

export default getRequestConfig(async () => {
  const store = await cookies();
  const locale = store.get("locale")?.value || "en-US";

  return {
    locale,
    messages: (await import(`../../messages/${locale}.json`)).default,
  };
});
```
1. locale이라는 이름의 쿠키의 값을 읽어옴
2. locale과 같은 이름을 가진 json으로 언어팩을 로딩
### 서버 사이드에서
``` tsx
import {getTranslations} from 'next-intl/server';
 
export default async function HomePage() {
  const t = await getTranslations('HomePage');
  return <h1>{t('title')}</h1>;
}
```
### 클라이언트 사이드에서
- 클라이언트 사이드에서는 컨텍스트 공급을 위해 NextIntlClientProvider가 필요
``` tsx
import {NextIntlClientProvider} from 'next-intl';
 
type Props = {
  children: React.ReactNode;
};
 
export default async function RootLayout({children}: Props) {
  return (
    <html>
      <body>
        <NextIntlClientProvider>{children}</NextIntlClientProvider>
      </body>
    </html>
  );
}
```
- 실제 사용
``` tsx
import {useTranslations} from 'next-intl';
 
export default function HomePage() {
  const t = useTranslations('HomePage');
  return <h1>{t('title')}</h1>;
}
```
