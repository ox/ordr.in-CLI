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

`ordr.in [cuisine] around <zip>` show restaurants and their id's serving [cuisine] in `<zip>`

`ordr.in categories <id>` show menu categories from restaurant with `<id>`

`ordr.in menu <id> [for <category>]` show the menu for the specified restaurant `<id>`, trimmed to the specific `<category>`

`ordr.in compile_tray <id> <quantity> <id> <quantity> ...` compile a collection of food `<id>`s and their `<quantities>`.

`ordr.in order <restaurant id> <tray> <tip> <email> <first name> <last name> <street address> <town> <state> <zip> <phone number> <cc number> <cc security code> <expiration month><expiration year (2 digits)>` The motherload of all commands.

This grabs your compiled `<tray>`, cc information and assumes that your billing address is the same as the ordering address. You're not leaving your house anyway, why should that change?

`ordr.in user make_account <email> <password> <first name> <last name>` make an ordr.in account to save your credentials for easy ordering. This creates a '~/.ordr.in.acct' file which holds some common info about you.

`ordr.in user order <id> <tray> <tip> <cc num> <cc sec> <cc exp mon><cc exp year>` order food when you have an account. ~/.ordr.in.acct needs to exist

## future usage ##

this depends soley on when ordr.in enables account creation via their API.

`ordr.in add_card <nick> <full name> <cc number> <security code> <expiring month [1-12]> <expiring year> <street address> <street address 2> <town> <state> <zip> <phone number>` make a new card associated to a user, must be logged in first
`ordr.in remove_card <nick>` delete a credit card with <nick>, must be logged in
`ordr.in order_history [order]` show order [order], no order returns a full history

## ~/.ordr.in.acct ##

This is a file which holds your email, password, first name, laste name, street, town, state, zip, phone number for easy access when ordering again and again.