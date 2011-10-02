# ordr.in #

[ordr.in][ordr.in] is a website that lets you order food online, and offer a great api.
Being the hungry developer I am, I wanted to never have to lift my hands from these glowing
keys.

Benefits include:
* reduced exposure to cell phone radiation
* reduced hand movement, no need to use the mouse!

## installation ##

```gem install ordr.in-cli```

## usage ##

`ordr.in` to display the help
`ordr.in [cuisine] from <zip>` show restaurants and their id's serving [cuisine] in <zip>
`ordr.in categories <id>` show menu categories from restaurant with <id>
`ordr.in menu <id> [for <category>]` show the menu for the specified restaurant <id>, trimmed to the specific <category>, which is a number, if it is included, includes price, description, price, id
`ordr.in compile_tray <id> <quantity>, <id> <quantity>,...` compile a collection of food <id>s and their <quantities>.`ordr.in order 
`ordr.in order <restaurant id> <tray> <tip> <email> <first name> <last name> <street address> <town> <state> <zip> <cc number> <cc security code> <expiration month><expiration year (2 digits)>` The motherload of all commands.
This grabs your compiled <tray>, cc information and assumes that your billing address is the same as the ordering address. You're not leaving your house anyway, why should that change?


## future usage ##

`ordr.in make_account <email> <password> <first name> <last name>` make an ordr.in account to save your credentials for easy ordering
`ordr.in log_in <email> <pass>` log in to ordr.in to enable faster ordering
`ordr.in add_card <nick> <full name> <cc number> <security code> <expiring month [1-12]> <expiring year> <street address> <street address 2> <town> <state> <zip> <phone number>` make a new card associated to a user, must be logged in first
`ordr.in remove_card <nick>` delete a credit card with <nick>, must be logged in
`ordr.in order_history [order]` show order [order], no order returns a full history
