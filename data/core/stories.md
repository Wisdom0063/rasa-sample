## happy path 
* greet
  - action_hello_world
  - utter_greet
* mood_great
  - utter_happy
  - utter_how_can_help
> handle_pleasantries_happy


## sad path 
* greet
  - action_hello_world
  - utter_greet
* mood_unhappy
  - utter_sorry
  - utter_how_can_help
> handle_pleasantries_unhappy



## talk to agent
* talk_to_agent
  - utter_agent_will_respond
> handle_talk_to_agent


## goodbye
* goodbye
  - utter_goodbye
  - action_restart
<!-- > handle_goodbye -->


## about bot
* bot_challenge
  - utter_iamabot
> handle_botchallenge

## other help affirm
* affirm
    - utter_other_help
* affirm
    - utter_how_can_help
<!-- > handle_other_help_affirm -->


## other help deny
* affirm
    - utter_other_help
* deny
    - utter_goodbye
<!-- > handle_other_help_deny -->


## happy path 1 talk to agent and affirm other help
> handle_pleasantries_happy
> handle_talk_to_agent
* affirm
    - utter_other_help
* affirm
    - utter_how_can_help



## happy path 1 talk to agent and deny other help
> handle_pleasantries_happy
> handle_talk_to_agent
* affirm
    - utter_other_help
* deny
    - utter_goodbye


## sad path 1 talk to agent and affirm other help
> handle_pleasantries_unhappy
> handle_talk_to_agent
* affirm
    - utter_other_help
* affirm
    - utter_how_can_help


## sad path 1 talk to agent and deny other help
> handle_pleasantries_unhappy
> handle_talk_to_agent
* affirm
    - utter_other_help
* deny
    - utter_goodbye

 ## happy path 1 and bot challenge and affirm other help
> handle_pleasantries_happy
> handle_botchallenge
* affirm
    - utter_other_help
* affirm
    - utter_how_can_help

## happy path 1 and bot challenge and deny other help
> handle_pleasantries_happy
> handle_botchallenge
* affirm
    - utter_other_help
* deny
    - utter_goodbye

## sad path 1 and bot challenge and affirm other help
> handle_pleasantries_unhappy
> handle_botchallenge
* affirm
    - utter_other_help
* affirm
    - utter_how_can_help

## sad path 1 and bot challenge and deny other help
> handle_pleasantries_unhappy
> handle_botchallenge
* affirm
    - utter_other_help
* deny
    - utter_goodbye




