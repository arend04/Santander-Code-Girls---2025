Fazer o desenho da arquitetura AWS EC + EBS ou S3 + Lambda.   
Optei por fazer os dois para conhecimento.


<h1>🖥️ Modelo 1: EC2 + EBS + RDS

<h3>(o jeito “tradicional” de rodar sistemas na nuvem)  <br><br>

<img width="8044" height="2144" alt="image" src="https://github.com/user-attachments/assets/ae6ddca8-14fb-47ed-a6fb-f113ac66edbf" />  <br><br>

Imagine que você tem uma loja online.

Para rodar sua loja, você precisa de um computador sempre ligado. Esse computador é a EC2 (um servidor virtual da AWS).

O computador precisa de um HD para guardar arquivos (fotos, vídeos, documentos). Esse HD é o EBS.

Ele também precisa de um banco de dados para salvar informações organizadas (como clientes, pedidos, produtos). Esse banco é o RDS.

Mas só isso não basta. Você precisa deixar sua loja rápida, segura e confiável:

O Route 53 é como uma lista telefônica: transforma o endereço da loja (ex: www.minhaloja.com
) no endereço real do servidor.

O CloudFront é como uma rede de filiais espalhadas pelo mundo, que guardam cópias das páginas para que clientes de longe acessem mais rápido.

O ELB (Load Balancer) é como um gerente que divide os clientes entre vários computadores, para nenhum ficar sobrecarregado.

O Auto Scaling é como contratar mais atendentes na hora do pico: ele cria novos computadores automaticamente.

O IAM é como um segurança que controla quem pode entrar em cada parte da loja.

👉 Em resumo:
Você tem controle total sobre seus computadores, mas também precisa cuidar deles (manutenção, atualizações, escalabilidade).  <br><br><br>



    
<h1>⚡ Modelo 2: S3 + Lambda + DynamoDB (Serverless)

<h3>(o jeito “moderno” e automático de rodar sistemas na nuvem)  <br><br>

<img width="8996" height="2404" alt="image" src="https://github.com/user-attachments/assets/7713c68f-d6e7-46df-8991-e9fc4bcb9473" />  <br><br>

Agora imagine que em vez de manter computadores ligados, você usa serviços que funcionam sob demanda, só quando necessário.

O S3 é como um depósito infinito e barato onde você guarda todos os arquivos (fotos, vídeos, PDFs).

O DynamoDB é como uma prateleira mágica que cresce sozinha para guardar informações (clientes, pedidos etc.), sem você precisar organizar nada.

A Lambda é como um funcionário temporário: só aparece quando precisa fazer um trabalho (ex: processar um arquivo, validar dados) e depois some — você só paga pelo tempo que ele trabalhou.

E, para deixar tudo ainda melhor:

O Route 53 e o CloudFront continuam funcionando como na primeira arquitetura (endereços e velocidade).

O API Gateway é como um porteiro: recebe pedidos de clientes e entrega para a Lambda.

O SQS (fila) é como uma fila organizada no caixa: garante que todos os pedidos sejam atendidos, mesmo se chegarem muitos ao mesmo tempo.

O SNS (notificações) é como um sistema de avisos: manda mensagem quando algo foi concluído.

O CloudWatch é como uma câmera de segurança: monitora tudo e mostra relatórios.

O IAM continua como o segurança que controla quem pode fazer o quê.

👉 Em resumo:
Você não precisa cuidar de servidores, nem se preocupar se vai ter 10 ou 10.000 acessos. Tudo cresce e encolhe automaticamente. Você paga apenas pelo que usa.





