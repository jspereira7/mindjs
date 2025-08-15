Conteudo retirado do forum black sider:

Autor: **Nini**

Sei que já te passei os programas no post anterior, pórem vou te dar mais um caminho e também deixar regsitrado pro pessoal que vir aqui procurar respostas...

Mano seguinte: **TikTok não tem uma API pública** de postagem aberta pra geral, então a gente vai precisar de uma abordagem mais ‘raiz’. 

A parada é entender como o TikTok autentica e valida essas requisições, e aí interceptar tudo no processo. Pra começar, você pega uma ferramenta como **Burp Suite** ou **OWASP ZAP** (essas são clássicas pra interceptar tráfego). Tu abre o TikTok Web ou app no celular (melhor ainda se usar num emulador pra não estourar nada no seu device). Aí intercepta tudo que rola ali nas requisições

O segredo é pescar os cabeçalhos que o TikTok usa pra validar: 

*"`Authorization`, `Cookies`, `User-Agent`, e `X-Tt-Token`. "*

Esses tokens e cookies são o ouro.

Cada sessão que abre carrega uns identificadores únicos, e a gente só precisa replicar eles depois nos nossos requests

Agora, se não quiser replicar o login toda hora, tem uma manha que é **usar os cookies de uma sessão autenticada**. 

O que você faz é logar uma vez no TikTok pelo navegador, captura esses cookies todos e usa direto nas suas requests. 

Pra isso, cara, **Puppeteer** (pra Node.js) e **Selenium** (pra Python) são as ferramentas perfeitas pra isso. 

Com elas você consegue automatizar o login, capturar os cookies e depois jogar eles nas requisições que precisar

Depois, vem a parte do upload. 

Normalmente o TikTok divide o upload em duas partes: primeiro manda o arquivo de vídeo, e aí rola a request de publicação mesmo.

O lance aqui é enviar o vídeo como `multipart/form-data` e estruturar o post exatamente igual como o TikTok espera. 

No seu script, os headers e o corpo da request precisam tá iguais, tipo cópia e cola do que capturou com o Burp ou OWASP.

Isso pode ser feito em Python, na biblioteca Requests. Dá uma olhada no esqueleto do código:

import requests

headers = {  
    "Authorization": "Bearer SEU_TOKEN",  
    "User-Agent": "Mozilla/5.0 ...",  
    # Outros cabeçalhos que tu pescou  
}

data = {  
    "caption": "Texto do seu post",  
    "schedule_time": "Horário de postagem, se aplicável"  
}

files = {  
    "video": open("caminho/do/video.mp4", "rb")  
}

response = requests.post("https://api.tiktok.com/upload_endpoint", headers=headers, data=data, files=files)  
print(response.json())  
 

A chave é usar os cookies da sessão ou o `Authorization` token capturado e manter tudo idêntico pra não levantar suspeita. 

Mas se precisar fazer postagens programadas, tem um macete a mais: usa um **scheduler** tipo o cron no Linux ou a Tarefa Agendada no Windows. 

Isso roda o script automaticamente no horário que definir. Outra opção dark é usar o **APScheduler**, um scheduler Python que roda no seu script direto e deixa tudo programado, tipo:

from apscheduler.schedulers.blocking import BlockingScheduler

scheduler = BlockingScheduler()  
scheduler.add_job(post_video, 'date', run_date='2024-11-12 08:00:00')  
scheduler.start()  

Isso chama a função `post_video` que roda o script de upload de forma automática, sem precisar de intervenção manual

Agora, pra não ter sua conta banida, manja? Faz um esquema usando **IPs rotativos** e dá um delay entre as requisições, tipo simulando comportamento humano. Nada de estourar limite de request, ou o TikTok te pega fácil. 

Outra coisa que ajuda: testa isso num ambiente de teste antes de rodar tudo de uma vez

Qualquer coisa a mais que precisar ajustar ou que você não entendeu me avisa irmão...