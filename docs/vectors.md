# Vectors
## Description
Vectors are used for everything postion-related. In Source, `y` and `z` axies are "flipped". That means that `z` is up-down and `y` is left-right.

## Syntax
### `vector3()`
**Arguments:**  
- `x` - Type: `number`  
- `y` - Type: `number`  
- `z` - Type: `number`  
**Returns:**  
- `vector` - Type: `vector3`

### `vecString()`
**Arguments:**  
- `vector` - Type: `vector3`  
**Returns:**  
- `string` - Type: `string`  

### `vecAdd()`
**Arguments:**  
- `vector1` - Type: `vector3`  
- `vector2` - Type: `vector3`  
**Returns:**  
- `vector` - Type: `vector3`  

### `vecSub()`
**Arguments:**  
- `vector1` - Type: `vector3`  
- `vector2` - Type: `vector3`  
**Returns:**  
- `vector` - Type: `vector3`  

### `vecMul()`
**Arguments:**  
- `vector1` - Type: `vector3`  
- `vector2` - Type: `vector3` or `number`  
**Returns:**  
- `vector` - Type: `vector3`  

### `vecCrossProduct()`
**Arguments:**  
- `vector1` - Type: `vector3`  
- `vector2` - Type: `vector3`  
**Returns:**  
- `vector` - Type: `vector3`  

### `vecDotProduct()`
**Arguments:**  
- `vector1` - Type: `vector3`  
- `vector2` - Type: `vector3`  
**Returns:**  
- `vector` - Type: `vector3`  

### `vecNormalize()`
**Arguments:**  
- `vector` - Type: `vector3`  
**Returns:**  
- `normalized_vector` - Type: `vector3`  

### `vecLength()`
**Arguments:**  
- `vector` - Type: `vector3`  
**Returns:**  
- `length` - Type: `number`  
