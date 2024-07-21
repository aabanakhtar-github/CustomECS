# CustomECS
Toy ECS that improves performance by optimizing cache lines and preventing cache misses. Based on the framework by Austin Molan.

## Example
```C++
// define a component
struct pos_component : ECS::ComponentBase {
  float x, y; 
};

// make the game scene and register components
ECS::Scene scene;
scene.registerComponent<pos_component>();

// create an entity
ECS::EntityID entity = scene.createEntity();
scene.addComponent<pos_component>(entity) = {
  .x = 0, .y = 10
};

// "system"
SceneView<pos_component> view(scene);
for (auto ID : view.getEntities()) {
  auto& pos = scene.getComponent<pos_component>(ID);

  // do some operations
  pos.x += 3;
  pos.y += 5; 
}
```
