
- Biblioteca = curl_cffi (melhor que requests)
- Selium driverless = biblioteca top pra web_scrapping
- Navegadores_headless para automação.
- Web_scraping com android.

Hoje em dia é MUITO facil identificar um navegador, porque eles rastreiam TUDO, site pra ver oque os sites sabem sobre você:
	https://amiunique.org/

ADB android é muito melhor pra scraping e automação, e funciona perfeitamente!

Precisamos instalar um compilador pra controlar o android do PC (que vai rodar no baixo nivel em C), e conseguimos jogar essa automação dentro de um servidor e ela ficar rodando infinitamente sem consumir seu pc.

Passo a passo:

Video completo no youtube: https://www.youtube.com/watch?v=QM_DAcAjBp8

1 - Instalar emulador
2 - instalar root no emulador
3 - Baixar Termux no android (Repositorio do dono do canal)
5- Mudar nome do termux, tirar o main
6- Você só precisa instalar numpy e pandas (mas você pode instalar todos os pacotes)
	Pode usar varias bibliotecas, selenium e tudo!

RESUMO: Vamos instalar o termux com python no emulador de android e depois controlar o termux via terminal do pc.

O problema de rodar os scrips com python é que vai consumir bastante memoria, mas em C é muito mais leve!

Importante: instale o magisk para ofuscar que é um emulador.