# CustomECS
Toy ECS that improves performance by optimizing cache lines to not miss.

## Features
- Scenes
- Entity ID
- Components (Max 255)
  - Contiguous storage of components (cache optimization) via component pooling
  - User can register their own components
 
- Convenience Macros like *DECLARE_MEMBER_AND_ACCESSOR()*
