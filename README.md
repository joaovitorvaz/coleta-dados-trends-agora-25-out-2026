# Trends ao vivo — Brasil

Agente `coleta trends-now-agent` · config `trends_agora_20261025`.

A cada ciclo (~5 min):

1. Lista fresca Twitee BR + Nitter `/trends` → coleta em `termos/trends_agora_br/`
2. **Boost fixo** nordeste + nordestino → `termos/nordeste/` e `termos/nordestino/`
3. No snapshot, `nordeste_related` lista os TT do momento que batem com nordeste/gentílicos (não só os boosts)

```bash
cd ../projeto-coleta
coleta trends-now-agent --mode daemon
# um ciclo:
coleta trends-now-agent --mode once
```

Snapshot: `data/manifests/trends_live_snapshot.json`
