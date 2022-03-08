# php8-xdebug

## VSCODE

Instale o plugin no VSCODE

Nome: PHP Debug
ID: xdebug.php-debug
Descrição: Debug support for PHP with Xdebug
Versão: 1.25.0
Editor: Xdebug
Link do Marketplace do VS: https://marketplace.visualstudio.com/items?itemName=xdebug.php-debug

## Browser

Instale no browser o plugin do Xdebug
https://xdebug.org/docs/step_debug#browser-extensions

1. Clique com o botão direito do mouse no ícone do plugin
2. Seleciona Opções
3. Na seção IDE Key selecione "Other" e preencha com a mesma key definada nas configurações do XDEBUG, ou seja, VSCODE (xdebug.idekey=VSCODE)
4. Clique em Salvar

## VSCODE

Abra o Terminal do VSCODE

** Nota: meu VSCODE está configurado dentro do WSL2

Execute o comando para criar o container
```
docker-compose build
```

Execute o comando para subir o container
```
docker-compose up
```

## index.php

Abra o arquivo app/index.php e marque alguns breakpoints e pressione F5, entrará no modo  de debug

## Browser

1. Acesse a página http://localhost:8000 e você verá o debug no vscode
2. Caso a página seja executada clique no ícone da extensão do xdebug e marque a opção DEBUG


## Firewall

Caso não funcione, talvez seja necessário criar um regra de firewall no Windows, no Powershell execute (como admin)
```
New-NetFirewallRule -DisplayName "WSL" -Direction Inbound  -InterfaceAlias "vEthernet (WSL)"  -Action Allow
```

### Fonte / Referências:

https://dev.to/getjv/xdebug-3-docker-laravel-vscode-52bi
https://gist.github.com/antfroger/1f2b24fdba0f215a41c8a94e8aa062f7