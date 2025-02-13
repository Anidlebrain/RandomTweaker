# Function

## isReady

决定当前 Tick 是否触发 `performEffect` 函数

### 导包

```zenscript
import mods.randomtweaker.cote.PotionIsReady;
```

* duration as int 药水时间

* amplifier as int 药水等级

```zenscript
potionObj.isReady = function(duration, amplifier) {
	if (duration % 20 == 0) {
		return true;
	}
	return false;
};
```

## performEffect

此函数每 Tick 都会调用

### 导包

```zenscript
import mods.randomtweaker.cote.PotionPerformEffect;
```

* living as [IEntityLivingBase](https://docs.blamejared.com/1.12/en/Vanilla/Entities/IEntityLivingBase/) 具有此药水效果的有生命实体

* amplifier as int 药水等级

```zenscript
potionObj.performEffect = function(living, amplifier) {
 	if(!living.world.remote && living instanceof Player) {
		var player as Player = living;
		player.sendChat("didiidid~~~");
	}
};
```

## affectEntity

此函数仅 `Potion` 的 `instant` 为 `true` 时触发

### 导包

```zenscript
// 这不是一个错误
import mods.randomtweaker.cotx.PotionPerformEffect; 
```

* living as [IEntityLivingBase](https://docs.blamejared.com/1.12/en/Vanilla/Entities/IEntityLivingBase/) 具有此药水效果的有生命实体

* amplifier as int 药水等级

```zenscript
potionObj.affectEntity = function(living, amplifier) {
 	if(!living.world.remote && living instanceof Player) {
		var player as Player = living;
		player.sendChat("didiidid~~~");
	}
};
```
