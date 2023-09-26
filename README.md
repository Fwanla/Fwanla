client.on("guildMemberAdd", member => {
  const channel = member.guild.channels.cache.find(channel => channel.name === "giriş-çıkış");
  if (!channel) return;
  const embed = new MessageEmbed()
    .setColor("#10f700")
    .setThumbnail(member.user.displayAvatarURL())
    .setTitle("Sunucuya Katıldı!")
    .setFooter({text:'Developer: Athenax'})
    .setDescription(`${member} Adlı Kullanıcı Sunucuya Katıldı!`)
    .setTimestamp();
    channel.send({embeds: [embed]})
});
