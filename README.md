# are.na trmnl recipe plugin

Source code for a recipe to display random are.na channel blocks on the trmnl device

## Recipe direct install URL

Coming after approval from trmnl devs...

## installing 

1. Navigate to the trmnl website's <a href="https://usetrmnl.com/plugins">plugins page</a> then navigate to "private plugin."

2. Under advanced settings, set strategy to polling if it is not already. Then paste the following into "polling url(s)"

``https://api.are.na/v2/channels/{{ channel_id }}``

3. Then under "form fields" paste in content that will open up a field for the channel ID. In the published recipe (see trmnl_plugin_export/settings.yml), this means pasting the following 

``- keyname: author_bio
  name: About This Plugin
  field_type: author_bio
  description: Randomly displays a block from the desired are.na channel. Created by Jack Hester. Not officially affiliated with are.na.
- keyname: channel_id
  field_type: string
  placeholder: 'community-news-1afxa6bjvcc'
  name: Channel Name
  description: The name of the channel you want to display random blocks from.
  help_text: Get by taking the last part of the URL of the channel of interest. E.g. are.na/jack-hester/what-is-art-zyaobjea7by -> what-is-art-zyaobjea7by``

The channel_id section is strictly necessary.

4. You should then save, at which point it will prompt you to fill in the channel name. Set this as desired (examples would be: community-news-1afxa6bjvcc, what-is-art-zyaobjea7by). You can do this even if you do not own the channel. You only need to paste the channel name from the channel's web url, not the username or other parts of the url (see help_text above).

5. Save again, then go to "edit markup." Paste the exact code from the relevant .liquid size file in the trmnl_plugin_export folder. You must fill in at least one size to be able to display it.

6. Save again and set this plugin as part of your trmnl's recipe!
