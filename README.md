import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;
import org.bukkit.plugin.java.JavaPlugin;

public class BanPlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        // Plugin aktivieren
    }

    @Override
    public void onDisable() {
        // Plugin deaktivieren
    }

    @Override
    public boolean onCommand(CommandSender sender, Command command, String label, String[] args) {
        if (command.getName().equalsIgnoreCase("ban")) {
            if (args.length == 1) {
                String playerName = args[0];
                // Hier kannst du den Spieler "playerName" bannen
                sender.sendMessage("Der Spieler " + playerName + " wurde gebannt.");
                return true;
            } else {
                sender.sendMessage("Verwendung: /ban <Spielername>");
                return false;
            }
        }
        return false;
    }
}
