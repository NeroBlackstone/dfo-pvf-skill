# DNF 怪物文件 (.mob) 格式参考

## 文件位置

怪物文件位于 `monster/[type]/` 目录下，如：
- `monster/zombie/zombiezombie.mob`
- `monster/skeleton/skillskeleton.mob`

## .mob 文件结构

```
#PVF_File

[name]           怪物名称
[type]           怪物类型
[level]          等级
[hp]             生命值
[attack]         攻击力
[defense]        防御力
[move speed]     移动速度
[ai]             AI行为类型
[attack type]    攻击类型
[skill]          使用的技能列表
```

## 常见字段说明

| 字段 | 说明 |
|------|------|
| `[name]` | 怪物显示名称 |
| `[type]` | 怪物分类（undead, beast, demon等） |
| `[level]` | 怪物等级 |
| `[hp]` | 生命值 |
| `[attack]` | 物理攻击力 |
| `[magic_attack]` | 魔法攻击力 |
| `[defense]` | 物理防御力 |
| `[magic_defense]` | 魔法防御力 |
| `[ai]` | AI行为脚本名称 |

## AI 行为文件

AI行为定义位于 `aicharacter/` 目录，对应 `.mob` 中的 `[ai]` 字段。

## 怪物类型目录

- `monster/zombie/` - 僵尸类
- `monster/skeleton/` - 骷髅类
- `monster/demon/` - 恶魔类
- `monster/beast/` - 野兽类
