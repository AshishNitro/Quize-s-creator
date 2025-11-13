# Quize-s-creator --> High-level architecture

*   **Frontend (client)**: Single-page app (React or Vue). Responsible for authoring UI, game play UI, dashboards, media uploads, responsive layout for projection and student devices.
    
*   **Backend API**: RESTful/GraphQL API (Node.js + Express/Nest or Python FastAPI or PHP Laravel if you prefer similarity to original). Handles auth, game CRUD, sessions, payments, analytics.
    
*   **Realtime service**: WebSockets (Socket.IO) or server-sent events for live game control, team updates, timers and leaderboards.
    
*   **Database**: Relational DB (Postgres) for users/games/permissions; optional document DB (MongoDB) for flexible question content/media metadata.
    
*   **File storage / CDN**: S3-compatible object storage + CDN (CloudFront, Cloudflare) for images/audio used in quizzes.
    
*   **Caching & session store**: Redis for caching, rate-limiting and session storage.
    
*   **Search & indexing**: ElasticSearch or Postgres full-text for fast game/content search and tagging.
    
*   **Payments & subscriptions**: Stripe (or Paddle) for freemium/paid features.
    
*   **Auth / SSO**: Email/password + OAuth (Google/Office365) + role-based access (teacher/admin/student).
    
*   **Analytics & logs**: Segment/Matomo for analytics; Sentry for error monitoring.
    
*   **Hosting / infra**: Docker containers on AWS (ECS / EKS) or managed services (Heroku / Render / Fly). Use IaC (Terraform) for repeatability.
