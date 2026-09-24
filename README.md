# Forms Campos do Jordão

Página de pré-inscrição da Expedição Campos do Jordão da Usina do Jet, realizada de 21 a 23 de agosto de 2026. Projeto construído com React, TypeScript, Vite e Tailwind CSS.

## Desenvolvimento

```bash
npm install
npm run dev
```

## Validação

```bash
npm run lint
npm run build
```

## Integração com o Basin

O formulário envia os dados e os documentos ao Basin no endpoint `https://usebasin.com/f/4c202af3081c`. A geração do contrato não faz parte desta etapa.

O endpoint está definido diretamente em `src/components/ExpeditionForm.tsx`; não é necessário configurar variável de ambiente local ou na Vercel. A variável antiga `VITE_BASIN_ENDPOINT`, se ainda existir no painel, não é utilizada pelo formulário. Para mudar o destino futuramente, altere o endereço no código e publique novamente o projeto.

O envio usa `multipart/form-data`, mantém os documentos em seus formatos originais e apresenta os campos no painel do Basin com nomes legíveis, incluindo o protocolo da inscrição. Um endpoint inválido impede o envio.
