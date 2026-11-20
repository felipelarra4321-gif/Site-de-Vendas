# Casa em Ordem

Catálogo responsivo de potes com sacola de compras e envio do pedido pelo WhatsApp. O projeto usa HTML, CSS e JavaScript sem dependências e pode ser publicado como site estático na Vercel.

## Abrir localmente

Abra `index.html` no navegador. Para uma experiência local semelhante à hospedagem, rode um servidor estático na pasta, por exemplo `npx serve .`.

## Publicar na Vercel

1. Envie estes arquivos para um repositório Git.
2. Importe o repositório na Vercel.
3. Escolha **Other** como preset, deixe o build command vazio e defina `.` como diretório de saída.
4. Publique. Não há variáveis de ambiente necessárias para a versão estática.

## Configurar o vendedor

No rodapé, abra **Área do vendedor**. A senha inicial é `1234`. Na aba **Configurações**, troque a senha e informe o WhatsApp com código do país e DDD, apenas números (exemplo: `5511999999999`). Na aba **Produtos**, cadastre, edite, oculte ou remova itens. Na aba **Pedidos**, registre manualmente pedidos recebidos no WhatsApp e atualize seus status. É possível salvar um arquivo de cópia e restaurá-lo em outro navegador.

## Limites desta versão estática

O catálogo, a senha e a sacola são salvos no `localStorage` do navegador. Assim, alterações feitas no navegador do vendedor não aparecem automaticamente para clientes em outros dispositivos, e o catálogo volta aos valores iniciais em um navegador novo. A senha é uma barreira simples da interface, não uma autenticação segura; como os arquivos são públicos, não use essa área para dados privados. Para uso real com catálogo compartilhado e acesso protegido, conecte uma base de dados e autenticação (por exemplo, Supabase) e implemente as operações por um serviço de backend.

O site monta a mensagem e abre o WhatsApp com os itens e o total dos produtos. O vendedor ainda precisa copiar os detalhes da conversa para a aba **Pedidos** manualmente; a confirmação de envio ao WhatsApp não cria um registro no painel. Frete e pagamento ficam para combinar diretamente com o vendedor.
