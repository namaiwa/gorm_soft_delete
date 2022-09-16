# xiaomate_libs

gorm 软删枚举字段类型


##### GORM 软删枚举
```golang
import sd "git.domob-inc.cn/xiaomate/xiaomate_libs/soft_delete"
//定义结构体时：
DeleteStatus sd.DeletedEnum `gorm:"deleteEnum:DELETE_STATUS_DEL;normalEnum:DELETE_STATUS_NORMAL;default:DELETE_STATUS_NORMAL"`
```
    其中：deleteEnum：删除的枚举值， normalEnum:正常的枚举值， default：插入的默认值
    可简写, 默认枚举值为 DELETE_STATUS_DEL 和 DELETE_STATUS_NORMAL：
```golang
//简写
DeleteStatus sd.DeletedEnum `gorm:"default:DELETE_STATUS_NORMAL"`
```

