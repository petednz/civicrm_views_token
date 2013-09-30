civicrm_views_token
===================

add a mailing token to include a view. (look for 'Configured Drupal View' in the token box)

Drupal views are made as available as a token in CiviMail & in pdf / emails

NOTE - they do NOT work from the civimail test mailing which I think is a civimail
but.

Two ways to select your view
1) name it email (db name)
2)set the variable to the view name
-e.g  drush vset civicrm_views_token_views  nodequeue_1

Note that technically the module should support an array of views but that is not yet
tested

Make sure your view is set up with paging off & Hide contextual links is on

you will need to put css into your email template to format - e.g the CiviMail
template for the nodequeue_1 view with a tasteful & subtle colourscheme is

<style type="text/css">body {background-color:yellow;}
p {color:blue;}
</style>
<p>{civicrm_views_tokens.viewnodequeue_1}</p>

<p>&nbsp;</p>


