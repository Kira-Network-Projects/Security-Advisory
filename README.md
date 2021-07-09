##Security-Advistory

This repoistory contains general information about our security and what you can feel safe about on our network.


##General Information

Our network does store your ip address but it is not the ip that you would normally think. A normal IP in our collection would look something like this:

`ODVkMWQ5M2MxOWNiMjljMDk4YzdjZWJkNTFhMmFhNWM1YmY2MGU1MDRiMzZiZDAzZmU1NzcxNWI3
MWFmNzViMw==`

That ip uses two different methods to "obfuscate" the ip address which is we first use a method to hex the string and make it just numbers and letters then we encode the hexed ip address to make an output that looks something like that

##Our Guidelines

We do allow the use of VPNs because wee do want people to feel safe on our network but if you do actually want to play on your main IP and are scared of what might happen contact me on telegram or discord (@ign98ping or 98ping#3040) and I will willingly send you your profile document that contains stats such as your username, ip, uuid, active prefix, ect.

They look something like this:

`Document document = new Document("uuid", String.valueOf(uuid))
                .append("username", profile.getUsername())
                .append("firstJoined", profile.getFirstJoined())
                .append("lastSeen", profile.getLastSeen())
                .append("staffChat", profile.isStaffChat())
                .append("activePrefix", (profile.getActivePrefix() == null ? null : profile.getActivePrefix().getId()))
                .append("activePrefix", (profile.getActivePrefix() == null ? null : profile.getActivePrefix().getId()))
                .append("ip", CipherHelper.base64encode(EncryptionHelper.toHexString(profile.getIp())))
                .append("currentServer", profile.getCurrentServer())
                .append("disguisedRank", profile.getDisguisedRank())
                .append("playerperms", profile.getPlayerperms())
                .append("disguised", profile.isDisguised())
                .append("friends", ListTransformUtils.UUIDtoStringList(profile.getFriends()));
        ProjectXShared.getInstance().getMongoManager().getProfiles().insertOne(document);`
