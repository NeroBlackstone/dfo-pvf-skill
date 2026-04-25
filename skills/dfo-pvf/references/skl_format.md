# DNF 技能文件 (.skl) 格式参考

## 文件位置

技能文件位于 `skill/[job]/` 目录下，如：
- `skill/swordman/basicattackup.skl` - 基础精通
- `skill/atfighter/closepunch.skl` - 接近拳
- `skill/swordmanskill.lst` - 技能列表索引

## .skl 文件结构

```
#PVF_File

[name]           技能名称（中文）
[name2]          技能名称（英文）
[explain]        技能说明
[type]           `[active]` 或 `[passive]`
[skill class]    职业编号
[maximum level]  最大等级
[icon]           图标路径  图标索引
[level info]     等级属性数据
[required level]  前置等级要求
[purchase cost]  购买价格
```

## 职业编号 (skill class)

| 编号 | 职业 |
|------|------|
| 0 | 通用/基础 |
| 1 | Swordman |
| 2 | Gunner |
| 3 | Mage |
| 4 | Priest |
| 5 | Thief |
| 6 | Demonicswordman |
| 7 | Fighter |
| ... | ... |

## 字段说明

| 字段 | 说明 |
|------|------|
| `[name]` | 技能显示名称 |
| `[type]` | `active`=主动技能, `passive`=被动技能 |
| `[icon]` | 技能图标路径和索引 |
| `[level info]` | 每级属性值变化 |

## 技能列表文件

- `skill/skilllist.lst` - 所有技能列表
- `skill/swordmanskill.lst` - 战士职业技能列表
