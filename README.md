# Simple Chair — Three.js 3D Viewer

Atividade prática de visualização 3D interativa usando **Three.js**, com modelo obtido do **Sketchfab**.

---

## Modelo utilizado

| Campo       | Informação |
|-------------|-----------|
| **Nome**    | Simple Chair |
| **Origem**  | [https://sketchfab.com/3d-models/simple-chair-0efe6f9479c044cda34265b75b067704] |
| **Licença** | CC Attribution |
| **Formato** | `.glb` (GLTF Binary) |

> Substitua o link acima pelo link exato do modelo que você baixou no Sketchfab.

---

## Estrutura do projeto

```
/
├── index.html          # Aplicação principal
├── simple_chair.glb    # Modelo 3D (baixado do Sketchfab)
└── README.md
```

---

## Como executar

O arquivo `index.html` usa módulos ES (`type="module"`) e importa o Three.js via CDN com **importmap**, portanto **precisa ser servido por um servidor HTTP** — não funciona com `file://`.

### Opção 1 — VS Code Live Server
Instale a extensão **Live Server** e clique em *"Go Live"*.

### Opção 2 — Python (sem instalação)
```bash
python -m http.server 8080
# acesse http://localhost:8080
```

### Opção 3 — Node.js / npx
```bash
npx serve .
```

---

## Critérios atendidos

| Critério | Status |
|----------|--------|
| Modelo GLB carregado via `GLTFLoader` | ✅ |
| `OrbitControls` — rotação, zoom e pan | ✅ |
| Luz direcional (`DirectionalLight`) configurada | ✅ |
| Luz ambiente (`AmbientLight`) configurada | ✅ |
| Loop de animação com `requestAnimationFrame` | ✅ |
| Resize handler (câmera + renderer) | ✅ |
| Código legível, variáveis bem nomeadas | ✅ |
| Modelo de natureza adequada (objeto/mobiliário) | ✅ |

---

## Dependências

Todas via CDN (sem instalação local):

- [Three.js r165](https://threejs.org/) — engine 3D
- `GLTFLoader` — carregamento do modelo `.glb`
- `OrbitControls` — controle de câmera
