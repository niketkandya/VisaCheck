The intent of this script to filter messages from the
`H1B_H4_Visa_Dropbox_slots` group so that it is manageable to look use info in
that group.

----TL;DR----

#####Background

usvisascheduling.com site that is used for Visa appointment booking in India has
several restrictions:
1. You can only check the site upto 3-4 times in a day.
2. You cannot use any browser plugins to automate any process.
3. There is a waiting room at the start which blocks you for an unknown amount of
time.

To overcome this, people created the above telegram group where they post
availability and everyone can benefit from that. However, currently that group
hs over 100K members and there is an update almost every minute. It is near
impossible to monitor that group.

This script helps you in monitoring the group for visa slot availability.
Basically, it reads all incoming messages in your group of interest(SUB) and
filters and forwards only those messsages that look relevant to a different
group(PUB) of your choice.

#####Steps
1. This script is written in python and uses a module called `Telethon` to do
   its job. So the first step is installing Telethon. You can do this by running
   the following in a terminal.

   ```pip3 install telethon```

2. You need to be a part of both your PUB and SUB groups.

3. Generate your api_id and api_hash by following instructions
[here](https://core.telegram.org/api/obtaining_api_id#obtaining-api-id) and
substitute in `TG_API_ID` and `TG_API_HASH` global variables and uncomment lines
19 and 20.

4. You can add other people to the PUB group ofcourse. Turn off notifications
   for the SUB group and enable it for the PUB group.

5. Run this script on an always on computer by doing the following.

   ```python3 print_messages.py```
