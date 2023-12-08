# XCOM 2 - WAR OF THE CHOSEN - MASTER MATERIALS
**A list of important native WOTC master materials and their native material instance options.**
<br>Included In: `Materials_XPack`

> [!CAUTION]
> Do not modify native master materials when creating mods; this will affect all base game and mod material instances.
> <br>Create a copy of a native master material if you wish to modify the functionality of a specific master material.

> [!NOTE]
> The explained master materials below are the important ones used by many assets rather than every master material.
> <br>This is for the sake of page length, as their are 36 master materials in total built for WOTC.

> [!NOTE]
> UDK Materials & Textures Link: [MaterialsAndTexturesHome](https://docs.unrealengine.com/udk/Three/MaterialsAndTexturesHome.html)

-------------

# UnitArmor_M
**Used with faction soldier armor assets.**
> [!IMPORTANT]
> Material Function Dependencies: StandardMetalic , ClothFuzz

> [!NOTE]
> Master Material Variations: UnitArmor_M_ClearCoat , UnitArmor_M_OpacityMasked

> [!NOTE]
> Example Material Instance: Skirmisher_Helmets > Materials > Skirmisher_Helmet_A

-------------

<details>

<summary>Shared Textures</summary>

## Shared Textures

| Cloth Mask | One Channel Texture |
|     :---:      |     :---:      |
| Red   | Cloth Mask |
| Green | Black |
| Blue  | Black |
| Alpha | White |

| Emissive Mask | One Channel Texture |
|     :---:      |     :---:      |
| Red   | Emissive Mask |
| Green | Black |
| Blue  | Black |
| Alpha | White |

| Pattern Mask | Two Channel Texture |
|     :---:      |     :---:      |
| Red   | Primary Pattern Tint Mask |
| Green | Secondary Pattern Tint Mask |
| Blue  | Black |
| Alpha | White |

| Diffuse | Default Texture |
|     :---:      |     :---:      |
| Red   | Base Color |
| Green | Base Color |
| Blue  | Base Color |
| Alpha | Roughness |

| Metallic Mask | Two Channel Texture |
|     :---:      |     :---:      |
| Red   | Metallic Mask |
| Green | Occlusion Map |
| Blue  | Black |
| Alpha | White |

| Normal | Normal Texture |
|     :---:      |     :---:      |
| Red   | Normal X |
| Green | Normal Y |
| Blue  | Normal Z |
| Alpha | White |


</details>

<details>

<summary>UnitArmor_M_ClearCoat Textures</summary>

### UnitArmor_M_ClearCoat Textures

| Clear Coat Mask | One Channel Texture |
|     :---:      |     :---:      |
| Red   | Clear Coat Mask |
| Green | Black |
| Blue  | Black |
| Alpha | White |

</details>

<details>

<summary>UnitArmor_M_OpacityMasked Textures</summary>

### UnitArmor_M_OpacityMasked Textures

| Opacity Mask | One Channel Texture |
|     :---:      |     :---:      |
| Red   | Opacity Mask |
| Green | Black |
| Blue  | Black |
| Alpha | White |

</details>

-------------

<details>

<summary>Shared Properties</summary>

## Shared Properties

| Cloth | Optional | An effect for mimicking how light interacts with cloth. |
|     :---:      |     :---:      |     :---:      |
| Cloth Fuzz   | Float   | 0.500000 |
| Cloth Mask   | Texture | Texture2D'Materials_XPack.Textures.BlackRG' |
| Enable Cloth | Boolean | False |

| Debug | Optional | Adjusts the strength of the roughness & specularity outputs. |
|     :---:      |     :---:      |     :---:      |
| Roughness Scale | Float | 1.000000 |
| Specular Scale  | Float | 1.000000 |

* Only use the above debug scales if you need to preview changes you should then make to your roughness map or metallic mask.

| Emissive | Optional | Affects the colored lightmap generation of the mesh. |
|     :---:      |     :---:      |     :---:      |
| Emissive Color  | Color   | { 1.000000, 1.000000, 1.000000, 1.000000 } |
| Emissive Mask   | Boolean | Texture2D'Materials_XPack.Textures.BlackRG' |
| Emissive FLow   | Texture | False |
| Emissive Scale  | Float   | 1.000000 |
| Enable Emissive | Boolean | False |

* Emissive FLow enables a scrolling effect that modulates the constant emissive scale.

| Pattern | Real-Time | Alters the tint mask of the tinting parameters. |
|     :---:      |     :---:      |     :---:      |
| Non Square Tiling | Boolean | False |
| Pattern           | Texture | Texture2D'Materials_XPack.Textures.BlackRG' |
| Pattern Use       | Float   | 0.000000 |
| Pattern UV Scale  | Float   | 2.000000 |

* While Pattern Use is a Float value, the value acts as a Boolean, so the value should only ever be 0 or 1.

| Textures | Required | The base textures that make up the base layers of a mesh. |
|     :---:      |     :---:      |     :---:      |
| Diffuse      | Texture | Texture2D'Materials_XPack.Textures.GrayRGBA' |
| MetallicMask | Texture | Texture2D'Materials_XPack.Textures.BlackR_WhiteG' |
| Normal       | Texture | Texture2D'Materials_XPack.Textures.NormalRGB' |

| Tinting | Optional | Alters the base color of a mesh. |
|     :---:      |     :---:      |     :---:      |
| Enable Tinting              | Boolean | False |
| Legacy Tinting              | Boolean | False |
| Primary Color               | Color   | { 1.000000, 0.000000, 0.000000, 1.000000 } |
| Secondary Color             | Color   | { 0.000000, 1.000000, 0.000000, 1.000000 } |
| Secondary Color As Emissive | Boolean | False |
| Tint Mask                   | Texture | Texture2D'Materials_XPack.Textures.BlackRG' |

* Legacy Tinting will use a much simpler calculation for altering the base color used for XCOM EU / EW assets.

</details>

<details>

<summary>UnitArmor_M Properties</summary>

### UnitArmor_M Properties

| Scalar Parameter Values | Optional | Miscellaneous parameters. |
|     :---:      |     :---:      |     :---:      |
| Pans Speed And Direction | Float | -0.050000 |

* Pan Speed And Direction will alter the scrolling speed & direction of the Emissive FLow parameter option.

</details>

<details>

<summary>UnitArmor_M_ClearCoat Properties</summary>

### UnitArmor_M_ClearCoat Properties

| Textures | Required | The base textures that make up the base layers of a mesh. |
|     :---:      |     :---:      |     :---:      |
| Add Clear Coat Mask  | Boolean | False |
| Clear Coat Mask      | Texture | Texture2D'Materials_XPack.Textures.BlackR_WhiteG' |
| CLear Coat Roughness | Float   | 0.200000 |

</details>

<details>

<summary>UnitArmor_M_OpacityMasked Properties</summary>

### UnitArmor_M_OpacityMasked Properties

| Textures | Required | The base textures that make up the base layers of a mesh. |
|     :---:      |     :---:      |     :---:      |
| Opacity Mask | Texture | Texture2D'Materials_XPack.Textures.WhiteRG' |

</details>
