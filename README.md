# Desafio Villani

Projeto estático pronto para GitHub Pages + Firebase Firestore.

## Publicar
1. Coloque `index.html`, `style.css` e `app.js` na raiz do repositório.
2. GitHub > Settings > Pages > Deploy from a branch > `main` / root.
3. Firebase Console > Authentication > Sign-in method > habilite **Anonymous**.
4. Firebase Console > Firestore Database > crie o banco se ainda não existir.
5. Em Firestore > Rules, cole o conteúdo de `firestore.rules` e publique.
6. O ranking usa `where(turma)` + `orderBy(pontos)`. Se o Firebase solicitar um índice composto ao primeiro acesso, clique no link exibido no erro do Console e crie o índice para `resultados`: `turma` + `pontos` (descendente).

## Estrutura
- 7º B/C: Educação Financeira (4 questões)
- 8º B/C: Educação Financeira (4 questões)
- 9º B/C: Matemática (10 questões)
- Ordem das questões e alternativas embaralhada a cada tentativa.
- Resultados gravados na coleção `resultados`.
- Ranking por turma.
- Compartilhamento nativo/WhatsApp.
- Botão do professor envia para +55 19 99647-0380.

## Segurança
A configuração web do Firebase fica no cliente por design. O que protege o banco são Authentication + Firestore Security Rules. Não use regras `allow read, write: if true` em produção.
