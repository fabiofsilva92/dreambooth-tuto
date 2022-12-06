# Criar avatar com Dreambooth

1. Para iniciar, escolha ou tire 20 fotos de seu rosto, focando nos detalhes e angulos, após isso utilize a ferramenta [BIRME](https://www.birme.net/?target_width=512&target_height=512&image_format=jpeg&quality_jpeg=100) para recortar suas fotos em 512x512.


2. Crie sua conta no [Huggiing Face](https://huggingface.co/) e crie um token com a permissão de escrita (write)
![image](https://user-images.githubusercontent.com/61157010/205781645-5118bf6c-ef9f-46e6-8289-ecd0880034fe.png)
![image](https://user-images.githubusercontent.com/61157010/205781770-9fa08487-c634-4a8e-a239-960f819f2ff0.png)

3. Entre na pagina do [Stable Difusion](https://huggingface.co/runwayml/stable-diffusion-v1-5) e autorize a interação do modelo com sua conta.

4. Entre com seu login google no [Colab], clique em arquivo -> abrir notebook e selecione a aba do github e cole este link https://github.com/ShivamShrirao/diffusers/tree/main/examples/dreambooth
![image](https://user-images.githubusercontent.com/61157010/205784837-cd8d9809-6ccf-4acd-b757-e7779a03bf7a.png)
![image](https://user-images.githubusercontent.com/61157010/205784917-71f85be7-7d7a-4f03-a358-56464f2f3bf2.png)

5. Após isso devemos iniciar as configurações, comece colocando a token criada no Hugging Face neste campo:
![image](https://user-images.githubusercontent.com/61157010/205785292-5505fb50-ba1e-44e1-a4a7-57c3f36e2111.png)

6.A próxima parte a ser configurada é a concepts_lists, substitua as informações colocando o nome da token criada no Hugging Face no lugar conforme o exemplo a seguir:
![image](https://user-images.githubusercontent.com/61157010/205785688-9538edf0-4cb4-4d5b-b9d6-0dce1ecb0827.png)
Obs: sem as chaves, no campo class_prompt e class_data_dir deve vir escrito "dog", basta mudar para person.

7.No campo "save_sample_prompt" coloque o nome da sua token, sem as chaves.
![image](https://user-images.githubusercontent.com/61157010/205786084-e8161a9a-513a-4f9b-af0e-8311581e557a.png)

8.No campo WEIGHTS_DIR coloque conforme a figura -> stable_diffusion_weights/zwx: 
![image](https://user-images.githubusercontent.com/61157010/205786175-41660e03-6fb9-4a4c-8bf6-50e571ed7794.png)

9.Na seção Inference, muda "model_path" de WEIGHTS__DIR para "stable_diffusion_weights/zwx/800"
![image](https://user-images.githubusercontent.com/61157010/205786450-9b8644a4-9a32-45c6-9725-827904e49d22.png)

10. Após isso podemos começar a executar o ambiente onde irá gerar as imagens. Comece executando todos os blocos, não pule nenhum, clique no botao "play" e espere a execução, após finalizar, passe para o proximo. 
![image](https://user-images.githubusercontent.com/61157010/205786874-7334cf97-1aea-407e-9902-7df246bbfda5.png)
Quando se deparar com o bloco [7], clique para executar, este bloco irá criar uma pasta com o nome da sua token, arraste todas suas imagens redimensionadas para esta pasta:
![image](https://user-images.githubusercontent.com/61157010/205787000-2a7d37e1-53e9-42a4-bd7d-71eff5dd9d6a.png)
apos isso clique no botão cancelar do bloco, e passe para o proximo.
