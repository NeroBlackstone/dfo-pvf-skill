# DNF 动画文件 (.ani) 格式参考

## 文件位置

动画文件位于 `character/[job]/animation/` 目录下，如：
- `character/swordman/animation/attack1.ani`
- `character/fighter/animation/attack1.ani`

## .ani 文件结构

```
#PVF_File

[FRAME MAX]     总帧数

[FRAME000]
    [IMAGE]        `img路径`  帧索引
    [IMAGE POS]    X偏移  Y偏移
    [DELAY]        毫秒
    [DAMAGE BOX]   相对X  相对Y  相对Z  宽度  高度  深度
    [ATTACK BOX]   攻击判定区域（部分帧有）

[FRAME001]
    ...
```

## 帧字段说明

| 字段 | 说明 |
|------|------|
| `[IMAGE]` | 贴图路径（printf格式如 `%04d` 表示帧号），及帧索引 |
| `[IMAGE POS]` | 角色基准点偏移 |
| `[DELAY]` | 该帧持续时间（毫秒） |
| `[DAMAGE BOX]` | 伤害判定区域（hitbox） |
| `[ATTACK BOX]` | 攻击判定区域（部分技能帧有） |

## DAMAGE BOX / ATTACK BOX 格式

```
相对X  相对Y  相对Z  宽度  高度  深度
```

## Swordman 基础攻击动画

### Attack1 (Z键第一下)
- 文件: `character/swordman/animation/attack1.ani`
- 帧数: 10帧 (FRAME000-FRAME009)
- IMG: `Character/Swordman/Equipment/Avatar/skin/sm_body%04d.img`
- 帧索引: 0-9

### Attack2 (Z键第二下)
- 文件: `character/swordman/animation/attack2.ani`
- 帧数: 11帧
- IMG: `sm_body%04d.img` 帧 10-20

### Attack3 (Z键第三下)
- 文件: `character/swordman/animation/attack3.ani`
- 帧数: 9帧
- IMG: `sm_body%04d.img` 帧 33-41
