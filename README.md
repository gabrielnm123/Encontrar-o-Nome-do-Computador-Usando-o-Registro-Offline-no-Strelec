# Encontrar o Nome do Computador Usando o Registro Offline no Strelec

**Objetivo:** Acessar o nome do computador de um Windows instalado no HD usando o Editor de Registro (Registry Editor) no ambiente Strelec.

## 1. Inicie o Editor de Registro
- Abra o **Registry Editor** (Editor de Registro) no Strelec.

## 2. Carregue o Hive do Registro do Sistema
1. Clique em **HKEY_LOCAL_MACHINE**.
2. No menu superior, clique em **File** e depois em **Load Hive**.
3. Navegue até a pasta do Windows montado, geralmente `C:\Windows\System32\Config`.
4. Selecione o arquivo **SYSTEM** e clique em **Open**.
5. Quando solicitado, nomeie o hive como **OfflineSystem** (ou outro nome que preferir).

## 3. Navegue até a Chave do Nome do Computador
1. No Editor de Registro, expanda **HKEY_LOCAL_MACHINE**.
2. Expanda a chave que você carregou (exemplo: **OfflineSystem**).
3. Siga o caminho:
   ```
   OfflineSystem\ControlSet001\Control\ComputerName\ComputerName
   ```

## 4. Verifique o Nome do Computador
- No lado direito, localize o valor **`ComputerName`**.
- O dado associado a esse valor mostrará o nome do computador.

## 5. Descarregue o Hive
1. Após verificar o nome do computador, clique com o botão direito na chave **OfflineSystem** (ou o nome que você deu) em **HKEY_LOCAL_MACHINE**.
2. Escolha **Unload Hive** para evitar problemas futuros.

Esse procedimento permite visualizar o nome do computador do sistema Windows montado sem precisar inicializar o sistema operacional. Se precisar de mais alguma informação ou ajuda, me avise!
