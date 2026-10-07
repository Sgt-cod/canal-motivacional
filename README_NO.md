# Canal norueguês (Det Forsvunne Forge) — como ativar

Copie os arquivos deste pacote para a raiz do repositório (sobrescrevendo os existentes).
O canal Convergência continua igual: sem `CONFIG_FILE`, tudo usa `config.json`.

## Secrets novos (GitHub → Settings → Secrets)
YOUTUBE_CLIENT_ID_NO, YOUTUBE_CLIENT_SECRET_NO, YOUTUBE_REFRESH_TOKEN_NO
(os demais — GEMINI, PEXELS, TELEGRAM — são reaproveitados).

## Preencher em config_no.json (itens marcados TROQUE)
contexto_nicho, documento_estilo (2–3 trechos em norueguês), temas_reflexao.
Ajuste termos_pesquisa_validados ao nicho (em inglês, para o Pexels).

## Assets
Coloque vinheta em assets/no/intro/ e CTA em assets/no/cta/ (vazio = sem vinheta/CTA).

## Rodar
Actions → "Gerar e Publicar Vídeo Longo (… NO)". Teste antes com PULAR_UPLOAD="true".

## Fluxo no Telegram
Tema → (por segmento) texto NO + tradução PT-BR → você manda o áudio → revisão de cada clipe
(trecho NO + PT-BR + mídia sugerida) → thumbnail com título/texto traduzidos.
Sem áudio no tempo limite, o workflow é cancelado (nada é publicado).

## Agendamento (Telegram) — vale pros dois canais
Depois da thumbnail, o bot pergunta: 🚀 Publicar agora ou 📅 Agendar. Ao agendar, mande
"25/12 18:30", "amanhã 19:00", "hoje 21h" ou "18:30" (no fuso de `agendamento_telegram.fuso_horario`).
O vídeo sobe privado e o YouTube o publica sozinho na hora marcada (publishAt).
No canal NO a confirmação mostra também o horário de Oslo.
`se_sem_resposta`: "agora" (padrão) ou "cancelar".
