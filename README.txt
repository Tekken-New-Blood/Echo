To apply new code to Echo just copy and paste into the chat. I use #test usually.

This line taken from mymain.txt line 6 will be the example:

    ParamRegex.((?i)Nina\s?(Williams)?)?:{role:Nina Williams}{/user} mains Nina Williams

?:{role:Nina Williams}
    This is the meat of giving someone a role. Whatever is in brackets will be run if the condition before it is met.

{/user} mains Nina Williams
    This is what echo says in chat. {/user} mentions the user that called .mymain

ParamRegex.(...)
    This tells echo to look at the parameter using Regex to see if it matches whatever is in parenthesis. Note that "?:{" is after the condition so that is not what Regex looks at. It gets confusing because ?'s are used in Regex

(?i)
    This is a flag to declare the rest of the Regex as being "case (i)nsensitive"

\s?
    I think I remember you saying that you know Regex but to be safe "\s" is any whitespace character and the ? after it makes it optional for the user

(Williams)?
    Again this says that Williams with any case insensitivity is optional for the condition of Nina being met

Note:

    Discord can only have so many characters in a message which is why larger commands like ".iamnot" are split up.

    iamnot.txt:

        22 Response.nil?:{ars:iamnot2}
        23
        24 .auto iamnot2={init}
        25 {arslock}

    Response.nil is basically "else." It calls .iamnot2 with the original parameter given to .iamnot.
    {arslock} prevents iamnot2 from being called. Not needed to function but I thought it was a nice touch.
