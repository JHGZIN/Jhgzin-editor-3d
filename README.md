# JH Model Studio

Editor 3D leve para Android, com interface escura, detalhes ciano e vermelho, projetado para funcionar localmente sem depender de bibliotecas ou serviços online.

## Recursos desta versão
- Viewport 3D com grade, eixos e órbita por toque/arrasto; zoom por gesto de pinça/roda.
- Primitivas: cubo, esfera, cilindro e plano.
- Hierarquia de objetos, seleção, duplicação, exclusão, renomeação e visibilidade.
- Inspetor para posição, rotação, escala e cor.
- Salvamento automático local no aparelho e exportação/importação do projeto `.jhmodel`/JSON.
- Exportação de malhas `.obj` e `.glb` para a pasta Downloads do Android.
- Workflow GitHub Actions para compilar APK de depuração.

## Compilar APK pelo GitHub
1. Envie o conteúdo desta pasta ao repositório, mantendo `.github/workflows/build.yml`.
2. Abra Actions → Build APK → Run workflow.
3. Ao terminar, baixe o artefato `JH-Model-Studio-APK`.

Também é possível compilar localmente com JDK 17, Android SDK 34 e Gradle 8.7 ou superior: `gradle assembleDebug`.

## Observações
Esta é uma primeira versão funcional e leve. A viewport desenha e projeta malhas primitivas por software, não é um motor de renderização avançado. A ferramenta de mover/rotacionar/escala permite editar valores no inspetor; os botões de ferramenta servem para indicar o modo atual, mas ainda não há manipuladores 3D arrastáveis. OBJ exporta geometria; cores são mantidas no projeto e no GLB. Não há texturas, escultura, rigging, animação, Boolean, importação de malhas externas ou renderização PBR avançada nesta versão.
