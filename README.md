# yotyot_plugin
## THis is Mc plugin for open crafting table and ender chest GUI.
### commands :
```
  //craftingtable
  //enderdhest
```
------------------------------------------------------------------------
 
 ### source (java) : 
 
 ```
 package yotyot;

import org.bukkit.Bukkit;
import org.bukkit.ChatColor;
import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;
import org.bukkit.entity.Player;
import org.bukkit.inventory.Inventory;
import org.bukkit.plugin.java.JavaPlugin;

public class Yotyot extends JavaPlugin{
	@Override
	public void onEnable() {
		System.out.println(ChatColor.AQUA +"욧욧 플러그인 ver.1 활성화..");
	}
	@Override
	public void onDisable() {
		System.out.println(ChatColor.AQUA +"욧욧 플러그인 ver.1 비활성화..");
	}
	
@Override
public boolean onCommand(CommandSender sender, Command cmd, String label, String[] args) {
	if(cmd.getName().equalsIgnoreCase("/craftingtable")) {
		if(sender instanceof Player) {
			sender.sendMessage(ChatColor.AQUA +"open crafting table ");
			Player p = (Player)sender;
			p.openWorkbench(null, true);
			return false;
		}
		sender.sendMessage(ChatColor.AQUA +"이 명령어는 플레이어만 사용이 가는합니다.");
		return false;
	}else if(label.equalsIgnoreCase("/enderchest")) {
    sender.sendMessage(ChatColor.AQUA +"open ender chest ");
		Player p = (Player)sender;
		p.openInventory(p.getEnderChest());
	}
return true;
}
}
```

### plugin.yml : 
```
name: yotyot
version: 1.0
main: yotyot.Yotyot

commands: 
  /craftingtable:
  /enderchest:
```
------------------------------------------------------------------------
 
 ### maker : yot_yot(minecraft nickname)
