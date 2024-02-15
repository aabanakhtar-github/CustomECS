# CustomECS
Toy ECS that improves performance by optimizing cache lines and preventing cache misses

## Features
- Scenes
- Entity ID, (Max 10'000, can be modified)
- Components (Max 32, can be modified)
  - Contiguous storage of components (cache optimization) via component pooling
  - User can register their own components
 
- Convenience Macros like *DECLARE_MEMBER_AND_ACCESSOR()*
