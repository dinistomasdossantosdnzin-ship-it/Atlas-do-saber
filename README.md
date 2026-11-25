# Atlas do Saber — DNZIN

Aplicação web estática em HTML, CSS e JavaScript. A autenticação Google usa Supabase Auth.

## Publicar na Vercel

1. No painel da Vercel, escolhe **Add New → Project**.
2. Importa o repositório **Atlas-do-saber** a partir do GitHub.
3. Mantém o framework como **Other** (site estático).
4. Deixa **Build Command** e **Output Directory** vazios; o ficheiro `index.html` está na raiz.
5. Clica em **Deploy**.

Os próximos commits na branch principal podem gerar implantações automáticas.

## Configurar autenticação Google

No Supabase, abre **Authentication → URL Configuration** e adiciona o endereço público da Vercel à lista de Redirect URLs, por exemplo `https://o-teu-projeto.vercel.app/**`. Define também o domínio final como Site URL.

Em **Authentication → Providers → Google**, ativa Google e configura o OAuth Client ID e Client Secret gerados no Google Cloud.

No Google Cloud, o URI de redirecionamento autorizado deve ser:

`https://wbsfgejmxaobzvjeqlyg.supabase.co/auth/v1/callback`

O HTML usa apenas a chave pública do Supabase. Não coloques credenciais secretas no HTML ou no GitHub.
