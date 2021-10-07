module.exports = {
    name: "clear",
    aliases: ["purge", "nuke"],
    category: "moderation",
    description: "Очищает чат",
    clientPerm: ['MANAGE_MESSAGES'],
    memberPerm: ['MANAGE_MESSAGES'],
    onlyOwner: true,
    run: async (client, message, args) => {

        let messageSize = parseInt(args[0]);
        if (isNaN(messageSize) || parseInt(messageSize) <= 1) return message.reply("Укажите сколько сообщений удалить!");

        let member = message.mentions.users.first();
        let channel = message.channel;

        let msgDeletedPerCycle = 100;
        let messagesDeleted = 0;

        message.delete();
        await sleep(300);

        if (messageSize > 100)
            for (let i = 0; i <= parseInt(messageSize / 100); i++) {
                if (i == parseInt(messageSize / 100))
                    msgDeletedPerCycle = messageSize % 100;
                if (msgDeletedPerCycle != 0)
                    channel.messages.fetch({ limit: msgDeletedPerCycle }).then(messages => {
                        messages = member ? messages.filter(m => m.author.id === member.id).array().slice(0, messageSize) : messages.array();
                        message.channel.bulkDelete(messages);
                        messagesDeleted += messages.length;
                    });
                await sleep(5000);
            }
        else {
            channel.messages.fetch({ limit: messageSize }).then(messages => {
                messages = member ? messages.filter(m => m.author.id === member.id).array().slice(0, messageSize) : messages.array();
                message.channel.bulkDelete(messages);
                messagesDeleted += messages.length;
            });
        }

        await sleep(300);
        message.channel.send("Удалено " + messagesDeleted + " сообщений");
    }

}
function sleep(ms) {
    return new Promise((resolve) => {
        setTimeout(resolve, ms);
    });
}
