# App Mobile - Monitoramento de Escolas (Recife)

Aplicativo mobile desenvolvido em React Native (usando Expo) como requisito da atividade de recuperação de Desenvolvimento de App Mobile Individual. O objetivo é mapear as escolas municipais do Recife integrando dados abertos com a localização do usuário.

## Funcionalidades Implementadas
- **Geolocalização:** Captura a localização atual do dispositivo.
- **Integração com API Externa:** Consumo da API pública do portal Dados Recife para listar escolas municipais.
- **Integração com Backend:** Envia as coordenadas do usuário e os dados da escola escolhida para uma API RESTful própria (Node.js).
- **Navegação:** Utilização do Expo Router (baseado no React Navigation) para transição entre a tela principal e a tela de histórico.

## Como configurar e rodar o projeto localmente

### 1. Pré-requisitos
- Node.js instalado na máquina.
- Aplicativo **Expo Go** instalado no smartphone.
- O servidor backend (disponível no outro repositório) precisa estar rodando na máquina.

### 2. Instalação
No terminal, dentro da pasta do projeto, instale as dependências:
\`\`\`bash
npm install
\`\`\`

### 3. Configuração de Rede (IMPORTANTE)
Para que o aplicativo consiga se comunicar com o backend local, é necessário configurar o IP da sua máquina:
1. Descubra o seu endereço IPv4 local (no Windows, use `ipconfig` no CMD).
2. Abra os arquivos `app/(tabs)/index.tsx` e `app/(tabs)/explore.tsx`.
3. Procure pela palavra `SEU_IP_AQUI` na URL do `fetch` e substitua pelo seu endereço IPv4.
   - *Exemplo de como deve ficar: `http://192.168.1.15:3000/salvar`*

### 4. Executando o App
Inicie o servidor do Expo com o comando:
\`\`\`bash
npx expo start
\`\`\`
Um QR Code será gerado no terminal. Escaneie-o com a câmera do seu celular (iOS) ou com o aplicativo Expo Go (Android) para abrir a aplicação.