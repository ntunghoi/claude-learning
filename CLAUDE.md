# Planning Rules

Before editing code:
1. Analyze the current implementation
2. Explain architecture assumptions
3. List files to modify
4. Identify risks
5. Wait for confirmation before editing

# Response Format

Final output must include:
- files modified
- summary of change
- introduced risks
- unresolved issues
- follow-up recommendations

# Dependency Rules

Do not install new packages without approval. 

Prefer:
- native browser APIs
- existing internal utilities
- lightweight solutions

If a dependency is necessary:
- explain why
- compare alternative
- estimat bundle impact

# Design System Rules

- Use semantic tokens only
- Never hardcode colors
- Use existing spacing scale
- Minimum tap target: 44px
- Mobile-first layouts
- Prefer reusable primitives

# Code Standards

- TypeScript strict mode only
- Prefer functional components
- No inline styles
- Acessibility required
- Prefer composition over inheritance
- Avoid deep nesting
- Prefer early returns
- Keep functions small and focused
- Avoid creating files larger than 300 lines
- Prefer modularization

# Validation Workflow

After implementation:
1. Run lint
2. Run typescheck
3. Run unit tests
4. Fix all failures automatically

Never finish with failing checks. 

# Scope Control

Modify only files directly related to the requsted task. 

Do not:
- refactor adjacent systems
- rename or refactor unrelated files
- reorganize directories
- perform opportunistic cleanup
- rename for stylistic reason only

If broader changes are beneficial:
- explain them separately
- ask for approval

Stop and ask before:
- deleting files
- changing schema
- mdoifying environment variables
- editing secret/configuration
- changing auth flows

# Protected Areas

Claude must never modify these directories unless explicitly instructed:  

- /database/migrations

If a requested feature requres touching these areas:  
1. Explain why
2. List impacted files
3. Wait for approval

Do not create new migration files automically. 
Do not modify CI/CD workflows. 