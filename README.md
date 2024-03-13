- 👋 Hi, I’m @tygas137
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
tygas137/tygas137 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

# Configurando o navegador
driver = webdriver.Chrome(executable_path="caminho_para_o_executavel_do_chrome_driver")

# Navegando até o Google
driver.get("https://www.google.com")

# Encontrando o campo de busca e inserindo a consulta
search_box = driver.find_element_by_name("q")
search_query = "Exemplo de consulta"
search_box.send_keys(search_query)
search_box.send_keys(Keys.RETURN)

# Aguardando alguns segundos para visualização
driver.implicitly_wait(5)

# Fechando o navegador
driver.quit()
